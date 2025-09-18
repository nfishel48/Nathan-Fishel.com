---
title: "Why I Chose Elixir & Phoenix for My High-Throughput Sports Analytics Platform"
date: 2025-09-17T23:01:03-04:00
draft: false
tags:
- Elixir
- Phoenix
- Concurrency
- DevOps
- Side Project
type: post
---

![alt text](/images/cardinal-dashboard.jpg "A dashboard showing sports analytics data")

## The Challenge: A Tsunami of Athlete Data

When I first started building Cardinal, my sports load forecasting side project, I hit a massive technical wall almost immediately. The core idea was to process a firehose of data from athlete wearables in real-time, run complex analytics, and instantly serve those insights to users. But how could one person build a system that wouldn’t buckle under that kind of load?

My system had to meet two demanding, simultaneous requirements:
1.  **Massive Ingestion and Processing:** Each incoming data point kicks off a complex, multi-stage pipeline I designed—downloading files, parsing binary data, running calculations, updating forecasts, and storing results. This is heavy, asynchronous background work that absolutely cannot interfere with the user experience.
2.  **Real-Time Delivery:** At the same time, coaches and trainers are logged in, watching dashboards, and expecting to see insights from this data the moment it's processed. I needed to provide a responsive, real-time connection.

A traditional threaded web framework would mean spinning up threads for background jobs and using another set of threads to handle user requests. I knew from experience this would lead to resource contention, complex state management, and a constant battle against performance bottlenecks. I needed something fundamentally different if I was going to pull this off alone.

## Why Elixir? The Superpower of Concurrency

I chose Elixir because it's built on the Erlang Virtual Machine (BEAM), a battle-tested platform created to run the world's telephone systems. Its purpose was to handle millions of concurrent connections with extreme reliability. It achieves this not with heavy operating system threads, but with incredibly lightweight "processes."

Here’s the analogy I use: a traditional framework is like a factory with a few large, heavy-duty conveyor belts (threads). If one gets jammed, it can slow everything down. The BEAM, on the other hand, is like giving me millions of tiny, intelligent drones (processes) that can each carry a small task independently. If one drone fails, it doesn’t affect the others, and a "supervisor" drone I’ve set up can instantly launch a new one to take its place.

This is the "let it crash" philosophy that makes Elixir systems so fault-tolerant. In Cardinal, this means if the parsing of one athlete's file fails, it won't crash the ingestion pipeline for every other athlete. My supervisor simply logs the error and moves on.

## My Architecture in Action

The elegance of Elixir and Phoenix allowed me to build a system that is both powerful and surprisingly simple. When a new activity file is ready from Garmin, their server sends a "ping" to one of my Phoenix endpoints. This endpoint is incredibly lean; its only job is to acknowledge the request and immediately schedule a background job using **Oban**, a robust job processing library for Elixir.

As you can see in my `GarminActivityWorker`, this job then takes over the heavy lifting: securely downloading the file, calling a native C++ `FitDecoder` NIF I wrote to parse the binary data, and storing the raw "seconds" data. By offloading this work instantly, my web server stays free to handle user requests without getting bogged down. Because Elixir processes are so cheap, I can run tens of thousands of these ingestion jobs concurrently without my server breaking a sweat.

## The Killer Feature: Real-Time Dashboards

My favorite feature in Cardinal is the live-updating chart. A coach can literally watch a player's performance metrics change in real-time as new data is processed. I was able to build this thanks to **Phoenix Channels**, a seamless abstraction over WebSockets.

The flow I designed is beautiful in its simplicity:
1.  A background worker, like my `MetricsWorker`, finishes its calculations.
2.  It publishes an update using `Phoenix.PubSub` to a topic, like `"team:123"`.
3.  Every user subscribed to that topic via their `UserSocket` instantly receives the new data.
4.  The frontend JavaScript updates the charts.

This entire process, from data ingestion to a visual update on a user's screen, happens in seconds. And the scalability is astounding. A single Phoenix server can handle up to **2 million simultaneous WebSocket connections**.

## The Payoff: Performance, Scalability, and Cost

The raw power and efficiency of the BEAM have a direct impact on this project. As I mentioned in my tweet, a single Phoenix server can process an estimated **17,000 Oban jobs per second**.

What does this mean for me? I can handle a massive volume of data and a large number of real-time users with a remarkably small server footprint. This translates directly to **lower infrastructure costs**, a crucial factor for a personal side project. Choosing Elixir and Phoenix wasn't just about picking a cool technology; it was about leveraging a platform purpose-built for the exact problem I was trying to solve.
