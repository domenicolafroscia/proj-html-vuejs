<script>
export default {
    props: {
        items: Array
    }
}
</script>

<template>
    <header>
        <div class="container d-flex justify-content-between align-items-center">
            <img class="logo" src="../assets/img/dark-logo.png" alt="">
            <nav>
                <ul>
                    <li v-for="item in items"><a class="link-black" href="">{{ item }} <i class="chevron fa-solid fa-chevron-down" style="color: #0b0b0b;"></i> </a></li>
                    <li><a href=""><i class="fa-regular fa-circle-user" style="color: #0b0b0b;"></i></a></li>
                </ul>
                <div class="search">
                    <input class="search-text" type="text" placeholder="Search..." id="site-search" name="" />
                    <button class="search-btn"><i class="fa-solid fa-magnifying-glass" style="color: #1fad96;"></i></button>
                </div>
            </nav>
        </div>
    </header>
</template>

<style scoped lang="scss"> 
@use "../style/partials/variables" as *;
@import "@fortawesome/fontawesome-free/css/all.min.css";


header {
    border-bottom: 4px solid $hint-of-red;
    width: 100%;

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;

        .logo {
            width: 200px;
        }

        nav {
            display: flex;

            ul {
                display: flex;
                margin: 2rem;

                li {
                    padding: 0 .5rem;

                    .link-black {
                        color: $cod-gray;
                        display: flex;
                        padding: 0 20px;
                        gap: .3rem;
                        align-items: center;

                        .chevron {
                            font-size: 10px;
                        }
                    }
                }
            }
        

            .search {
                position: relative;

                .search-text {
                    height: 40px;
                    background-color: $hint-of-red;
                    border: none;
                    margin-left: 1rem;
                    border-radius: 5px;
                    margin-top: 1rem;

                }

                .search-btn {
                    border: none;
                    background: none;
                    position: absolute;
                    right: 10px;
                    top: 28px;
                    cursor: pointer;
                }
            }
        }
        
    }
}

 
</style>