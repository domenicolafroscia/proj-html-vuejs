<script>
export default {
    data() {
        return {
            courses: [
                {
                    img: 'course-02-480x298.jpg',
                    price: '$40,00',
                    title: 'Learning to Write as a Professional Author',
                    lessons: '20 Lessons',
                    students: '50 Students',

                },
                {
                    img: 'stock-full-hd-03-480x298.jpg',
                    price: 'Free',
                    title: 'Customer-centric Info-Tech Strategies',
                    lessons: '24 Lessons',
                    students: '769 Students'
                },
                {
                    img: 'stock-full-hd-04-480x298.jpg',
                    price: '$19,00',
                    title: 'Open Programming Courses for Everyone: Python',
                    lessons: '17 Lessons',
                    students: '62 Students'
                },
                {
                    img: 'stock-full-hd-06-480x298.jpg',
                    price: '$26,00',
                    title: 'Academic Listening and Note-taking',
                    lessons: '14 Lessons',
                    students: '67 Students'
                },
                {
                    img: 'course-featured-image-01-480x298.jpg',
                    price: '$39,00',
                    title: 'Master jQuery in a Short Period of Time',
                    lessons: '6 Lessons',
                    students: '51 Students'
                },
                {
                    img: 'stock-full-hd-05-480x298.jpg',
                    price: '$59,00',
                    title: 'Introduction to Javascript for Beginners',
                    lessons: '14 Lessons',
                    students: '76 Students'
                },
            ],
            programCourses: [
                {
                    img: 'home-2-image-box-01.png',
                    title: 'Customize Preferences',
                    description: 'Learners are given the right to arrange and customize their study schedule and timetable based on preferences.',
                    link: 'Start here'
                },
                {
                    img: 'about-us-02-image-box-02.png',
                    title: 'Cloud Storage',
                    description: 'You can store online lessons via online cloud or download to your device and revise lessons on the way.',
                    link: 'Get Free Quote'
                },
                {
                    img: 'home-2-image-box-03.png',
                    title: 'Multimedia Channels',
                    description: 'We provide study materials with various formats: video, audio, slide, doc, prints, books and applications.',
                    link: 'Start now'
                },
            ]
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
    <section class="section-1">
        <div class="container">
            <div class="titles">
                <p>STIMULATED TO LEARN?</p>
                <h2>Featured Online Courses</h2>
            </div>
            <div class="row">
                <div class="col" v-for="(course, index) in courses" :key="index">
                    <img :src="getImagePath(course.img)" alt="">
                    <div class="details">
                        <h3>{{ course.price }}</h3>
                        <a href=""><h4>{{ course.title }}</h4></a>
                        <span><i class="fa-solid fa-file-lines"></i>{{ course.lessons }}</span>
                        <span><i class="fa-regular fa-user"></i>{{ course.students }}</span>
                    </div>
                </div>
            </div>
            <div class="btn"><button>View all courses &rightarrow;</button></div>
        </div>
    </section>


    <section class="section-2">
        <div class="container">
            <div class="titles">
                <p>MAXCOACH AVAILABLE COURSES</p>
                <h2>Access <a class="title-green" href="">Smart Tutoring</a> Program For Benefits.</h2>
            </div>
            <div class="row">
                <div class="col" v-for="(program, index) in programCourses" :key="index">
                    <img :src="getImagePath(program.img)" alt="">
                    <div class="description">
                        <h3>{{ program.title }}</h3>
                        <p>{{ program.description }}</p>
                        <span><strong><a href="">{{ program.link }} &rightarrow;</a></strong></span>
                    </div>
                </div>
            </div>
            <div class="enjoy">
                <div class="img-enjoy">
                    <img class="popup" src="../assets/img/home-2-popup-video-poster.jpg" alt="">
                    <a href=""><img class="hover-1" src="../assets/img/icon-youtube-play.png" alt=""></a>
                    <img class="hover-2" src="../assets/img/maxcoach-shape-05-100x100.png" alt="">
                    <img class="hover-3" src="../assets/img/maxcoach-shape-07-100x100.png" alt="">
                </div>
                <div class="description-enjoy">
                    <p>GET STARTED <span>EFFORTLESSLY</span></p>
                    <h2>Enjoy Our <a class="title-green" href="">Companionship</a></h2>
                    <p>Sneek peek into what has in store for you on our online teaching and mentoring portal. Seek for some hidden hints of early-bird rewards as well.</p>
                    <p class="download"><a class="title-green" href="">Download free guidebook &rightarrow;</a></p>
                </div>
            </div>
        </div>
    </section>


    <section class="section-3">
        <div class="container">
            <div class="titles">
                <p>GREAT WORDS ABOUT MAXCOACH</p>
                <h2>Our <a class="title-green" href="">top learners'</a> verbatim</h2>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss"> 
    @use "../style/partials/variables" as *;
    @use "../style/partials/mixin" as *;
    @import "@fortawesome/fontawesome-free/css/all.min.css";



    .section-1 {
        background-color: $hint-of-red;
        padding: 4rem 0;

        .row {
            @include flex(row, center, stretch, wrap);

            .col {
                width: calc(100% / 2);
                margin-top: 3rem;
                display: flex;
                align-items: center;

                img {
                    border-radius: 50%;
                    width: 150px;
                    height: 150px;
                    margin-right: 1rem;
                }

                .details {
                    
                    h3 {
                        color: $mountain-meadow;
                    }

                    h4 {
                        color: $cod-gray;
                        padding: 10px 0;

                        &:hover {
                            color: $mountain-meadow;
                        }
                    }

                    span {
                        color: $shady-lady;
                        margin-right: 1rem;

                        i {
                            margin-right: .5rem;
                            font-size: .8rem;
                        }
                    }
                }
            }

        }

        .btn {
            text-align: center;
            margin-top: 4rem;

            button {
                background-color: $mountain-meadow;
                border: none;
                padding: .8rem 3rem;
                border-radius: 5px;
                color: $white;
                cursor: pointer;
            }
        }
    }


    .section-2 {
        padding: 4rem 0;
        

        .row {
            @include flex(row, center, stretch, nowrap);
            margin-top: 4rem;

            .col {
                width: calc(100% / 3);

                img {
                    width: 140px;
                }

                .description {
                    padding-top: 1rem;

                    p {
                        padding: 1rem 0;
                    }

                    a {
                        color: $outer-space;
                    }
                }
            
            }
        }
        
        .enjoy {
            padding-top: 2rem;
            display: flex;
            align-items: center;


            .img-enjoy {
                position: relative;
                .popup {
                    width: 450px;
                    position: relative;
                    z-index: 2;
                }

                .hover-1, .hover-2, .hover-3 {
                    position: absolute;
                }

                .hover-1 {
                    left: 50%;
                    transform: translate(-50%);
                    top: 40%;
                    z-index: 3;
                }

                .hover-2 {
                    top: 30px;
                    left: -60px;
                }

                .hover-3 {
                    bottom: -60px;
                    right: -10px;
                }
            }

            .description-enjoy {
                margin-left: 4rem;
                 
                p {
                    color: $edward;

                    span {
                        color: $cod-gray;
                    }
                }

                h2 {
                    color: $cod-gray;
                    padding: 1rem 0;
                }

                .download {
                    padding-top: 2rem;

                    a {
                        text-decoration: underline;
                        text-decoration-color: $edward;
                    }
                }
            }
        }
    }

    .section-3 {
        margin: 4rem 0;
    }





</style>