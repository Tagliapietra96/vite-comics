<template>
    <div>
        <div class="container">
            <button>SIGN-UP NOW</button>
            <div>
                <a href="#">FOLLOW US</a>
                <div>
                    <a v-for="element in socialList" href="#">
                        <img :src="`/img/footer-${element}.png`">
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>



<script>
export default {
    data() {
        return {
            socialList: [
                'facebook',
                'twitter',
                'youtube',
                'pinterest',
                'periscope',
            ]
        }
    }
}
</script>



<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;

div {
    background-color: $secondary;

    .container {
        padding: $s-5 0;
        display: flex;
        justify-content: space-between;
        align-items: center;

        button {
            background-color: transparent;
            border: 3px solid $primary;
            color: white;
            font-size: .8rem;
            padding: $s-3;
            transition: all .5s;

            &:hover {
                background-color: rgba(250, 250, 250, .2);
                transform: scale(1.1);
            }

            &:active {
                background-color: rgba(250, 250, 250, .4);
                transform: scale(.9);

            }
        }

        div {
            display: flex;
            align-items: center;

            a {
                color: $primary;
                font-weight: bold;
                font-size: 1.2rem;
                text-decoration: none;
            }

            div {
                display: flex;
                align-items: center;
                margin-left: $s-5;

                a {
                    height: 2rem;

                    img {
                        margin: 0 $s-1;
                        height: 100%;
                        aspect-ratio: 1/1;
                    }
                }
            }
        }
    }
}
</style>