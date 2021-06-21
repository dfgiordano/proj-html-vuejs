<template>
    <header>
        <div class="container_nav">
            <div class="accordion" role="tablist">
                <b-card no-body class="mb-1">
                <b-card-header header-tag="header" class="p-1" role="tab">
                    <b-button block v-b-toggle.accordion-1 variant="info">Accordion 1</b-button>
                </b-card-header>
                <b-collapse id="accordion-1" visible accordion="my-accordion" role="tabpanel">
                    <b-card-body>
                    <b-card-text>I start opened because <code>visible</code> is <code>true</code></b-card-text>
                    <b-card-text>{{ text }}</b-card-text>
                    </b-card-body>
                </b-collapse>
                </b-card>

                <b-card no-body class="mb-1">
                <b-card-header header-tag="header" class="p-1" role="tab">
                    <b-button block v-b-toggle.accordion-2 variant="info">Accordion 2</b-button>
                </b-card-header>
                <b-collapse id="accordion-2" accordion="my-accordion" role="tabpanel">
                    <b-card-body>
                    <b-card-text>{{ text }}</b-card-text>
                    </b-card-body>
                </b-collapse>
                </b-card>

                <b-card no-body class="mb-1">
                <b-card-header header-tag="header" class="p-1" role="tab">
                    <b-button block v-b-toggle.accordion-3 variant="info">Accordion 3</b-button>
                </b-card-header>
                <b-collapse id="accordion-3" accordion="my-accordion" role="tabpanel">
                    <b-card-body>
                    <b-card-text>{{ text }}</b-card-text>
                    </b-card-body>
                </b-collapse>
                </b-card>
            </div>
        </div>
        <div class="title">
            <h1>Untold stories</h1>
            <p>There is an untold story behind every favorite song&period;</p>
            <button class="first_btn">latest album</button>
            <button class="second_btn">live dates</button>
        </div>
        
    </header>
    
</template>

<script>
export default {
    name: "Header",
     
}

</script>

<style lang="scss" scoped>
  @import '../style/general.scss';
    
    header {
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
            .first_btn {
                width: 200px;
                margin-right: 10px;
                background-color: #EA4A56;
                border: none;
                color: white;
            }
            .second_btn {
                width: 150px;
                background-color: transparent;
                border: 1px solid white;
                color: white;
            }
    }
.container_nav {
    width: 85%;
    height: 900px;
    margin: auto;
        img {
            height: 50px;
        }
}
</style>