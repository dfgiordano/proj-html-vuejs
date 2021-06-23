<template>
    <div>
        <section class="bands">
            <div>
                <h3>
                <a href="#">
                    latest band news 
                </a>
                </h3>
                <div class="divider"></div>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime odit molestias vel tempore eius animi possimus perspiciatis inventore consectetur.</p>
            </div>
            <div class="bands-images">
                <div class="techno">
                    <img src="../assets/images/blog_music_techo.jpg" alt="music-techno-img">
                    <a href="#">
                        <h5>Technology and music</h5> 
                    </a>
                    <figure>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore placeat culpa sunt, aut perspiciatis nesciunt.</figure>
                </div>
                <div class="guitars">
                    <img src="../assets/images/blog-post3.jpg" alt="guitars-img">
                    <a href="#">
                        <h5>While my guitar gently weeps</h5> 
                    </a>
                    <figure>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore placeat culpa sunt, aut perspiciatis nesciunt.</figure>
                </div>
                <div class="sounds">
                    <img src="../assets/images/blog-post4.jpg" alt="sounds-img">
                    <a href="#">
                        <h5>It just sounds better</h5> 
                    </a>
                    <figure>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore placeat culpa sunt, aut perspiciatis nesciunt.</figure>
                </div>
                <div class="rock">
                    <img src="../assets/images/blog_flavor_rock.jpg" alt="sounds-img">
                    <a href="#">
                        <h5>The flavor of rock</h5> 
                    </a>
                    <figure>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore placeat culpa sunt, aut perspiciatis nesciunt.</figure>
                </div>
                <div class="legend">
                    <img src="../assets/images/blog-post2.jpg" alt="">
                    <a href="#">
                        <h5>Sharing the stage with a legend</h5> 
                    </a>
                    <figure>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore placeat.</figure>
                </div>
                <div class="old-school">
                    <img src="../assets/images/blog-post1.jpg" alt="old-school-music">
                    <a href="#">
                        <h5>Taking back to the old school</h5> 
                    </a>
                    <figure>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore placeat.</figure>
                </div>
            </div>
        </section>
        <button class="latest-news">
            <h4>
                view all latest news
            </h4>
        </button>
    </div>
    
    
</template>

<script>
export default {
    name: "Bands"
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
    a {
        text-decoration: none;
        color: $main_titles;
    }
    .bands {
        text-align: center;
        padding-bottom: 80px;
        background-color: #252A32;
        h3 {
          text-transform: capitalize;
          font-size: 50px;
          font-weight: 800;
          padding-top: 35px;
            a {
                text-decoration: none;
                color: $main_titles;
            }
            
        }
            .divider {
            height: 3px;
            width: 250px;
            margin: auto;
            background-color: #424958;
            }
                p {
                width: 40%;
                margin: 30px auto;
                line-height: 30px;
                font-size: 14px;
                color: $text-color;
                }
    }
    .bands-images {
        display: flex;
        position: relative;
        width: 45%;
        height: 950px;
        margin: auto;
        .techno {
                width: 530px;
                height: 230px;
                text-align: left;
                background-color: $background_Img;
                    img {
                        height: 150px;
                        width: 100%;
                        cursor: pointer;
                    }
                    h5 {
                        margin: 10px;
                        font-size: 14px;
                        font-weight: 600;
                        color: $secondary_titles;
                    }
                    figure {
                        margin: 10px;
                        font-size: 12px;
                        padding-bottom: 5px;
                        color: $text-color;
                    }
        }
        .old-school {
            width: 250px;
            height: 455px;
            position: absolute;
            right: 5%;
            text-align: left;
            margin-left: 20px;
            background-color: $background_Img;
                img {
                    height: 350px;
                    width: 100%;
                    cursor: pointer;
                }
                h5 {
                    margin: 10px;
                    font-size: 14px;
                    font-weight: 600;
                    color: $secondary_titles;
                }
                figure {
                    margin: 10px;
                    font-size: 12px;
                    padding-bottom: 5px;
                    color: $text-color;
                }
        }
        .sounds {
            position: absolute;
            top: 25%;
            left: 30%;
            width: 250px;
            height: 435px;
            text-align: left;
            margin-top: 20px;
            margin-left: 20px;
            background-color: $background_Img;
                img {
                    height: 320px;
                    width: 100%;
                    cursor: pointer;
                }
                h5 {
                    margin: 10px;
                    font-size: 14px;
                    font-weight: 600;
                    color: $secondary_titles;
                }
                figure {
                    margin: 10px;
                    font-size: 12px;
                    padding-bottom: 5px;
                    color: $text-color;
                }
        }
        .guitars {
            position: absolute;
            top: 25%;
            width: 250px;
            height: 435px;
            text-align: left;
            margin-top: 20px;
            background-color: $background_Img;
                img {
                    height: 320px;
                    width: 100%;
                    cursor: pointer;
                }
                h5 {
                    margin: 10px;
                    font-size: 14px;
                    font-weight: 600;
                    color: $secondary_titles;
                }
                figure {
                    margin: 10px;
                    font-size: 12px;
                    padding-bottom: 5px;
                    color: $text-color;
                }
        }
        .legend {
            width: 250px;
            height: 455px;
            position: absolute;
            top: 52%;
            right: 5%;
            text-align: left;
            margin-left: 20px;
            background-color: $background_Img;
                img {
                    height: 350px;
                    width: 100%;
                    cursor: pointer;
                }
                h5 {
                    margin: 10px;
                    font-size: 14px;
                    font-weight: 600;
                    color: $secondary_titles;
                }
                figure {
                    margin: 10px;
                    font-size: 12px;
                    padding-bottom: 5px;
                    color: $text-color;
                }
        }
        .rock {
            width: 530px;
            position: absolute;
            bottom: 0%;
            height: 230px;
            text-align: left;
            background-color: $background_Img;
                img {
                    height: 150px;
                    width: 100%;
                    cursor: pointer;
                }
                h5 {
                    margin: 10px;
                    font-size: 14px;
                    font-weight: 600;
                    color: $secondary_titles;
                }
                figure {
                    margin: 10px;
                    font-size: 12px;
                    padding-bottom: 5px;
                    color: $text-color;
                }
        }
    }
    .latest-news {
        display: flex;
        justify-content: center;
        height: 100px;
        width: 100%;
        text-align: center;
        border: none;
        background-color: $secondary_titles;
            &:hover {
                background-color: $main_titles;
                color: #2D2E46;
            }
            h4 {
                align-self: center;
                text-transform: uppercase;
                font-size: 16px;
            }
    }










</style>