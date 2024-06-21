<template>
    <header class="header" data-header>
        <div class="container">
            <a href="#" class="logo">
                <img src="../assets/images/logo.svg" alt="logo" loading="lazy" class="img-logo">
            </a>

            <ul class="nav-list">
                <li class="nav-item"><a href="#Features" class="nav-link">Features</a></li>
                <li class="nav-item"><a href="#Team" class="nav-link">Team</a></li>
                <li class="nav-item"><a href="#Sign In" class="nav-link">Sign In</a></li>
            </ul>
        </div>
    </header>
</template>

<style scoped>
    .header {
        font-family: var(--font-family-full);
        background-color: transparent;
        height: 70px;
        width: 100%;
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        z-index: 10;
        padding-top: 5px;
        transition: .4s;
    }
    .header.active {
        background-color: var(--Dark-Blue-18);
        padding-top: 0;
        transition: .4s;
    }
    .header .container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 70px;
    }
    .header .container .logo .img-logo {
        width: 100px;
        height: auto;
    }
    .header .container .nav-list {
        display: flex;
        align-content: center;
        gap: 30px;
    }
    .header .container .nav-list .nav-item .nav-link {
        color: #c1c1c1;
        font-size: 1.1rem;
        font-weight: 400;
        transition: .4s;
    }
    .header .container .nav-list .nav-item .nav-link:where(:hover, :focus-visible) {
        color: var(--White);
        text-decoration: underline;
    }

    /*-----------------------------------------------*\
      #MEDIA
    \*-----------------------------------------------*/

    /**
     * fit size 768px
     */
    @media screen and (min-width: 768px) {
        .header { padding-top: 30px; }

        .header.active { padding-top: 0; }

        .header .container .logo .img-logo { width: 110px; }

        .header .container .nav-list { gap: 50px; }
    }
</style>

<script>
    export default {
        name: "Header",
        data() {
            return {}
        },
        methods: {
            scrollHeader() {
                const header = document.querySelector("[data-header]");
                if (window.scrollY >= 100) {
                    header.classList.add("active");
                } else {
                    header.classList.remove("active");
                }
            }
        },
        mounted() {
            window.addEventListener('scroll', this.scrollHeader);
        },
        beforeDestroy() {
            window.removeEventListener('scroll', this.scrollHeader);
        }
    };
</script>