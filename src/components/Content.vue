<template>
    <section class="bg-d">
        <img class="jumbo" src="/img/jumbotron.jpg">
        <div class="container">
            <h1>CURRENT SERIRES</h1>
            <div class="row">
                <div class="card" v-for="element in comicsList">
                    <img :src="element.thumb" alt="">
                    <h2>{{element.price}}</h2>
                    <h3>{{element.type.toUpperCase()}}</h3>
                    <h4>{{element.series}}</h4>
                </div>
            </div>
            <div class="btn-container">
                <button>LOAD MORE</button>
            </div>
        </div>
    </section>
</template>



<script>
export default {
    props: {
        comicsList: Array,
    }
}
</script>


<style scoped lang="scss">
@use '../styles/partials/variables' as *;

section {
    img.jumbo {
        display: block;
        width: 100%;
        height: 700px;
        object-position: center;
        object-fit: cover;
    }

    .container {
        color: white;
        position: relative;
        top: -30px;
        h1 {
            background-color: $primary;
            display: inline-block;
            padding: $s-3;
            margin-bottom: $s-5;
        }

        .row {
            display: flex;
            flex-wrap: wrap;
            margin: $s-5 (-$s-2);

            .card {
            
                padding: $s-4 $s-2;
                width: calc(100% / 6);
                position: relative;

                img {
                    display: block;
                    width: 100%;
                }
                h4{
                    padding-top: $s-3;
                }
                h2, h3{
                    background-color: $primary;
                    position: absolute;
                    opacity: 0;
                    padding: $s-1;
                    transition: opacity .5s;
                }
                h2{
                    right: $s-2;
                    top: $s-4 + 31px;
                }
                h3{
                    left: $s-2;
                    right: $s-2;
                    top: $s-4;
                }

                &:hover{
                    h2, h3{
                        opacity: 1;
                    }
                }
            }
        }

        .btn-container{
            text-align: center;
            padding-top: $s-5;
            button{
                font-size: 1rem;
                background-color: $primary;
                border: transparent;
                color: white;
                padding: $s-3 $s-4;
                font-weight: bold;
                transition: all .5s;
                &:hover{
                    transform: scale(1.1);
                }
                &:active{
                    transform: scale(.9);   
                }
            }
        }
    }
}
</style>