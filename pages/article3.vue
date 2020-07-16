<template>
    <section>
        <div style="padding: 20px;" ></div>
        <div class="hero is-info">
        <div style="padding: 20px;" ></div>
        <div class="hero-body">
        <div class="container">
        <h1 class="title">
           Why your website needs to be fast and how to speed it up.
        </h1>
        <h2 class="subtitle">
        Weather your website serves strictly as marketing material or it is your main platform for business, you need to have a fast website. 
        Most people only have an attention span of 8-9 seconds, if users have to wait for your site to load any longer than 1-2 seconds they will leave.
        Websites that load faster have higher engagement and higher conversions. Site speed is also part of the google page ranking algorithm.
        </h2>
        <h2 class="subtitle" >
        But how do you speed up your website?
        </h2>
        <ol>
            <li>Poorly written JavaScript can block your page form loading. Changing script to load asynchronous can help remove the blockage. Removing any unnecessary scripts can help as well, having every little thing animated does not help if people leave your site before it loads.</li>
            <li>Lots of static files such as images, and large stylesheets can be a problem. The best way to speed up serving static files is using a CDN or at the very least hosting files on a separate cloud server like Amazon S3 or Google Cloud Storage. This can reduce the bandwidth used by your webserver and let your site load first and load the images when it can. Images can be large files and a CDN will store your files on server around the globe so they may be served faster to users further away.</li>
            <li>Too many HTTP requests can slow down your site. 80% of the load time is spent downloading parts of the website this way. To reduce Http Requests, you should remove any unnecessary requests and combine files that can be combined. </li>
            <li>Lastly you need to verify you are using the best possible host for your use case. With shared hosting, you may save money, but your site will be underprepared if a spike in users happens. The best option for most site will be using a Virtual Private Server like one provided by Amazon web services. These operate on a pay for what you use pricing and will be ready if you web traffic picks up.</li>
        </ol>
        </div>
    </div>
    </div>
    </section>
</template>

<script>
export default {
  layout: "navbar",

 data () {
    return {
      title: 'Nathaniel Fishel',
      year: '2020'
    }
  },
  head () {
    return {
      title: this.title,
      
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        { hid: 'description', name: 'article3', content: 'Why your website needs to be fast & how to speed it up.' },
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        { link:[{
            href: 'https://fonts.googleapis.com/css2?family=Spartan:wght@400;700&display=swap', rel: "stylesheet"
      }]} 
      ]

    }
  },
}
</script>
