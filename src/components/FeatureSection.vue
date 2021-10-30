<template>
    <div class="features">
        <div class="container">
        <div class="card">
            <img src="" alt="">
            <h1>Discuss and Ask question</h1>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Atque, dolor corrupti. Vel eos dolore, ea ducimus fugit corrupti sit fuga dolor, rerum dolorum animi incidunt aspernatur id assumenda. Possimus, repellat.</p>
        </div>
         <div class="card">
            <img src="" alt="">
            <h1>Meet new people</h1>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Atque, dolor corrupti. Vel eos dolore, ea ducimus fugit corrupti sit fuga dolor, rerum dolorum animi incidunt aspernatur id assumenda. Possimus, repellat.</p>
        </div>
         <div class="card">
            <img src="" alt="">
            <h1>no login required</h1>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Atque, dolor corrupti. Vel eos dolore, ea ducimus fugit corrupti sit fuga dolor, rerum dolorum animi incidunt aspernatur id assumenda. Possimus, repellat.</p>
        </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "FeatureSection",
}
</script>

<style lang="scss" scoped>
    .features {
        width: 100%;
        background-color: rgb(197, 226, 30);
        color: white;
       
       .container {
            width: 75%;
            margin: 0 auto;
            display: flex;
       }

        .card {
            background-color: black;
            padding: 1rem;
            margin: 10px;
            margin-top: 80px;
            margin-bottom: 80px;
            border-radius: 20px;
              
           }

           h1 {
               margin-bottom: 10px;
               text-align: center;
           }
           p {
               text-align: justify;
           }
    }

    @media(max-width: 990px) {
        .container {
            flex-direction: column !important;
            width: 90% !important;
            .card {
                margin-top: 20px;
                margin-bottom: 0px;
                  &:first-child {
                    margin-top: 45px;
                }

                &:last-child {
                    margin-bottom: 40px;
                }
            }
        }
    }
</style>