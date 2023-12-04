<script>
export default {
    data() {
        return {
            clients: [
                {
                    img: 'client-logo-01.png'
                },
                {
                    img: 'client-logo-02.png'
                },
                {
                    img: 'client-logo-03.png'
                },
                {
                    img: 'client-logo-04.png'
                },
                {
                    img: 'client-logo-05.png'
                },
                {
                    img: 'client-logo-06.png'
                },
            ],
        };
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        },
    },
};
</script>

<template>
    <div class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="description">
                    <h1>Distant learning for further expansion</h1>
                    <p>Learning a life-long journey that in fact we never find the terminate stop. Stop searching, enjoy the process.</p>
                    <button><i class="fa-solid fa-download" style="color: #ffffff;"></i> Download free guide</button>
                    <p>Have a questions? <a href=""><strong>Get Free Sample &rightarrow;</strong></a></p>
                </div>
                <div class="img-hero">
                    <img class="about-me" src="../assets/img/about-me-profile-ohm4dxoearqbxny7q3bq1pzbdgofdx0tobbeqcvzd0.jpg" alt="">
                    <img class="decoration-1" src="../assets/img/maxcoach-shape-02.png" alt="">
                    <img class="decoration-2" src="../assets/img/maxcoach-shape-07-100x100.png" alt="">
                    <img class="decoration-3" src="../assets/img/maxcoach-shape-08.png" alt="">
                    <img class="decoration-4" src="../assets/img/maxcoach-shape-08.png" alt="">
                </div>
            </div>
            <div class="client-logo">
                <ul>
                    <li v-for="client in clients" :key="client.img"><img :src="getImagePath(client.img)" alt=""></li>
                </ul>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss"> 
@use "../style/partials/variables" as *;
@import "@fortawesome/fontawesome-free/css/all.min.css";

.hero {
    margin: 3rem 0;
    display: flex;
    .hero-content {
        display: flex;
        align-items: center;

        .description {
            margin-right: 10rem;

            h1 {
                color: $cod-gray;
            }

            p {
                color: $edward;
                padding: 1rem 0;
            }

            button {
                background-color: $mountain-meadow;
                border: none;
                padding: .8rem 1.5rem;
                border-radius: 5px;
                color: $white;
                cursor: pointer;
            }

            a {
                color: $mountain-meadow;
                text-decoration: underline;
                text-decoration-color: $edward;
            }
        }

        .img-hero {
            position: relative;
            .about-me {
                border-radius: 50%;
                width: 450px;
                position: relative;
                z-index: 2;
            }

            .decoration-1 {
                width: 90px;
                position: absolute;
                top: 100px;
            }

            .decoration-2 {
                position: absolute;
                bottom: 7px;
                left: 270px;
            }

            .decoration-3 {
                position: absolute;
                top: 135px;
                left: -65px;
                width: 120px;
                
            }

            .decoration-4 {
                position: absolute;
                bottom: 105px;
                left: -65px;
                width: 120px;
            }
        }   
    }

    .client-logo {
       
        ul {
            display: flex;
            align-items: center;
            margin-top: 3rem;

            li {
                margin: 0 3rem;
                filter: grayscale(100%);
            }
        }
    }
}

</style>