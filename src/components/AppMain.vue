<script>
import AppCard from './AppCard.vue';

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
            ],
            topLearners: [
                {
                    title: "It's a choice of quality for people with special needs",
                    declaration: "I'm a very strict person so I require everything to be organized and neat. Then, I'll be able to make thinghs right and shine. MaxCoach guys just got me",
                    img: 'src/assets/img/testimonial-avata-03.jpg',
                    name: 'FLORENCE THEMES',
                    task: 'Multimedia Admin'
                },
                {
                    title: 'High level of efficiency and scientific teaching methods',
                    declaration: 'I am free to learn at my own pace, follow on my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.',
                    img: 'src/assets/img/testimonial-avata-02.jpg',
                    name: 'MINA HOLLACE',
                    task: 'Freelancer'
                },
                {
                    title: 'Professional team of specialists and passionate mentors at reach',
                    declaration: 'I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.',
                    img: 'src/assets/img/testimonial-avata-04.jpg',
                    name: 'MADLEY PONDOR',
                    task: 'IT Specialist'
                },
            ],
            results: [
                {
                    name: 'Successfully trained',
                    numbers: '1790',
                    objects: 'ENROLLED LEARNERS',
                },
                {
                    name: 'Proudly Received',
                    numbers: '19',
                    objects: 'COUNTRYWIDE AWARDS',
                },
                {
                    name: 'Firmly Estabilished',
                    numbers: '24',
                    objects: 'LOCAL BRANCHES',
                },
                {
                    name: 'Getting Featured on',
                    numbers: '1090',
                    objects: 'BLOG POSTS',
                },
            ],
            blogs: ['Become a Better Blogger: Content Planning', 'Promoting Your Online Business on Pinterest', 'Gamification and Game-Based Learning', "Designing an Online Course from Experet's Perspective", 'Why Online Courses Are the Future of Education'],
            cardBlogs: [
                {
                    img: 'artist-blog-03-480x352.jpeg',
                    task: 'ARTIST',
                    description: 'Brush Strokes Energize Trees in Paintings',
                    date: 'May 15, 2020',
                    views: '688 views',
                },
                {
                    img: 'artist-blog-01-480x352.jpg',
                    task: 'ARTIST',
                    description: 'Pocket-Sized Notebooks Hold Miniature Paintings',
                    date: 'May 15, 2020',
                    views: '603 views',
                },
            ]
        };
    },
    methods: {
        getImagePath(img) {
            return new URL(`../assets/img/${img}`, import.meta.url).href;
        },
    },
    components: { AppCard }
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
                        <a href="">
                            <h4>{{ course.title }}</h4>
                        </a>
                        <span><i class="fa-solid fa-file-lines"></i>{{ course.lessons }}</span>
                        <span><i class="fa-regular fa-user"></i>{{ course.students }}</span>
                    </div>
                </div>
            </div>
            <div class="btn"><button>View all courses &rightarrow;</button></div>
        </div>
    </section>


    <section class="section-2">
        <div class="background">
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
                        <p>Sneek peek into what has in store for you on our online teaching and mentoring portal. Seek for
                            some hidden hints of early-bird rewards as well.</p>
                        <p class="download"><a class="title-green" href="">Download free guidebook &rightarrow;</a></p>
                    </div>
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
            <div class="row">
                <div class="col" v-for="(top, index) in topLearners" :key="index">
                    <AppCard :title="top.title" :declaration="top.declaration" :img="top.img" :name="top.name"
                        :task="top.task" />
                </div>
            </div>
            <div class="titles">
                <p><strong>Start today for getting <a class="title-green" href="">Online Certification</a></strong></p>
                <h2>You can be your own guilding star with our help!</h2>
                <div class="btn"><button>Get started now &rightarrow;</button></div>
                <img class="decoration" src="../assets/img/maxcoach-shape-01.png" alt="">
                <img class="decoration-1" src="../assets/img/maxcoach-shape-02.png" alt="">
            </div>
        </div>
    </section>


    <section class="section-4">
        <div class="container">
            <div class="row">
                <div class="col" v-for="result in results" :key="result">
                    <h3>{{ result.name }}</h3>
                    <h2><strong>{{ result.numbers }}</strong></h2>
                    <p><strong>{{ result.objects }}</strong></p>
                </div>
            </div>
        </div>
    </section>


    <section class="section-5">
        <div class="container">
            <div class="blogs">
                <div class="best-blogs">
                    <p>ENJOYABLE INSIGHTS</p>
                    <h3><strong>Most Viewed</strong> <a class="title-green" href="">Best Blogs</a></h3>
                    <ul>
                        <li v-for="(blog, index) in blogs" :key="index"><a class="link-blogs"
                                href=""><strong><span>&rightarrow;</span>{{ blog }}</strong></a></li>
                    </ul>
                </div>
                <div class="card-blogs">
                    <div class="row">
                        <div class="col" v-for="card in cardBlogs" :key="card">
                            <div class="card">
                                <img :src="getImagePath(card.img)" alt="">
                                <div class="text-card">
                                    <p>{{ card.task }}</p>
                                    <h4><a href="">{{ card.description }}</a></h4>
                                    <span class="date"><i class="fa-regular fa-calendar"></i>{{ card.date }}</span>
                                    <span><i class="fa-solid fa-eye"></i>{{ card.views }}</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>


    <section class="section-6">
        <div class="container">
            <div class="titles">
                <h2>Subscribe <a class="title-green" href="">Newsletter</a></h2>
                <p class="newsletter">Enter your email address to register to our newsletter subscription delivered on a regular basis!</p>
            </div>
            <div class="email-btn">
                <input type="email" placeholder="Enter your email" id="site-search" name="" />
                <button>Subscribe</button>
            </div>
            <img class="details-1" src="../assets/img/maxcoach-shape-02.png" alt="">
            <img class="details-2" src="../assets/img/maxcoach-shape-02.png" alt="">
            <img class="details-3" src="../assets/img/maxcoach-shape-09.png" alt="">
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
                 object-fit: cover;
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

 }


 .section-2 {
     background-color: $hint-of-red;

     .background {
         background-color: $white;
         border-radius: 0 0 70% 0;
         padding-bottom: 5rem;

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

                 .hover-1,
                 .hover-2,
                 .hover-3 {
                     position: absolute;
                 }

                 .hover-1 {
                     left: 50%;
                     transform: translate(-50%);
                     top: 40%;
                     z-index: 3;
                     width: 70px;
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
                 width: 50%;

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

 }


 .section-3 {
     padding: 4rem 0;
     background-color: $hint-of-red;

     .row {
         @include flex(row, center, stretch, nowrap);
         gap: 3rem;


         .col {
             width: calc(100% / 3);

         }
     }

     .titles {
         position: relative;

         p {
             font-size: 1rem;
             color: black;
         }

         .decoration,
         .decoration-1 {
             width: 80px;
             position: absolute;
         }

         .decoration {
             left: 70px;
             top: 85px;

         }

         .decoration-1 {
             right: 50px;
             top: 70px;
         }

     }
 }


 .section-4 {

     .row {
         @include flex(row, center, stretch, nowrap);

         .col {
             text-align: center;
             border-right: 1px solid $hint-of-red;
             border-left: 1px solid $hint-of-red;
             padding: 5rem 2rem;

             h2 {
                 color: $mountain-meadow;
                 font-size: 2rem;
                 padding: 1rem 0;
             }

             p {
                 color: $edward;
                 font-size: .7rem;
             }
         }
     }
 }


 .section-5 {
     background-color: #f5f1ed;
     padding: 4rem 0;

    .blogs {
        display: flex;
        justify-content: center;
        align-items: center;
        .best-blogs {
            padding-right: 4rem;

            p {
                color: $edward;
                font-size: .7rem
            }

            h3 {
                font-size: 1.5rem;
                padding: 1rem 0;
            }

            li {
                padding: .5rem 0;

                .link-blogs {
                    color: $cod-gray;

                    span {
                        padding-right: 5px;
                    }

                }
            }
        }

        .card-blogs {
            .row {
                @include flex(row, center, stretch, nowrap);
                gap: 2rem;

                .col {
                    .card {
                        background-color: $white;
                        width: 250px;

                        .text-card {
                            padding: 1.5rem;

                            p {
                                color: $edward;
                                font-size: .7rem;
                            }

                            h4 {
                                padding-top: .5rem;
                                padding-bottom: 1rem;
                                
                                a {
                                    color: $cod-gray;
                                }
                            }

                            span {
                                font-size: .7rem;
                                color: $edward;

                                i {
                                    padding-right: 5px;
                                }
                            }

                            .date {
                               padding-right: 10px;

                            }

                        }

                    }
                }
            }
        }
    }
 }


 .section-6 {
    padding: 4rem 0;
    position: relative;
    .newsletter {
        font-size: .9rem;
        color: $cod-gray;
        padding-top: 1rem;
    }

    .email-btn {
        text-align: center;
        padding-top: 1rem;

        input {
            height: 40px;
            background-color: $hint-of-red;
            border: none;
            width: 35%;
            border-radius: 5px 0 0 5px;
        }

        button {
            color: $white;
            height: 40px;
            border: none;
            background: $mountain-meadow;
            border-radius: 0 5px 5px 0;
            cursor: pointer;
            padding: .5rem 1rem;
        }
    }

    .details-1, .details-2, .details-3 {
        position: absolute;
    }

    .details-1 {
        top: 60px;
        width: 80px;
    }

    .details-2 {
        bottom: 50px;
        right: 180px;
        width: 80px;
    }

    .details-3 {
        width: 100px;
        bottom: 90px;
        right: 190px;
        color: $edward;
    }
 }
</style>