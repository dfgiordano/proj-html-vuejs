<template>
    <div>
        <section class="bands position-relative text-center">
            <div class="active"></div>
            <div>
                <h3 class="text-capitalize">
                    <a href="#">
                        latest band news 
                    </a>
                </h3>
                <div class="divider"></div>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime odit molestias vel tempore eius animi possimus perspiciatis inventore consectetur.</p>
            </div>
            <div class="bands-images position-relative d-flex">
                <div class="techno">
                    <img src="../assets/images/blog_music_techo.jpg" alt="music-techno-img">
                    <div class="layover-orizontal">Technology and music</div>
                    <a href="#">
                        <h5>Technology and music</h5> 
                    </a>
                    <figure>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore placeat culpa sunt, aut perspiciatis nesciunt.</figure>
                </div>
                <div class="guitars">
                    <img src="../assets/images/blog-post3.jpg" alt="guitars-img">
                    <div class="layover-vertical">While my guitar gently weeps</div>
                    <a href="#">
                        <h5>While my guitar gently weeps</h5> 
                    </a>
                    <figure>Lorem ipsum dolor sit amet consectetur adipisicing elit.</figure>
                </div>
                <div class="sounds">
                    <img src="../assets/images/blog-post4.jpg" alt="sounds-img">
                    <div class="layover-vertical">It just sounds better</div>
                    <a href="#">
                        <h5>It just sounds better</h5> 
                    </a>
                    <figure>Lorem ipsum dolor sit amet consectetur adipisicing elit.</figure>
                </div>
                <div class="rock position-absolute">
                    <img src="../assets/images/blog_flavor_rock.jpg" alt="sounds-img">
                    <div class="layover-orizontal">The flavor of rock</div>
                    <a href="#">
                        <h5>The flavor of rock</h5> 
                    </a>
                    <figure>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore placeat culpa sunt, aut perspiciatis nesciunt.</figure>
                </div>
                <div class="legend">
                    <img src="../assets/images/blog-post2.jpg" alt="sharing-legend">
                    <div class="layover-vertical-2">Sharing the stage with a legend</div>
                    <a href="#">
                        <h5>Sharing the stage with a legend</h5> 
                    </a>
                    <figure>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore placeat.</figure>
                </div>
                <div class="old-school">
                    <div class="layover-vertical-2">Taking back to the old school</div>
                    <img src="../assets/images/blog-post1.jpg" alt="old-school-music">
                    <a href="#">
                        <h5>Taking back to the old school</h5> 
                    </a>
                    <figure>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore placeat.</figure>
                </div>
            </div>
        </section>
        <button class="latest-news d-flex text-center">
            <h4 class="text-uppercase">
                view all latest news
            </h4>
        </button>
    </div>
    
    
</template>

<script>
export default {
    name: "Bands",
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/mixins.scss';
    a {
        text-decoration: none;
        color: $main-titles;
    }
    .layover-orizontal {
        @include layover;
        height: 150px;
        width: 530px; 
    }
    .layover-vertical {
        @include layover;
        height: 350px;
        width: 250px;
    }
    .layover-vertical-2 {
        @include layover;
        height: 350px;
        width: 250px;
    }
    .bands {
        padding: 80px 0;
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
            }
    
    .bands-images {
        width: 45%;
        height: 950px;
        margin: auto;
        .techno {
            @include orizontal-img;
        }
        .old-school {
            @include vertical-img;
        }
        .sounds {
            @include vertical-middle-img;
            left: 30%;
            margin-left: 20px;
        }
        .guitars {
            @include vertical-middle-img;
        }
        .legend {
            @include vertical-img;
            top: 52%;
        }
        .rock {
            @include orizontal-img;
            bottom: 0%;
        }
    }
    .active {
        @include active-section;
        display: none;
    }
}  
    .latest-news {
        @include big_button;
    } 
</style>