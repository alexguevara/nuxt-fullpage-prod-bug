<template>
  <full-page
    id="fullpage"
    ref="fullpage"
    class="fullPage"
    :options="options">
    <section class="section-one section" data-tooltip="home" data-anchor="home">
      <div class="wrapper">
        <h1>Section 1</h1>
        <button class="btn" @click="updateIndex">
            Button
        </button>
        <br>
        <div class="index">
          {{ slideIndex }}
        </div>
      </div>
    </section>
    <section class="section-slides section" data-tooltip="slides" data-anchor="slides">
      <div class="slide">
        <h2 class="text-center">Slide 1</h2>
      </div>
	    <div class="slide">
        <h2 class="text-center">Slide 2</h2>
      </div>
	    <div class="slide">
        <h2 class="text-center">Slide 3</h2>
      </div>
	    <div class="slide">
        <h2 class="text-center">Slide 4</h2>
      </div>
    </section>
  </full-page>
</template>

<script>

export default {
  data () {
    return {
      slideIndex: 0,
      options: {
        licenseKey: 'OPEN-SOURCE-GPLV3-LICENSE',
      }
    }
  },
  methods: {
    updateIndex () {
      this.slideIndex = this.slideIndex +1;
    }
  }
}
</script>

<style>
  .fullPage {
    display: block;
  }
  .section {
    text-align: center;
  }
  .section-one{
    background-color: #f2f2f2;
  }
  .slide {
    background-color: #4BBFC3;
  }
  .wrapper {
    padding: 50px;
    border: 1px solid black;
    display: inline-block;
  }
</style>
