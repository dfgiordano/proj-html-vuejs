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
                    <li>
                        <a href="#">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <i class="fab fa-twitter"></i>
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <i class="fab fa-instagram"></i>
                        </a>
                    </li>
                    <li >
                        <a href="#">
                            <i class="fab fa-youtube"></i>
                        </a>
                    </li>
                </ul>
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
        background-color: #2D2E46;
            .section_1 {
                width: 85%;
                margin: auto;
            }
    }
    a:hover {
        color: white;
    }
    ul {
        display: inline;
        li {
            display: inline;
            list-style: none;
                .active {
                    color: white;
                }
                a {
                    margin-right: 10px;
                    text-decoration: none;
                    text-transform: capitalize;
                    margin-left: 10px;
                    color: #AEAEB0;
                }
        }
    }
    .section_2 {
        display: flex;
        height: 110px;
        background-color: #252A32;
        color: #AEAEB0;
            .divider {
            border-left: 2px solid #AEAEB0;
                .social {
                    padding: 5px;
                    background-color: #333844;
                }
        }
    }
</style>