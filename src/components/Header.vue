<template>
    <header>
        <div class="container-nav">
            <div class="accordion" :class="isOpen ? '' : 'background-color-red' " role="tablist">
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
                                <code class="link"> 
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
        <div class="title">
            <h1>Untold stories</h1>
            <p>There is an untold story behind every favorite song&period;</p>
            <button class="first-btn">latest album</button>
            <button class="second-btn">live dates</button>
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
            position: absolute;
            text-align: center;
            left: 50%;
            top: 30%;
            transform: translate(-50%,-30%);
            z-index: 1;
        }
            h1{
                font-size: 120px;
                font-weight: 700;
                letter-spacing: 5px;
                color: $main_titles;
            }
            p {
               color: $main_titles;
               font-style: italic;
               
            }
            button {
                height: 50px;
                text-transform: uppercase;
                border-radius: 2px;
            }
            .first-btn {
                width: 200px;
                margin-right: 10px;
                background-color: $secondary_titles;
                border: none;
                color: $main_titles;
            }
            .second-btn {
                width: 150px;
                background-color: transparent;
                border: 1px solid $main_titles;
                color: $main_titles;
                    &:hover {
                        background-color: $main_titles;
                        color: #2D2E46;
                    }
            }
    }
    .menu-button {
        background-color: transparent;
        border: none;
    }
    .accordion {
        position: relative;
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
        text-transform: capitalize;
        line-height: 50px;
        font-size: 20px;
            .active {
                color: $main_titles;
            }
                a {
                    text-decoration: none;
                    color: #DE7272;
                            &:hover {
                                color: $main_titles;
                            }
                }   
    }
    .background-color-red {
            background-color: $secondary_titles;
        }
        .btn-check:focus,
        .btn-check:hover,
        .btn-info,
        .btn-info:focus,
        .btn-info:hover {
            background-color: transparent;
        }
</style>