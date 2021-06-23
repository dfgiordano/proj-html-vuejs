<template>
    <header>
        <div class="container-nav">
            <div class="accordion position-relative" :class="isOpen ? '' : 'background-color-red' " role="tablist">
                <b-card no-body class="mb-1">
                <b-card-header header-tag="header" class="p-1 d-flex justify-content-between" role="tab">
                    <img src="../assets/images/avada-music-logo-retina.png" alt="avada-logo">
                    <b-button @click="clickMenuButton" class="menu-button" block v-b-toggle.accordion-1 variant="info"><i :class=" isOpen ? 'fas fa-bars' : 'fas fa-times' "></i></b-button>
                </b-card-header>
                <b-collapse id="accordion-1" collapse accordion="my-accordion" role="tabpanel">
                    <b-card-body>  
                        <b-card-text 
                        class="d-flex justify-content-center"
                            v-for="(link,url) in links"
                            :key="url"> 
                                <code class="link text-capitalize"> 
                                    <a 
                                    :class=" { active : link.current }"
                                    href="#">
                                        {{ link.text }} 
                                    </a>  
                                </code>
                        </b-card-text>
                    </b-card-body>
                </b-collapse>
                </b-card>
            </div>
        </div>
        <div class="title text-center position-absolute">
            <h1 class="text-capitalize">Untold stories</h1>
            <p>There is an untold story behind every favorite song&period;</p>
            <button class="first-btn text-uppercase">latest album</button>
            <button class="second-btn text-uppercase">live dates</button>
        </div>
        
    </header>
    
</template>

<script>
export default {
    name: "Header",
    data: function () {
        return {
            isOpen : true,
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
        }
    },
    methods: {
        clickMenuButton: function () {
            this.isOpen = !this.isOpen;
        }
    }
}

</script>

<style lang="scss" scoped>
  @import '../style/general.scss';
  @import '../style/mixins.scss';
    
    .container-nav {
        width: 90%;
        height: 900px;
        margin: auto;
            img {
                height: 50px;
            }
    }
    header:not(.p-1) {
        background-image: url('../assets/images/home_slider.jpg');
        background-position: 0% 60%;
            .title {
                left: 50%;
                top: 30%;
                transform: translate(-50%,-30%);
                z-index: 1;
            }
                h1{
                    font-size: 120px;
                    font-weight: 700;
                    letter-spacing: 5px;
                    color: $main-titles;
                }
                p {
                    font-style: italic;
                    color: $main-titles;
                }
                button {
                    height: 50px;
                    border-radius: 2px;
                }
                .first-btn {
                    width: 200px;
                    margin-right: 10px;
                    border: none;
                    background-color: $secondary-titles;
                    color: $main-titles;
                        &:hover {
                            @include hover-button;
                            }
                }
                .second-btn {
                    width: 150px;
                    border: 1px solid $main-titles;
                    background-color: transparent;
                    color: $main-titles;
                        &:hover {
                            @include hover-button;
                        }
                }
    }
    .menu-button {
        background-color: transparent;
        font-size: 20px;
        border: none;
        color: $main-titles;
            &:hover {
                color: $main-titles;
            }
            &:focus {
                outline: none;
                box-shadow: none;
            }
    }
    .fa-times {
        color: lightcoral;
            &:hover {
                color: $main-titles;
            }
            &:focus {
                outline: none;
                box-shadow: none;
            }
    }
    .accordion {
        z-index: 2;
        div.card.mb-1 {
            background-color: transparent;
            header.card-header.p-1 {
                display: flex;
                justify-content: flex-end;
                background-color: transparent;
                border: none;
            }
        }
    }
    .link {
        line-height: 50px;
        font-size: 20px;
            .active {
                color: $main-titles;
            }
            a {
                text-decoration: none;
                color: lightcoral;
                    &:hover {
                        color: $main-titles;
                    }
            }   
    }
    .background-color-red {
            background-color: $secondary-titles;
        }
        .btn-check:focus,
        .btn-check:hover,
        .btn-info,
        .btn-info:focus,
        .btn-info:hover {
            background-color: transparent;
        }
</style>