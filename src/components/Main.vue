<template>
  <div>
      <section class="music">
          <h3>
            <a href="#">
              music is lIfe
            </a>
          </h3>
          <div class="divider"></div>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Maxime odit molestias vel tempore eius animi possimus perspiciatis inventore consectetur.</p>
      </section>
      <Bands />
  </div>
</template>

<script>
import Bands from './Bands'
export default {
    name: "Main",
    components: {
      Bands
    }
}
</script>

<style lang="scss" scoped>
  @import '../style/general.scss';

    .music {
      height: 300px;
      background-color: #333844;
      text-align: center;
        h3 {
          text-transform: capitalize;
          font-size: 50px;
          font-weight: 800;
          padding: 50px 0;
            a {
              text-decoration: none;
              color: white;
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
          color: #AEAEB0;
        }
    }
</style>