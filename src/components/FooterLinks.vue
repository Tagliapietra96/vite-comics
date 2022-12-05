<template>
    <div>
        <div class="container">
            <div>
                <div class="column">
                    <ul class="dc-comics">
                        <li>
                            <h3>DC COMICS</h3>
                        </li>
                        <li v-for="element in dcComicsList">
                            <a :href="element.url">{{ element.text }}</a>
                        </li>
                    </ul>

                    <ul class="shop">
                        <li>
                            <h3>SHOP</h3>
                        </li>
                        <li v-for="element in shopList">
                            <a :href="element.url">{{ element.text }}</a>
                        </li>
                    </ul>
                </div>

                <ul class="dcList">
                    <li>
                        <h3>DC</h3>
                    </li>
                    <li v-for="element in dcList">
                        <a :href="element.url">{{ element.text }}</a>
                    </li>
                </ul>

                <ul class="sites">
                    <li>
                        <h3>SITES</h3>
                    </li>
                    <li v-for="element in sitesList">
                        <a :href="element.url">{{ element.text }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>



<script>
export default {
    data() {
        return {
            dcComicsList: [
                {
                    text: 'Characters',
                    url: '#'

                },
                {
                    text: 'Comics',
                    url: '#'

                },
                {
                    text: 'Movies',
                    url: '#'

                },
                {
                    text: 'TV',
                    url: '#'

                },
                {
                    text: 'Games',
                    url: '#'

                },
                {
                    text: 'Videos',
                    url: '#'

                },
                {
                    text: 'News',
                    url: '#'

                },
            ],
            shopList: [
                {
                    text: 'Shop DC',
                    url: '#'

                },
                {
                    text: 'Shop DC Collections',
                    url: '#'

                },
            ],
            dcList: [
                {
                    text: 'Terms Of Use',
                    url: '#'

                },
                {
                    text: 'Privacy Policy (New)',
                    url: '#'

                },
                {
                    text: 'Ad Choices',
                    url: '#'

                },
                {
                    text: 'Advertising',
                    url: '#'

                },
                {
                    text: 'Jobs',
                    url: '#'

                },
                {
                    text: 'Subscriptions',
                    url: '#'

                },
                {
                    text: 'Talent Workspace',
                    url: '#'

                },
                {
                    text: 'CPSC Certnificates',
                    url: '#'

                },
                {
                    text: 'Ratings',
                    url: '#'

                },
                {
                    text: 'Shop Help',
                    url: '#'

                },
                {
                    text: 'Contact US',
                    url: '#'

                },
            ],
            sitesList: [
                {
                    text: 'DC',
                    url: '#'

                },
                {
                    text: 'MAD Magazine',
                    url: '#'

                },
                {
                    text: 'DC Kids',
                    url: '#'

                },
                {
                    text: 'DC Universe',
                    url: '#'

                },
                {
                    text: 'DC Power Visa',
                    url: '#'

                },
            ]
        }
    }
}
</script>



<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;

div {
    .container {
        padding: $s-5 0;
        background-image: url('/img/dc-logo-bg.png');
        background-repeat: no-repeat;
        background-position: right;

        div {
            display: flex;
            gap: $s-5;
            .column {
                display: flex;
                flex-direction: column;
                gap: $s-4;
            }

            ul {
                list-style: none;
                margin-right: $s-3;
                h3 {
                    color: white;
                    margin-bottom: $s-4;
                }

                a {
                    color: #797979;
                    text-decoration: none;
                    margin-bottom: $s-1;
                    display: block;
                    font-size: .8rem;
                    transition: all .5s;
                    &:hover{
                        color: white;
                        text-decoration: underline;
                        transform: scale(1.1);
                    }
                }
            }
        }
    }
}
</style>