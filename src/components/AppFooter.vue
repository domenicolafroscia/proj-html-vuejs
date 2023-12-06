<script>
export default {
    data() {
        return {
            socialIcons: ['fa-square-facebook', 'fa-twitter', 'fa-instagram', 'fa-linkedin']
        };
    },
    props: {
        voiceMenu: Array,
        voiceMenu1: Array
    }
    
};
</script>

<template>
    <footer>
        <div class="container">
            <div class="menu">
                <div class="footer-left">
                    <h3>Address</h3>
                    <p>382 NE 191st St # 87394 Miami, FL 33179-3899 +1(305) 547-9909 (9am - 5pm EST, Monday - Friday) support@maxcoach.com</p>
                    <ul class="social-list">
                        <li class="social" v-for="social in socialIcons"><a href=""><i :class="`fa-brands ${social}`"></i></a></li>
                    </ul>
                </div>
                <div class="footer-right">
                    <div class="explore">
                        <h3>Explore</h3>
                        <ul>
                            <li v-for="menu in voiceMenu"><a href="">{{ menu }}</a></li>
                        </ul>
                    </div>
                    <div class="information">
                        <h3>Information</h3>
                        <ul>
                            <li v-for="menu1 in voiceMenu1"><a href="">{{ menu1 }}</a></li>
                        </ul>
                    </div>
                </div>
            </div>
            <p class="rights">2020 Maxcoach. All Rights Reserved</p>
        </div>
        <div class="footer-btn">
            <button>&uparrow;</button>
        </div>
    </footer>
</template>

<style scoped lang="scss"> 
@use "../style/partials/variables" as *;
@use "../style/partials/mixin" as *;
@import "@fortawesome/fontawesome-free/css/all.min.css";

footer {
    background-color: $hint-of-red;
    padding: 2rem 0;

    .menu {
        display: flex;
        justify-content: space-around;

        .footer-left {
            width: 50%;

            p {
                font-size: .9rem;
                color: $cod-gray;
                padding: 1rem 0;
            }

            .social-list {
                display: flex;
                gap: 1rem;

                .social {
                    font-size: 1.4rem;

                    i {
                        color: $edward;
                    }
                    
                }
            }
        }

        .footer-right {
            display: flex;
            gap: 5rem;

            .explore {
                
                h3 {
                    padding-bottom: 1rem;
                }

                ul {

                    li {
                        padding-bottom: .8rem;
                        
                        a {
                            color: $cod-gray;
                        }
                    }
                }
            }

            .information {
                
                h3 {
                    padding-bottom: 1rem;
                }

                ul {

                    li {
                        padding-bottom: .8rem;
                        
                        a {
                            color: $cod-gray;
                        }
                    }
                }
            }
        }

    }

    .rights {
        text-align: center;
        color: $edward;
        font-size: .8rem;
        padding-top: 4rem;
    }

    .footer-btn {
        text-align: end;
        margin-right: 1rem;

        button {
            color: $white;
            background-color: $mountain-meadow;
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            cursor: pointer;
        }
    }
}
</style>