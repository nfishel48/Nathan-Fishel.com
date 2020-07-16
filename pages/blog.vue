<template>
  <section>
   <script src="https://kit.fontawesome.com/4faac6e63e.js" crossorigin="anonymous"></script>
   <section>
      <div class="columns">
        <div  class="column main-text">
          <h1>Welcome to my Blog</h1>
      </div>
      </div>
   </section>

   <section>
       <div class="columns">
           <div class="column">
                <div id="body">
                    <article class="media" v-for="(posts, index) in blog" :key="index">
                        <div class="media-content">
                            <div class="content" >
                      
                            <h3>{{ posts.title }}</h3>
                              
                            <p>{{ posts.content }}</p>
                            </div>
                            <nav class="level is-mobile">
                            <div class="level-left">
                                <a class="level-item" :href='posts.link'>
                                  <p>Read more</p>
                                </a>
                            </div>
                            </nav>
                        </div>
                    </article>
                </div>
            </div> 
       </div>
   </section>
   
  <div style="padding-bottom: 100px;"></div>




  </section> 
</template>


<script>
export default {
  layout: "navbar",
  data(){
    return{
      blog: [
        
        { title: 'Why your website needs to be fast & how to speed it up', 
        content: 'Weather your website serves strictly as marketing material or it is your main platform for business, you need to have a fast website. Most people only have an attention span of 8-9 seconds, if users have to wait for your site to load any longer than 1-2 seconds they will leave. ',
        link: '/'},
        
         { title: 'Why you should be using Django for your next web project', 
        content: 'Finding the right tools for a project can sometimes be harder than the actual project itself. In this blog post I will discuss Django, a tool that I think everyone should try for their next web-based project...',
        link: '/article2'},

         { title: 'What is Google BigQuery ', 
        content: 'Have you ever spent hours waiting for a SQL query to finish running? Google has a solution for this. Google BigQuery is a data warehousing tool that enables scalable, cost-effective and fast analysis over petabytes of data...',
        link: '/article1'},

        { title: 'Next Post coming soon', 
        content: '',
        link: '/'}
      ]
    }
  },

head: {
  meta: [
    { charset: 'utf-8' },
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link:[{
    href: 'https://fonts.googleapis.com/css2?family=Spartan:wght@400;700&display=swap', rel: "stylesheet"
  }]
},

}
</script>
