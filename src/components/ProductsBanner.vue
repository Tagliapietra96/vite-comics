<template>
    <section class="bg-1">
        <div class="container">
            <div v-for="element in articlesList" :style="`width: ${100 / articlesList.length}%`">
                <img :src="`/img/${element.img}`" alt="">
                <h5>{{ element.title.toUpperCase() }}</h5>
            </div>
        </div>
    </section>
</template>



<script>
export default {
    data() {
        return {
            articlesList: [
                {
                    img: 'buy-comics-digital-comics.png',
                    title: 'digital comics',
                },
                {
                    img: 'buy-comics-merchandise.png',
                    title: 'dc merchandise',
                },
                {
                    img: 'buy-comics-subscriptions.png',
                    title: 'subscription',
                },
                {
                    img: 'buy-comics-shop-locator.png',
                    title: 'comic shop locator',
                },
                {
                    img: 'buy-dc-power-visa.svg',
                    title: 'dc power visa',
                },
            ],
        }
    },
}
</script>



<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;

section {
    .container {
        padding: $s-5 * 2;
        display: flex;

        div {
            display: flex;
            align-items: center;
            color: white;

            img {
                height: $s-5 * 2;
            }

            h5 {
                padding-left: $s-3;
            }

            &:last-of-type {
                img {
                    height: $s-5 * 1.5;
                }
            }
        }
    }
}

@media screen and (max-width: 1000px) {
    section {
        .container {

            div {
                justify-content: center;

                h5 {
                    display: none;
                }
            }
        }
    }
}
</style>