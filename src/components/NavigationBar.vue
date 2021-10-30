<template>
<div class="transition">
    <nav class="navigation" @change="onScreenChange(e)">
        <div class="container">
        <div class="logo">
            <router-link to="/">
            <a class="logo-text">CodeSmeggle</a>
            </router-link>
        </div>
        <div class="menu-list" v-if="isDesktop">
            <router-link to="/">Home</router-link>
            <router-link to="/video">Start Video</router-link>
            <router-link to="/about">About</router-link>
        </div>
        <div class="hamburger-menu" v-else>
            <i class="fas fa-bars" @click="toggleShowMenuNavbar" v-if="!isShowMenuNavbar"></i>
            <i class="fas fa-times" @click="toggleShowMenuNavbar" v-else></i>
            </div>
        </div>
    </nav>

    <div class="menu-show" v-if="isShowMenuNavbar">
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Video Chat</a></li>
            <li><a href="#">About</a></li>
        </ul>
    </div>

</div>

</template>

<script>
export default {
    name: "NavigationBar",
    data() {
        return {
            screenResolution: window.innerWidth,
            isDesktop: true,
            isShowMenuNavbar: false
        }
    },


    created() {
        window.addEventListener("resize", this.onScreenChange);
        this.isDesktop = this.screenResolution < 780 ? false : true;
    },
    destroyed() {
        window.removeEventListener("resize", this.onScreenChange);
    },
    methods: {
        onScreenChange(e) {
          this.screenResolution = e.target.innerWidth;
          this.isDesktop = this.screenResolution < 780 ? false : true;
          if(this.isDesktop) {
              this.isShowMenuNavbar = false
          }
          console.log(this.screenResolution, this.isDesktop)
    },
        toggleShowMenuNavbar() {
            this.isShowMenuNavbar = !this.isShowMenuNavbar
        }
}

}
</script>

<style scoped lang="scss">

    .navigation {
        height: 60px;
        display: flex;
        align-items: center;
        box-shadow: 0 2px 2px 0 rgba(0, 0, 0, 0.2), 0 2px 5px 0 rgba(0, 0, 0, 0.19);
        background-color: rgb(197, 226, 30);
        color: black;
        .logo-text {
            font-weight: bold;
            font-size: 25px;
            list-style: none;
            color: black;
        }

        a {
            text-decoration: none;
        }
        
        .hamburger-menu {
            display: block;
            cursor: pointer;
            font-size: 25px;
        }

        .container {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            align-items: center;
            width: 75%;
            margin: 0 auto;
        }

        .menu-list {
            a {
                list-style: none;
                text-decoration: none;
                color: black;
                margin-right: 25px;
                font-weight: 700;
            }
        }
    }

         .menu-show {
            height: 55vh;
            width: 100%;
            background-color: rgb(197, 226, 30);
            display: flex;
            position: absolute;
            justify-content: center;
            font-size: 25px;
            border-top: 1px solid black;
            position: absolute;
            z-index: 999;
            ul {
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;

                li {
                     list-style: none;
                     text-decoration: none;
                     font-style: none;
                     margin-bottom: 30px;

                     a {
                         text-decoration: none;
                         font-style: none;
                         color: black;
                     }
                }
            }
        }

    @media (max-width: 780px) {
        .container {
            width: 100% !important;
            justify-content: space-around !important;
        }
    }
    
</style>