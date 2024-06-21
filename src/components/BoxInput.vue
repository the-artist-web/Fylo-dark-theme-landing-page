<template>
    <section class="box-form " id="Sign In">
        <div class="container">
            <div class="box-content">
                <h1 class="title-box">Get early access today</h1>
                <p class="text-box">
                It only takes a minute to sign up and our free starter tier is extremely generous. 
                If you have any questions, our support team would be happy to help you.</p>
                <div class="form">
                    <div class="input-box">
                        <input type="text" placeholder="email@example.com" class="email" data-email>
                        <span class="error" data-error>please enter a valid email address</span>
                    </div>
                    <button @click="emailValue()" class="btn-primary">Get Started For Free</button>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "BoxInput",
    data() {
        return {}
    },
    methods: {
        emailValue: function() {
            const email = document.querySelector("[data-email]");
            const error = document.querySelector("[data-error]");

            const emailRegex = /^([a-z\d\.-]+)@([a-z\d-]+)\.([a-z]{2,3})(\.[a-z]{2,3})?$/;
            
            if (
                email.value.trim().toLowerCase() === "" 
                || 
                email.value.trim().toLowerCase() !== emailRegex
            ) {
                error.classList.add("active");
            } else {
                error.classList.remove("active");
            };
        }
    }
}
</script>

<style scoped>
    .box-form { background-color: var(--Dark-Blue-13); }

    .box-form .container .box-content {
        background-color: var(--Dark-Blue-15);
        box-shadow: 10px 10px 20px -10px black;
        padding: 50px 25px 25px;
        text-align: center;
        border-radius: 8px;
        position: relative;
        max-width: 900px;
        margin: 0 auto;
        width: 100%;
        top: 120px;
    }
    .box-form .container .box-content .title-box {
        font-size: 1.5rem;
        margin-bottom: 20px;
    }
    .box-form .container .box-content .text-box {
        color: #c1c1c1;
        font-size: 1.2rem;
        line-height: 1.6;
        font-weight: 400;
        margin-bottom: 25px;
    }
    .box-form .container .box-content .form {
        margin: 0 auto;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 30px;
    }
    .box-form .container .box-content .form .input-box { 
        position: relative;
        width: 100%; 
    }
    .box-form .container .box-content .form .input-box .email {
        background-color: var(--White);
        border-radius: 100px;
        padding: 18px 30px;
        font-size: 1.1rem;
        height: 55px;
    }
    .box-form .container .box-content .form .input-box .error {
        color: var(--Light-Red);
        text-align: start;
        font-size: 13px;
        display: none;
        position: absolute;
        bottom: -20px;
    }
    .box-form .container .box-content .form .input-box .error.active { display: block; }

    .box-form .container .box-content .form .btn-primary {
        text-wrap: nowrap;
        background-color: var(--Blue);
        padding: 18px 30px;
        border-radius: 100px;
        font-size: 1.1rem;
        height: 55px;
        font-weight: 600;
        color: var(--White);
        width: 100%;
        transition: .4s;
    }
    .box-form .container .box-content .form .btn-primary:where(:hover, :focus-visible) {
        background-color: var(--Cyan);
        transition: .4s;
    }

    /*-----------------------------------------------*\
      #MEDIA
    \*-----------------------------------------------*/

    /**
     * fit size 768px
     */
    @media screen and (min-width: 768px) {
        .box-form .container .box-content { padding: 60px 80px 40px; }

        .box-form .container .box-content .title-box { font-size: 2.5rem; }

        .box-form .container .box-content .text-box { margin-bottom: 35px; }

        .box-form .container .box-content .form {
            width: 100%;
            flex-direction: row;
            gap: 25px;
        }
        .box-form .container .box-content .form .btn-primary { max-width: max-content; }
    }
</style>