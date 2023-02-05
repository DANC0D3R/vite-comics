<script>
export default {
    name: 'AppFooter',
    data() {
            return {
                blueMenuContent: [
                    {
                        img: 'buy-comics-digital-comics.png',
                        title: 'digital comics',
                        link: '#',
                    },
                    {
                        img: 'buy-comics-merchandise.png',
                        title: 'dc merchandise',
                        link: '#',
                    },
                    {
                        img: 'buy-comics-subscriptions.png',
                        title: 'subscription',
                        link: '#',
                    },
                    {
                        img: 'buy-comics-shop-locator.png',
                        title: 'comic shop locator',
                        link: '#',
                    },
                    {
                        img: 'buy-dc-power-visa.svg',
                        title: 'dc power visa',
                        link: '#',
                    },
                ],
            };
        },
        methods: {
            getImgPath(img) {
                return new URL(`../assets/img/${img}`, import.meta.url).href;
            },
        }
}
</script>

<template>
        <footer>
            <!-- Blu Menu -->
            <div class="blue-menu">
                <div class="container">
                    <ul>
                        <li v-for="item in blueMenuContent">
                            <a :href="item.link">
                                <img :src="getImgPath(item.img)" :alt="item.title">
                                <span>{{item.title}}</span>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
            <!-- Link Utili -->
            <div class="jumbo-bg">
                <div class="container">
                    <!-- Parte Sinistra -->
                    <div class="d-flex">
                        <div class="col">
                            <h3>DC Comics</h3>
                            <ul>
                                <li><a href="#">Characters</a></li>
                                <li><a href="#">Comics</a></li>
                                <li><a href="#">Movies</a></li>
                                <li><a href="#">TV</a></li>
                                <li><a href="#">Games</a></li>
                                <li><a href="#">Videos</a></li>
                                <li><a href="#">News</a></li>
                            </ul>
                            <h3>Shop</h3>
                            <ul>
                                <li><a href="#">Shop DC</a></li>
                                <li><a href="#">Shop DC Collectibles</a></li>
                            </ul>
                        </div>
                        <div class="col">
                            <h3>DC</h3>
                            <ul>
                                <li><a href="#">Terms of Use</a></li>
                                <li><a href="#">Privacy policy (New)</a></li>
                                <li><a href="#">Ad Choices</a></li>
                                <li><a href="#">Advertising</a></li>
                                <li><a href="#">Jobs</a></li>
                                <li><a href="#">Subcriptions</a></li>
                                <li><a href="#">Talent Workshops</a></li>
                                <li><a href="#">CPSC Certificates</a></li>
                                <li><a href="#">Ratings</a></li>
                                <li><a href="#">Shop Help</a></li>
                                <li><a href="#">Contact Us</a></li>
                            </ul>
                        </div>
                        <div class="col">
                            <h3>Sites</h3>
                            <ul>
                                <li><a href="#">DC</a></li>
                                <li><a href="#">MAD Magazine</a></li>
                                <li><a href="#">DC Kids</a></li>
                                <li><a href="#">DC Universe</a></li>
                                <li><a href="#">DC Power Visa</a></li>
                            </ul>
                        </div>
                    </div>
                    <!-- Parte Destra -->
                    <div>
                        <figure>
                            <img src="../assets/img/dc-logo-bg.png" alt="DC">
                        </figure>
                    </div>
                </div>
            </div>
            <!-- Social -->
            <div class="gray-bg">
                <div class="container">
                    <button>SIGN-UP NOW!</button>

                    <div>
                        <a href="#">FOLLOW US</a>
                        <ul>
                            <li><img src="../assets/img/footer-facebook.png" alt="Facebook"></li>
                            <li><img src="../assets/img/footer-twitter.png" alt="Twitter"></li>
                            <li><img src="../assets/img/footer-youtube.png" alt="Youtube"></li>
                            <li><img src="../assets/img/footer-pinterest.png" alt="Pinterest"></li>
                            <li><img src="../assets/img/footer-periscope.png" alt="Periscope"></li>
                        </ul>
                    </div>
                </div>
            </div>
        </footer>
</template>

<!-- Stile -->
<style lang="scss" scoped>
    @use '../assets/scss/variables' as *;
    footer{
        // Blu Menu
        .blue-menu{
        padding: 3rem;

        background-color: var(--dc-blue);
        ul{
            display: flex;
            justify-content: space-around;
            
            list-style: none;
            li a{
                display: flex;
                align-items: center;

                text-transform: uppercase;
                text-decoration: none;

                color: #FFFFFF; 
                img{
                    max-width: 65px;
                    height: 60px;
                    
                    margin-right: 1rem;
                }
            }
        }
    }
        // Link Utili
        .jumbo-bg{
            height: 300px;

            background-image: url(../assets/img/footer-bg.jpg);
            background-size: cover;
            background-repeat: no-repeat;

            color: #FFFFFF;
            .container{
                display: flex;
                justify-content: space-between;

                height: 100%;
                .col {
                    padding: 40px 20px;
                    h3{
                        margin-bottom: 5px;

                        text-transform: uppercase;
                    }
                    ul{
                        margin-bottom: 10px;

                        list-style-type: none;
                        li a{
                            font-size: 12px;

                            color: #808080;

                            text-decoration: none;
                        }
                    }
                }
                figure{
                    width: 450px;
                    height: 100%;

                    overflow: hidden;
                    img{
                        transform: translateY(-17%);

                        width: 100%;
                        height: auto;
                    }
                }
            }
        }
        // Social
        .gray-bg{
            padding: 30px 0;

            background-color: #3C3C3C;
            .container{
                display: flex;
                justify-content: space-between;
                align-items: center;
                button{
                    padding: 10px;

                    font-size: 20px;

                    border: 3px solid var(--dc-blue);

                    color: #FFFFFF;
                    background-color: rgba(rgb(0, 0, 0), 0);
                    cursor: pointer;
                }
                div{
                    display: flex;
                    align-items: center;
                    a{
                        margin-right: 10px;

                        font-size: 25px;
                        font-weight: bold;

                        color: var(--dc-blue);
                        
                        text-decoration: none;
                    }
                    ul{
                        display: flex;

                        list-style-type: none;
                        li{
                            margin: 0 10px;
                            img{
                                width: auto;
                                height: 40px;
                            }
                        }
                    }
                }
            }
        }
    }
</style>