<template>
  <section class="grid-list section" id="Features">
    <div class="container">
        <div class="grid-box">
            <img src="../assets/images/icon-access-anywhere.svg" alt="icon-access-anywhere" loading="lazy"class="img-box">
            <div class="grid-box-content">
                <h2 class="title-content">Access your files, anywhere</h2>
                <p class="text-content">
                The ability to use a smartphone, tablet, or computer to access 
                your account means your files follow you everywhere.</p>
            </div>
        </div>
        
        <div class="grid-box">
            <img src="../assets/images/icon-security.svg" alt="icon-security" loading="lazy"class="img-box">
            <div class="grid-box-content">
                <h2 class="title-content">Security you can trust</h2>
                <p class="text-content">
                2-factor authentication and user-controlled encryption are just a couple of the security 
                features we allow to help secure your files.</p>
            </div>
        </div>
        
        <div class="grid-box">
            <img src="../assets/images/icon-collaboration.svg" alt="icon-collaboration" loading="lazy"class="img-box">
            <div class="grid-box-content">
                <h2 class="title-content">Real-time collaboration</h2>
                <p class="text-content">
                Securely share files and folders with friends, family and colleagues for live collaboration. 
                No email attachments required.</p>
            </div>
        </div>
        
        <div class="grid-box">
            <img src="../assets/images/icon-any-file.svg" alt="icon-any-file" loading="lazy"class="img-box">
            <div class="grid-box-content">
                <h2 class="title-content">Store any type of file</h2>
                <p class="text-content">
                Whether you're sharing holidays photos or work documents, Fylo has you covered allowing for all 
                file types to be securely stored and shared.</p>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    name: "GridList",
    data() {
        return {}
    }
}
</script>

<style scoped>
    .grid-list { background-color: var(--Dark-Blue-13); }

    .grid-list .container {
        display: grid;
        grid-template-columns: repeat(1, 1fr);
        align-items: start;
        gap: 100px;
        max-width: 1000px;
        width: 100%;
        margin: 0 auto;
    }
    .grid-list .container .grid-box .img-box { margin: 0 auto 30px; }

    .grid-list .container .grid-box .grid-box-content { text-align: center; }

    .grid-list .container .grid-box .grid-box-content .title-content { 
        font-size: 1.5rem; 
        margin-bottom: 15px;
    }

    .grid-list .container .grid-box .grid-box-content .text-content {
        font-size: 1.2rem;
        font-weight: 400;
        color: #c1c1c1;
        line-height: 1.6;
    }

    /*-----------------------------------------------*\
      #MEDIA
    \*-----------------------------------------------*/

    /**
     * fit size 768px
     */
    @media screen and (min-width: 768px) {
        .grid-list .container {
            grid-template-columns: repeat(2, 1fr);
            gap: 150px;
        }
    }
</style>