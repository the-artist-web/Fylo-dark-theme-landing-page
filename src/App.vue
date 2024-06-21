<template>
  <Header />

  <main>
    <article>

      <Hero />
      <GridList />
      <About />
      <Custom />
      <BoxInput />
      
    </article>
  </main>

  <Footer />
</template>

<script>
import Header from '@/components/Header.vue'
import Hero from '@/components/Hero.vue'
import GridList from '@/components/GridList.vue'
import About from '@/components/About.vue'
import Custom from '@/components/Custom.vue'
import BoxInput from '@/components/BoxInput.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    GridList,
    About,
    Custom,
    BoxInput,
    Footer
  }
}
</script>

<style>
  #app {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: auto;
  }
</style>
