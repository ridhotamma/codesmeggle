<template>
    <div class="footer">
        <div class="container">
            <ul>
                <li><i class="fab fa-instagram"></i></li>
                <li><i class="fab fa-github"></i></li>
                <li><i class="fab fa-facebook"></i></li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: "FooterSection"
}
</script>

<style lang="scss" scoped>
    .footer {
        background-color: black;
        color: white;
        padding: 50px;

        .container {
            width: 75%;
            margin: 0 auto;
            display: flex;
            justify-content: center;
            align-content: center;

            ul {
                display: flex;
                .fab {
                    margin-right: 5px;
                    font-size: 35px;
                }
                li {
                    list-style: none;
                    text-decoration: none;
                    margin-right: 10px;
                }
            }
        }
    }
</style>