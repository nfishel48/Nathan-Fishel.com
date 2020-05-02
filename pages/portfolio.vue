<template>
    <section>
        <h1 class="main-text">View some of my work</h1>

        <nav class="level">
        <div class="level-item has-text-centered">
            <div class="box">
                 <figure class="image is-64x64">
                <img src="~/assets/css/me.png" alt="Image">
            </figure>
            <p class="heading">Tweets</p>
            <p class="title">3,456</p>
            </div>
        </div>
        <div class="level-item has-text-centered">
            <div class="box">
            <p class="heading">Following</p>
            <p class="title">123</p>
            </div>
        </div>
        <div class="level-item has-text-centered">
            <div class="box">
            <p class="heading">Followers</p>
            <p class="title">456K</p>
            </div>
        </div>
        <div class="level-item has-text-centered">
            <div class="box">
            <p class="heading">Likes</p>
            <p class="title">789</p>
            </div>
        </div>
        </nav>
    </section>
</template>
<script>
export default {
    layout: 'navbar',

}
</script>