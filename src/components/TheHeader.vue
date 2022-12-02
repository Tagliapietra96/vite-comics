<template>
    <header class="bg-w">
        <div class="container">
            <img src="../../public/img/dc-logo.png" alt="">
            <ul>
                <li>
                    <a href="#">CHARACTERS</a>
                </li>
                <li>
                    <a href="#">COMICS</a>
                </li>
                <li>
                    <a href="#">MOVIES</a>
                </li>
                <li>
                    <a href="#">TV</a>
                </li>
                <li>
                    <a href="#">GAMES</a>
                </li>
                <li>
                    <a href="#">COLLECTIBLES</a>
                </li>
                <li>
                    <a href="#">VIDEOS</a>
                </li>
                <li>
                    <a href="#">FANS</a>
                </li>
                <li>
                    <a href="#">NEWS</a>
                </li>
                <li>
                    <a href="#">SHOP</a>
                </li>
            </ul>
        </div>
    </header>
</template>



<script>
export default {

}
</script>



<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;

header {
    position: fixed;
    top: 0;
    right: 0;
    left: 0;

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
                    padding: $s-2;
                    font-weight: bold;
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
                        bottom: 0;
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

</style>