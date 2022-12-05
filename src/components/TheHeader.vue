<template>
    <header class="bg-w">
        <div class="container">
            <img src="../../public/img/dc-logo.png" alt="">
            <ul>
                <li v-for="element in headerMenuList">
                    <a :href="element.url">{{ element.text.toUpperCase() }}</a>
                </li>
            </ul>
        </div>
    </header>
</template>



<script>
export default {
    data() {
        return {
            headerMenuList: [
                {
                    text: 'characters',
                    url: '#'

                },
                {
                    text: 'comics',
                    url: '#'

                },
                {
                    text: 'movies',
                    url: '#'

                },
                {
                    text: 'tv',
                    url: '#'

                },
                {
                    text: 'games',
                    url: '#'

                },
                {
                    text: 'collectibles',
                    url: '#'

                },
                {
                    text: 'videos',
                    url: '#'

                },
                {
                    text: 'fans',
                    url: '#'

                },
                {
                    text: 'news',
                    url: '#'

                },
                {
                    text: 'shop',
                    url: '#'

                },
            ]
        };
    },
}
</script>



<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;

header {
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    z-index: 10;

    .container {
        display: flex;
        justify-content: space-between;
        padding: $s-3 0;

        img {
            width: $s-3 * 5;
            display: block;
            aspect-ratio: 1/1;
        }

        ul {
            display: flex;
            align-items: center;
            list-style: none;

            li {
                height: 100%;
                display: flex;
                align-items: center;
                position: relative;

                a {
                    color: $dark;
                    text-decoration: none;
                    padding: $s-4;
                    font-weight: bold;
                    font-size: .7rem;
                }

                &::after {
                    background-color: transparent;
                    right: 50%;
                    left: 50%;
                    transition: all .5s;
                }

                &:hover {
                    &::after {
                        content: '';
                        background-color: $primary;
                        position: absolute;
                        bottom: -$s-3;
                        right: 0;
                        left: 0;
                        height: $s-1;
                    }

                    a {
                        color: $primary;
                    }
                }
            }

        }
    }
}

@media screen and (max-width: 1000px) {
    header {
        .container {
            ul {
                display: none;
            }
        }
    }
}
</style>