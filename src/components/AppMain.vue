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
    <div class="section">
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
    </div>
</template>

<style scoped lang="scss"> 
@use "../style/partials/variables" as *;
@use "../style/partials/mixin" as *;
@import "@fortawesome/fontawesome-free/css/all.min.css";



 .section {
    background-color: $hint-of-red;
    padding: 4rem 0;

    .titles {
        text-align: center;

        p {
            color: $shady-lady;
        }

        h2 {
            color: $cod-gray;
        }
    }

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
</style>