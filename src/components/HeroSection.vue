<template>
    <section class="hero">
        <div class="hero-image">
            <div class="box"></div>
             <div class="hero-title">
                <h1>Let's find your Pair Programmer Friends</h1>
                <h3>Get started It's totally free</h3>
                <router-link to="video">
                <button>Start Video Chat <i class="fas fa-video"></i></button>
                </router-link>
             </div>
     </div>
    </section>    
</template>

<script>
export default {
    name: "HeroSection"
}
</script>

<style lang="scss" scoped>
    .hero{
        width: 100%;
        background: url("https://images.unsplash.com/photo-1480714378408-67cf0d13bc1b?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=870&q=80");
        background-attachment: fixed;
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        height: 91vh;
    }

    .box {
        position: absolute;
        height: 91vh;
        width: 100%;
        background-color: black;
        opacity: 0.5;
    }
    .hero-title {
        position: absolute;
        z-index: 99;
        display: flex;
        flex-direction: column;
        height: 80vh;
        justify-content: center;
        align-items: center;
        text-align: center;
        width: 75%;
        margin-left: auto;
        margin-right: auto;
        left: 0;
        right: 0;     
        h1, h2, h3 {
            padding: 5px;
        }

        h1 {
            font-size: 65px;
            color: white;
            font-weight: bold;
        }

        h3 {
            font-size: 25px;
            font-weight: 500;
            color: white;
        }

        button {
            margin-top: 20px;
            padding: 15px;
            width: 14em;
            font-size: 25px;
            background-color: rgb(197, 226, 30);
            border: none;
            border-radius: 20px;
            cursor: pointer;

            &:hover {
            background-color: rgb(178, 202, 41);
            }

            a {
                text-decoration: none;
                list-style: none;
                color: black;
            }
        }
    }

    @media(max-width: 780px) {
        h1 {
            font-size: 2.5rem !important;
        }

        h3 {
            font-size: 1rem !important;
        }

        button {
            width: 12em !important;
            font-size: 1rem !important;
        }
    }
</style>