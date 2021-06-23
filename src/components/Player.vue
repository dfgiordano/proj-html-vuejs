<template>
    <section class="player">
        <p>
            &quot; I just listened to it and said to myself&comma;&quot; Man&comma; I really love this album&period;&quot;Still&comma; today&comma; it just sounds so fresh&period; It sounds full of ideas&period; These guys knew they were doing&period; They&apos;e good&period; And they&apos;re inventive&period; I havent&apos;t heard anything this year that&apos;s as inventive&period; I don&apos;t really expect to&period;&quot;
        </p>
        <div class="icon">
            <img src="../assets/images/band_interview_play_icon.png" alt="">
        </div>
    </section>
</template>

<script>
export default {
    name: "Player",
}
</script>

<style lang="scss" scoped>
    @import '../style/general.scss';
        .player {
            height: 800px;
            display: flex;
            position: relative;
            text-align: center;
            background-image: url('../assets/images/home-testimonial-parallax.jpg');
                p {
                    width: 24%;
                    margin: auto;
                    font-size: 14px;
                    line-height: 35px;
                    font-style: italic;
                    color: $main_titles;
                }
                    .icon {
                        position: absolute;
                        bottom: 20%;
                        left: 50%;
                        transform: translateX(-50%);
                        cursor: pointer;
                    }
        }
</style>