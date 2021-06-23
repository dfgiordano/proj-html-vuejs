<template>
    <section class="dates position-relative text-center">
        <div class="active"></div>
        <h3 class="text-capitalize">
            <a href="#">
                live dates
            </a>
        </h3>
        <div class="divider"></div>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aspernatur nemo numquam natus sit, culpa tempore nam, amet alias obcaecati delectus et iusto. Repudiandae, eaque magnam.</p>
        <div 
            class="accordion text-uppercase d-flex align-items-center" 
            v-for="date in LiveDates" :key="date.band"
        >   <i class="fas fa-plus"></i> 
            <span> {{ date.date }} </span>
            <span> {{ date.band }} </span>
            <span> {{ date.place }} </span>
        </div>
         <button class="latest-news d-flex position-absolute text-center">
            <h4 class="text-uppercase">
                view all live dates
            </h4>
        </button>
    </section>
</template>

<script>
export default {
    name: "Dates",
    data: function () {
        return {
            LiveDates: [
                {
                    date: "17/08/2020",
                    band: "gem festival 2020",
                    place: "anakalia, georgia"
                },
                 {
                    date: "24/09/2020",
                    band: "groovefest",
                    place: "dominical republic"
                },
                 {
                    date: "31/10/2020",
                    band: "oasis festival 2020",
                    place: "marrakech, morocco"
                },
                 {
                    date: "07/11/2020",
                    band: "moga festival",
                    place: "essaouria, morocco"
                },
                 {
                    date: "17/08/2020",
                    band: "envision festival",
                    place: "ubita, costa rica"
                },
            ]
        }
    }
}
    
</script>

<style lang="scss" scoped>
  @import '../style/general.scss';
  @import '../style/mixins.scss';

    .dates {
        height: 800px;
        padding-top: 80px;
        background-color: $dark-background;
            &:hover div.active {
                display: block;
            }
            h3 {
                @include h3;
            }
                .divider {
                    @include divider;
                }
                    p {
                        @include paragraph;
                        padding-bottom : 30px;
                    }
    }
    .accordion {
        height: 50px;
        width : 60%;
        margin: 10px auto;
        background-color: $light-background-img;
        color: $secondary-titles;
            i {
                color: $main-titles;
                margin: 0 20px;
                font-size: 10px;
                cursor: pointer;
            }
            span {
                margin: 0 5px;
                font-size: 18px;
                letter-spacing: 1px;
                cursor: pointer;
            }
    }
    .latest-news {
        @include big-button;
        bottom: 0%; 
    }
    .active {
        @include active-section;
        display: none;
    }
</style>