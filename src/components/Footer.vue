<template>
    <footer class="footer">
        <div class="container">
            <a href="#" class="logo">
                <img src="../assets/images/logo.svg" alt="logo" loading="lazy" class="img-logo">
            </a>

            <div class="footer-list">
                <div class="footer-top">
                    <div class="footer-box">
                        <img src="../assets/images/icon-location.svg" alt="icon-location">
                        <p class="footer-text">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod 
                            tempor incididunt ut labore et dolore magna aliqua
                        </p>
                    </div>

                    <div class="contact-list">
                        <a href="#" class="contact-text">
                            <img src="../assets/images/icon-phone.svg" alt="icon-phone">
                            <span class="span">+1-543-123-4567</span>
                        </a>
                        <a href="#" class="contact-text">
                            <img src="../assets/images/icon-email.svg" alt="icon-email">
                            <span class="span">example@fylo.com</span>
                        </a>
                    </div>
                </div>

                <div class="footer-bottom">
                    <ul class="links-list">
                        <li class="link-items">
                            <a href="#" class="link-footer">About Us</a>
                            <a href="#" class="link-footer">Jobs</a>
                            <a href="#" class="link-footer">Press</a>
                            <a href="#" class="link-footer">Blog</a>
                        </li>
                        <li class="link-items">
                            <a href="#" class="link-footer">Contact Us</a>
                            <a href="#" class="link-footer">Terms</a>
                            <a href="#" class="link-footer">Privacy</a>
                        </li>
                    </ul>

                    <div class="social-list">
                        <a href="#" class="social-link">
                            <i class="fa-brands fa-facebook-f"></i>
                        </a>
                        <a href="#" class="social-link">
                            <i class="fa-brands fa-twitter"></i>
                        </a>
                        <a href="#" class="social-link">
                            <i class="fa-brands fa-instagram"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: "Footer",
    data() {
        return {}
    }
}
</script>

<style scoped>
    .footer {
        background-color: var(--Dark-Blue-9);
        padding: 200px 0 40px;
    }
    .footer .container {
        display: flex;
        flex-direction: column;
        gap: 40px;
    }
    .footer .container .footer-list {
        display: flex;
        flex-direction: column;
        gap: 50px;
    }
    .footer .container .footer-list .footer-top {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }
    .footer .container .footer-list .footer-top .footer-box {
        display: flex;
        align-items: start;
        gap: 15px;
    }
    .footer .container .footer-list .footer-top .footer-box .footer-text {
        color: #c1c1c1;
        font-size: 1.2rem;
        line-height: 1.6;
        font-weight: 400;
        width: 100%;
        max-width: 350px;
    }
    .footer .container .footer-list .footer-top .contact-list {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }
    .footer .container .footer-list .footer-top .contact-list .contact-text {
        display: flex;
        align-items: center;
        gap: 15px;
    }
    .footer .container .footer-list .footer-top .contact-list .contact-text .span {
        font-size: 1.2rem;
        line-height: 1.6;
        font-weight: 400;
    }
    .footer .container .footer-list .footer-bottom {
        display: flex;
        flex-direction: column;
        gap: 40px;
    }
    .footer .container .footer-list .footer-bottom .links-list {
        display: flex;
        flex-direction: column;
        gap: 35px;
    }
    .footer .container .footer-list .footer-bottom .links-list .link-items {
        display: flex;
        flex-direction: column;
        gap: 10px;
    }
    .footer .container .footer-list .footer-bottom .links-list .link-items .link-footer {
        color: #c1c1c1;
        font-size: 1.2rem;
        line-height: 1.6;
        font-weight: 400;
        transition: .4s;
    }
    .footer .container .footer-list .footer-bottom .links-list .link-items .link-footer:hover {
        color: var(--White);
        transition: .4s;
    }
    .footer .container .footer-list .footer-bottom .social-list {
        display: flex;
        align-items: center;
        margin: 0 auto;
        gap: 15px;
    }
    .footer .container .footer-list .footer-bottom .social-list .social-link {
        display: flex;
        align-items: center;
        justify-content: center;
        height: 35px;
        width: 35px;
        font-size: 1rem;
        border: 2px solid var(--White);
        border-radius: 100px;
        transition: .4s;
    }
    .footer .container .footer-list .footer-bottom .social-list .social-link:hover {
        border: 2px solid var(--Blue);
        color: var(--Blue);
        transition: .4s;
    }

    /*-----------------------------------------------*\
      #MEDIA
    \*-----------------------------------------------*/

    /**
     * fit size 768px
     */
    @media screen and (min-width: 768px) {
        .footer .container .footer-list { 
            flex-direction: row; 
            align-items: start;
            justify-content: space-between;
        }
        .footer .container .footer-list .footer-top { flex-direction: column; }

        .footer .container .footer-list .footer-bottom { flex-direction: column; }

        .footer .container .footer-list .footer-bottom .links-list { flex-direction: row; }

        .footer .container .footer-list .footer-bottom .social-list { margin: 0 0; }
    }

    /**
     * fit size 992px
     */
    @media screen and (min-width: 992px) {
        .footer { padding: 200px 0 80px; }

        .footer .container .footer-list { 
            flex-direction: row; 
            align-items: start;
            justify-content: space-between;
            gap: 80px;
        }
        .footer .container .footer-list .footer-top {
            flex-direction: row;
            gap: 120px;
        }
        .footer .container .footer-list .footer-bottom {
            display: flex;
            flex-direction: row;
            align-items: start;
            gap: 120px;
        }
        .footer .container .footer-list .footer-bottom .links-list { 
            flex-direction: row; 
            gap: 110px;
        }

        .footer .container .footer-list .footer-bottom .social-list { margin: 0 0; }
    }
</style>