<template>
    <section class="custom-list section" id="Team">
        <div class="container">
            <img src="../assets/images/bg-quotes.png" alt="bg-quotes" loading="lazy" class="bg-quotes">
            <div class="custom-box">
                <p class="text-content">
                Fylo has improved our team productivity by an order of magnitude. Since making 
                the switch our team has become a well-oiled collaboration machine.</p>
                <div class="profile-list">
                    <img src="../assets/images/profile-1.jpg" alt="profile-1" class="avatar">
                    <div class="profile-content">
                        <h3 class="title-profile">Satish Patel</h3>
                        <p class="text-profile">Founder & CEO, Huddle</p>
                    </div>
                </div>
            </div>

            <div class="custom-box">
                <p class="text-content">
                Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has 
                become a well-oiled collaboration machine.</p>
                <div class="profile-list">
                    <img src="../assets/images/profile-2.jpg" alt="profile-1" class="avatar">
                    <div class="profile-content">
                        <h3 class="title-profile">Bruce McKenzie</h3>
                        <p class="text-profile">Founder & CEO, Huddle</p>
                    </div>
                </div>
            </div>

            <div class="custom-box">
                <p class="text-content">
                Fylo has improved our team productivity by an order of magnitude. Since making the switch our team has 
                become a well-oiled collaboration machine.</p>
                <div class="profile-list">
                    <img src="../assets/images/profile-3.jpg" alt="profile-1" class="avatar">
                    <div class="profile-content">
                        <h3 class="title-profile">Iva Boyd</h3>
                        <p class="text-profile">Founder & CEO, Huddle</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "Custom",
    data() {
        return {}
    }
}
</script>

<style scoped>
    .custom-list { 
        background-color: var(--Dark-Blue-13); 
        padding-inline: 20px;
        position: relative;
    }
    .custom-list .container {
        display: grid;
        grid-template-columns: repeat(1, 1fr);
        gap: 40px;
    }
    .custom-list .container .bg-quotes {
        position: absolute;
        top: 55px;
        left: 40px;
        width: 30px;
        z-index: 1;
    }
    .custom-list .container .custom-box {
        box-shadow: 10px 10px var(--Dark-Blue-15);
        background-color: var(--Dark-Blue-18);
        padding: 50px 25px 25px;
        border-radius: 8px;
        position: relative;
        z-index: 2;
    }
    .custom-list .container .custom-box .text-content {
        color: #c1c1c1;
        font-size: 1.2rem;
        line-height: 1.6;
        font-weight: 400;
        margin-bottom: 20px;
    }
    .custom-list .container .custom-box .profile-list {
        display: flex;
        align-items: center;
        gap: 10px;
    }
    .custom-list .container .custom-box .profile-list .avatar {
        border-radius: 100px;
        width: 40px;
        height: 40px;
    }
    .custom-list .container .custom-box .profile-list .profile-content {
        display: grid;
        gap: 4px;
    }
    .custom-list .container .custom-box .profile-list .profile-content .title-profile {
        font-size: 1.1rem;
        font-weight: 500;
    }
    .custom-list .container .custom-box .profile-list .profile-content .text-profile {
        color: #c1c1c1;
        font-size: 1rem;
        font-weight: 500;
    }

    /*-----------------------------------------------*\
      #MEDIA
    \*-----------------------------------------------*/

    /**
     * fit size 992px
     */
    @media screen and (min-width: 992px) {
        .custom-list { padding-inline: 0; }

        .custom-list .container { grid-template-columns: repeat(3, 1fr); }

        .custom-list .container .bg-quotes {
            top: 38px;
            left: 40px;
            width: 70px;
        }
    }
</style>