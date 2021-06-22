<template>
    <header>
        <div class="container-nav">
            <div class="accordion" :class="isOpen ? 'background-color-red' : '' " role="tablist">
                <b-card no-body class="mb-1">
                <b-card-header header-tag="header" class="p-1" role="tab">
                    <b-button @click="clickMenuButton" class="menu-button" block v-b-toggle.accordion-1 variant="info"><i :class=" isOpen ? 'fas fa-times' : 'fas fa-bars' "></i></b-button>
                </b-card-header>
                <b-collapse id="accordion-1" visible accordion="my-accordion" role="tabpanel">
                    <b-card-body>
                    <b-card-text>I start opened because <code>visible</code> is <code>true</code></b-card-text>
                    <b-card-text>stocazzo</b-card-text>
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
        // width: 85%;
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
        }
            h1{
                font-size: 120px;
                font-weight: 700;
                letter-spacing: 5px;
                color: white;
            }
            p {
               color: white;
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
                background-color: #EA4A56;
                border: none;
                color: white;
            }
            .second-btn {
                width: 150px;
                background-color: transparent;
                border: 1px solid white;
                color: white;
                    &:hover {
                        background-color: white;
                        color: #2D2E46;
                    }
            }
    }
    .menu-button {
        background-color: transparent;
        border: none;
    }
    
    .accordion {
        div.card.mb-1 {
            background-color: transparent;
            header.card-header.p-1 {
                background-color: transparent;
                border: none;
            }
        }
    }
    .background-color-red {
            background-color: #EC4758;
        }
        .btn-check:focus,
        .btn-check:hover,
        .btn-info,
        .btn-info:focus,
        .btn-info:hover {
            background-color: transparent;
        }
</style>