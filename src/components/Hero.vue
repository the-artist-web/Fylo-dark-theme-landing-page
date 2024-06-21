<template>
  <div class="hero">
    <div class="container">
      <div class="container-in-main">
      <img src="../assets/images/illustration-intro.png" alt="illustration intro" class="img-cover">

      <div class="hero-content">
        <h1 class="title-content">All your files in one secure location, accessible anywhere.</h1>
        <p class="text-contant">
        Fylo stores all your most important files in one secure location. Access them 
        wherever you need, share and collaborate with friends family, and co-workers.</p>
        <button class="btn-primary">Get Started</button>
      </div>
    </div>
    </div>
    <img src="../assets/images/bg-curvy-desktop.svg" alt="bg-curvy-desktop" class="bg-curvy-desktop">
    <img src="../assets/images/bg-curvy-mobile.svg" alt="bg-curvy-mobile" class="bg-curvy-mobile">
  </div>
</template>

<script>
export default {
    name: "Hero",
    data() {
        return {}
    }
}
</script>

<style scoped>
  .hero {
    padding-block: 100px 80px; 
    text-align: center;
    position: relative;
  }
  .hero .container .container-in-main .hero-content .title-content { 
    font-size: 1.8rem;
    line-height: 1.8;
    margin: 50px 0 22px;
  }
  .hero .container .container-in-main .hero-content .text-contant { 
    color: #c1c1c1;
    font-weight: 600;
    font-size: 1.1rem;
    line-height: 1.6;
    max-width: 550px;
    width: 100%;
    margin: 0 auto 25px;
  }
  .btn-primary {
    background-color: var(--Blue);
    padding: 18px 60px;
    margin: 0 auto;
    border-radius: 100px;
    font-size: 1.1rem;
    font-weight: 600;
    color: var(--White);
    transition: .4s;
  }

  .btn-primary:where(:hover, :focus-visible) {
      background-color: var(--Cyan);
      transition: .4s;
  }

  /*-----------------------------------------------*\
    #BG HERO BOTTOM 
  \*-----------------------------------------------*/

  .bg-curvy-desktop {
    position: absolute;
    bottom: 0;
    right: 0;
    left: 0;
    z-index: -1;
    width: 100%;
    height: auto;
    display: none;
  }
  .bg-curvy-mobile {
    position: absolute;
    bottom: 0;
    right: 0;
    left: 0;
    z-index: -1;
    width: 100%;
    height: auto;
  }

  /*-----------------------------------------------*\
    #MEDIA
  \*-----------------------------------------------*/

  /**
   * fit size 768px
   */
  @media  screen and (min-width: 768px) {
    .hero { padding-block: 120px 80px; }

    .hero .container .container-in-main .hero-content .title-content { font-size: 2.5rem; }

    .hero .container .container-in-main .hero-content .text-contant { font-size: 1.3rem; }

    /* #BG HERO BOTTOM */
    .bg-curvy-desktop { display: block; }

    .bg-curvy-mobile { display: none; }
  }

  /**
   * fit size 992px
   */
  @media  screen and (min-width: 992px) { .hero { padding-block: 130px 80px; } }
</style>