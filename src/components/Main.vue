<template>
  <div>
      <section class="music position-relative text-center">
        <div class="active"></div>
          <h3 class="text-capitalize">
            <a href="#">
              music is lIfe
            </a>
          </h3>
          <div class="divider"></div>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime odit molestias vel tempore eius animi possimus perspiciatis inventore consectetur.</p>
      </section>
      <Bands />
      <Player />
      <Dates />
  </div>
</template>

<script>
import Bands from './Bands'
import Player from './Player'
import Dates from './Dates'

export default {
    name: "Main",
    components: {
      Bands,
      Player,
      Dates,
    },
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/mixins.scss';

  .music {
      height: 315px;
      padding-top: 80px;
      background-color: $light-background-img;
        h3 {
          @include h3;
        }
        .divider {
          @include divider;
        }
        p {
          @include paragraph;
        }
    }
    .active {
      @include active-section;
    }
</style>