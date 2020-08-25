<template>
  <section>
   <script src="https://kit.fontawesome.com/4faac6e63e.js" crossorigin="anonymous"></script>
   
   <!-- Intro section -->
   <section class="section" style="background-color: #2c2c2c;">
     <div class ="container">
        <div class="columns">
          <div  class="column main-text">
            <h1 style="color: white;">Nathaniel Fishel</h1>
            <div id="buttons">
              <b-button tag="router-link" :to="{ path: '/portfolio' }" class="button is-medium is-link">View my work</b-button>
              <b-button tag="router-link" :to="{ path: '/about' }" class="button is-medium">Read my résumé</b-button>
            </div>
          </div>
        

          <div class="column main-text">
              <span id="github" class="icon">
                <a href="https://github.com/nfishel48">
                  <i class="fab fa-github"></i>
                </a>
              </span>
              <span id="linkedin" style="padding-left: 10%;" class="icon">
                <a href="https://www.linkedin.com/in/nathaniel-fishel-722a72165/" >
                  <i class="fab fa-linkedin"></i>
                </a>
              </span>
          </div>
        </div>
     </div>
   </section>
   <!------------->

   <!-- About me section -->
       <section class="section" style="background-color: #424242;">
        <h1 class="main-text" style="color: white;">About me</h1>
     <div class="padding">
     </div>
      
        <div class="tile is-ancestor">
           
            <div class="tile is-vertical is-4">
                <div class="tile">
                <div class="tile is-parent is-vertical">

                    <article class="tile is-child notification is-blue">
                    <p class="title">Education</p>
                    <p class="subtitle">Pursing Bachelor of Science (2021)</p>
                    <p class="subtitle">Eastern Michigan University- Ypsilanti MI</p>
                    <p class="subtitle">Major: Computer Science – Applied</p>
                    <p class="subtitle">Received Education First Scholarship – Full tuition</p>
                    <p class="subtitle">Relevant courses:</p>
                    <div class="content">
                        <ul>
                            <li>Algorithms and Data structures</li>	
                            <li>Computer Organization </li>
                            <li>Programming Languages</li>		
                            <li>Discrete Mathematics </li>
                            <li>Operating systems</li>
                            <li>Database Principles</li>
                        </ul>
                    </div>
                    </article>
                    <article class="tile is-child notification is-grey">
                    <p class="title">Languages and Frameworks</p>
                    <p class="subtitle">Backend:</p>
                    <div class="content">
                        <ul>
                            <li>Java</li>
                            <li>Python</li>
                            <li>C</li>
                            <li>PHP</li>
                            <li>SQL</li>
                        </ul>
                    </div>
                        <br>
                    <p class="subtitle">Frontend:</p>
                    <div class="content">
                        <ul>
                            <li>HTML and CSS</li>
                            <li>JavaScript</li>
                            <li>Vue.js</li>
                            <li>Nuxt.js</li>
                        </ul>
                    </div>
                    </article>
                </div>
        </div>

    <div class="tile is-parent">
      <article class="tile is-child notification is-blue">
        <p class="title">Certifications:</p>
        <div class="content">
          <ul>
              <li>Google Analytics Individual Certification (2020)</li>
              <li>CDE-SPARK Digital Media Certification (2020)</li>
              <li>CompTIA A+ Certificate (2016)</li>
              <li>Microsoft Technology Associate: Windows OS, Security, and Network Fundamentals (2017) </li>
              <li>Certified Microsoft Office Specialist (2017)</li>
          </ul>
        </div>
      </article>
    </div>
  </div>

  <div class="tile is-parent">
    <article class="tile is-child notification is-greytwo">
      <div class="content">
        <p class="title">Experience:</p>
        <p class="subtitle">Data Engineering Intern, Impellia, 6/15/2020-8/15/2020</p>
        <div class="content">
            <ul>
                <li>Created, Presented and Executed plan for Data pipeline</li>
                <li>Created data visualizations the help attract and retain customers</li>
                <li>Built data pipelines to automate the creation of visualizations dashboards</li>
            </ul>  
        </div>
        <p class="subtitle">Web Developer, Eastern Michigan University, 6/1/19-Present</p>
        <div class="content">
            <ul>
                <li>Develop new web pages and applications using PHP, JavaScript, Vue.js.</li>
                <li>Develop XSLT templates to be used by our CMS</li>
                <li>Maintain current web pages and applications while adhering to version control.</li>
                <li>Use SQL to display stored data on webpages.</li>
                <li>Work with a diverse team that includes other developers, designers, and SEO specialists</li>
                <li>Verify all pages meet legal accessibility requirements.</li>
            </ul>  
        </div>

        <p class="subtitle">IT Field Technician, Eastern Michigan University, 9/1/2017-6/1/19</p>
        <div class="content">
            <ul>
                <li>Provide in person desktop support for all university staff and faculty</li>
                <li>Provide over the phone support for all staff and faculty</li>
                <li>Use remote login tools to support remote employees</li>
                <li>Deployed both Windows and Macintosh systems</li>
                <li>worked within Active Directory for user accounts and privileges</li>
            </ul>  
        </div>

        <p class="title">Freelance Experience:</p>
        <p class="subtitle">Full Stack Developer, simntx.net, 6/12/2020-8/1/2020</p>
        <div class="content">
            <ul>
                <li>Build the initial version of the E-commerce website</li>
                <li>Interview and hire my own team of developers to assist me</li>
                <li>Set up dedicated production server</li>
                <li>Work with tight deadlines dealines</li>
                <li>Manage entire project and set achievable goals</li>
            </ul>  
        </div>
      </div>
    </article>
  </div>
</div>
</section>
<!------------>
   
  <div style="padding-bottom: 150px;"></div>




  </section> 
</template>

<script>
import Card from '~/components/Card'

export default {
  name: 'HomePage',
  layout: 'navbar',

  components: {
    Card
  },
  head: {
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' }
    ],
  },



}


</script>
