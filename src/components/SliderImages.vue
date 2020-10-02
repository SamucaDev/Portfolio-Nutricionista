<template>
  <div>
    <div class="slide-image" :class="{'scroll': scrollScreenHeader == true}">
      <b-carousel
        id="carousel-1"
        class="carousel-class"
        v-model="slide"
        :interval="4000"
        controls
        indicators
        background="#ababab"
        img-width="1024"
        img-height="480"
        style="text-shadow: 1px 1px 2px #333;"
        @sliding-start="onSlideStart"
        @sliding-end="onSlideEnd"
      >
        <b-carousel-slide class="item-carousel">
          <template v-slot:img>
            <img
              class="d-block img-fluid w-100"
              width="1024"
              height="480"
              src="../assets/img/img-carousel/image2.jpg"
              alt="image slot"
            />
          </template>
        </b-carousel-slide>

        <b-carousel-slide class="item-carousel">
          <template v-slot:img>
            <img
              class="d-block img-fluid w-100"
              width="1024"
              height="480"
              src="../assets/img/img-carousel/image1.jpg"
              alt="image slot"
            />
          </template>
        </b-carousel-slide>

        <b-carousel-slide class="item-carousel">
          <template v-slot:img>
            <img
              class="d-block img-fluid w-100"
              width="1024"
              height="480"
              src="../assets/img/img-carousel/image3.jpg"
              alt="image slot"
            />
          </template>
        </b-carousel-slide>

        <!-- <b-carousel-slide
          caption="Blank Image"
          img-blank
          img-alt="Blank image"
          class="item-carousel"
        >
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eros felis, tincidunt
            a tincidunt eget, convallis vel est. Ut pellentesque ut lacus vel interdum.
          </p>
        </b-carousel-slide>-->
      </b-carousel>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      sliding: null,
    };
  },
  props: {
    scrollScreenHeader: Boolean,
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true;
    },
    onSlideEnd(slide) {
      this.sliding = false;
    },
  },
};
</script>

<style lang="scss" >
.slide-image {
  &.scroll {
    padding-top: 102px;
  }
}

.carousel-class {
  height: 650px;
}

.item-carousel {
  height: 650px;
}
</style>