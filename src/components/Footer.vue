<template>
    <div>
        <div class="section_1_cont d-flex">
            <div class="section_1 d-flex justify-content-between">
                <a href="#">
                    <img src="../assets/images/logo_footer.png" alt="avada_logo">
                </a>
                <ul class="align-self-center">
                    <li 
                        v-for="(link, index) in links"
                        :key="index">
                        <a :href="link.url" :class=" { active : link.current } ">
                            {{ link.text }}
                        </a>
                    </li>
                </ul> 
            </div>
        </div>
        <div class="section_2_cont">
            <div class="section_2 d-flex justify-content-between">
                <ul class="align-self-center">
                    <li>
                        <a href="#">
                            <i class="far fa-copyright"></i>
                            Copyright 2012-2020
                        </a>
                    </li>
                    <li
                        class="divider"
                        v-for="link in rightsLinks"
                        :key="link.url"
                    >
                        <a href="#">
                            {{ link.text }}
                        </a>
                    </li>
                </ul>
                <ul class="align-self-center">
                    <li class="social">
                        <a href="#">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                    </li>
                    <li class="social">
                        <a href="#">
                            <i class="fab fa-twitter"></i>
                        </a>
                    </li>
                    <li class="social">
                        <a href="#">
                            <i class="fab fa-instagram"></i>
                        </a>
                    </li>
                    <li class="social">
                        <a href="#">
                            <i class="fab fa-youtube"></i>
                        </a>
                    </li>
                </ul>
        </div>
        </div>
        
    </div>
</template>

<script>
export default {
    name: "Footer",
    data: function () {
        return {
            links: [
                {
                    text: "home",
                    url: "#Home",
                    current: true
                },
                {
                    text: "meet the band",
                    url: "#Meet_the_band",
                    current: false
                },
                {
                    text: "live Dates",
                    url: "#Live_Dates",
                    current: false
                },
                {
                    text: "latest News",
                    url: "#Latest_News",
                    current: false
                },
                {
                    text: "albums",
                    url: "#Albums",
                    current: false
                },
                {
                    text: "fans",
                    url: "#Fans",
                    current: false
                }
            ],
            rightsLinks: [
                {
                    text: "AVADA THEME BY THEMEFUSION",
                    url: "#avada_theme"
                },
                {
                    text: "ALL RIGHTS RESERVED",
                    url: "#all_rights"
                },
                {
                    text: "POWERED BY WORDPRESS",
                    url: "#wordpress"
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/general.scss';

    .section_1_cont {
        height: 150px;
        background-color: #333844;
            .section_1 {
                width: 90%;
                margin: auto;
            }
    }
    a:hover {
        color: $main_titles;
    }
    ul {
        display: inline;
        li {
            display: inline;
            list-style: none;
                .active {
                    color: $main_titles;
                }
                a {
                    margin-right: 10px;
                    text-decoration: none;
                    text-transform: capitalize;
                    margin-left: 10px;
                    color: $text-color;
                }
        }
    }
    .section_2_cont {
        display: flex;
        background-color: #252A32;
    }
    .section_2 {
        width: 90%;
        margin: auto;
        height: 110px;
        color: $text-color;
            .divider {
            border-left: 2px solid $text-color;
        }
    }
    .social {
        padding: 5px;
        margin: 5px;
        background-color: #333844;
    }
</style>