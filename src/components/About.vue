<template>
  <section class="about section">
    <div class="container">
        <img src="../assets/images/illustration-stay-productive.png" alt="illustration-stay-productive" class="img-cover">

        <div class="about-content">
            <h1 class="title-content">Stay productive, wherever you are</h1>
            <p class="text-content">
            Never let location be an issue when accessing your files. Fylo has you 
            covered for all of your file storage needs.<br><br>Securely share files 
            and folders with friends, family and colleagues for live collaboration. 
            No email attachments required.</p>
            <button class="btn-under-line">
                <span class="span">See how Fylo works</span>
                <img src="../assets/images/icon-arrow.svg" alt="icon-arrow">
            </button>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    name: "About",
    data() {
        return {}
    }
}
</script>

<style scoped>
    .about { background-color: var(--Dark-Blue-13); }

    .about .container {
        display: grid;
        grid-template-columns: repeat(1, 1fr);
        align-items: center;
        gap: 50px;
    }
    .about .container .about-content .title-content { 
        font-size: 1.5rem; 
        margin-bottom: 20px;
    }
    .about .container .about-content .text-content {
        color: #c1c1c1;
        font-size: 1.2rem;
        line-height: 1.6;
        font-weight: 400;
        margin-bottom: 15px;
    }
    .about .container .about-content .btn-under-line {
        display: flex;
        align-items: center;
        color: var(--Cyan);
        border-bottom: 2px solid var(--Cyan);
        padding-bottom: 5px;
        font-size: 1.1rem;
        gap: 10px;
        transition: .4s;
    }
    .about .container .about-content .btn-under-line:where(:hover, :focus-visible) {
        color: var(--White);
        border-bottom: 2px solid var(--White);
        transition: .4s;
    }

    /*-----------------------------------------------*\
      #MEDIA
    \*-----------------------------------------------*/

    /**
     * fit size 992px
     */
    @media screen and (min-width: 992px) {
        .about .container {
            grid-template-columns: repeat(2, 1fr);
            gap: 50px;
        }
        .about .container .about-content .title-content { 
            font-size: 3rem; 
            width: 400px;
        }
        .about .container .about-content .text-content {
            margin-bottom: 20px;
            font-size: 1.3rem;
            width: 600px;
        }
    }
</style>