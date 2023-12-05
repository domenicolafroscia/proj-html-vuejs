<script>
export default {
    props: {
        title: String,
        declaration: String,
        img: String,
        name: String,
        task: String,

    }
}
</script>
    
<template>
    <a href="">
        <div class="card">
            <h3>{{ title }}</h3>
            <p>{{ declaration }}</p>
            <div class="person">
                <img :src="img" alt="">
                <div class="details">
                    <p><strong>{{ name }}</strong></p>
                    <span>/</span>
                    <span>{{ task }}</span>
                </div>
            </div>
        </div>
    </a>
</template>

<style scoped lang="scss"> 
@use "../style/partials/variables" as *;
.card {
    background-color: $white;
    padding: 3rem;
    margin: 2rem 0;
    transition: opacity 200ms;
    

    &:not(:hover){
        opacity: 0.3;
    }

    h3 {
        color: black;
    }

    p {
        padding: 1rem 0;
        color: $outer-space;
    }

    .person {
        display: flex;
        align-items: center;

        img {
            width: 70px;
            border-radius: 50%;
        }

        .details {
             margin-left: 1rem;
        
            p {
                font-size: .8rem;
            }

            span {
                font-size: .8rem;
                color: $edward;
                padding: 0 2px;
            }
        }
    }
}
</style>