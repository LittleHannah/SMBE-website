<template>
  <div class="container" style="padding: 2rem">
    <h1>PLENARY SPEAKERS</h1>
    <hr class="hr">
    <div class="card mb-3" style="height: 300px;margin-bottom: 2rem" v-for="s in speakers" v-bind:key="s.name">
      <div class="row g-0">
        <div class="col-md-3">
          <img :src="s.img" class="img-fluid rounded-start" alt="..." style="height: 300px;width: 240px">
        </div>
        <div class="col-md-9">
          <div class="card-body">
            <h5 class="card-title" style="font-size: 2rem;font-weight: 650">{{ s.name }}</h5>
            <p class="card-text" style="font-size: 1.2rem">{{s.description}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ConfSpeakers',
  data() {
    return {
      speakers: [
        {name: "Jonathan Pritchard", img: require('@/assets/img/speakers/2.jpg'), description:"Jonathan Karl Pritchard is an English-born professor of genetics at Stanford University, best known for his development of the STRUCTURE algorithm for studying population structure and his work on human genetic variation and evolution. His research interests lie in the study of human evolution, in particular in understanding the association between genetic variation among human individuals and human traits.", affiliation: ""},
        {name: "Qiaomei Fu", img: require('@/assets/img/speakers/1.jpg'), description:"QIAOMEI FU is a Chinese researcher at Institute of Vertebrate Paleontology and Paleoanthropology, Chinese Academy of Sciences. She is mainly engaged in the research of evolutionary heredity and population heredity, with a focus on the direction of \"human palaeogenomics research\". Due to her remarkable achievements, she was named one of the \"Top Ten Stars of Science in China\" by Nature, one of the \"Innovative Figures of Science and Technology in China\" by CCTV, selected as a Young corresponding academician of the Academy of Sciences for Developing Countries (TWAS).", affiliation: ""}
      ]
    }
  }
}
</script>

<style scoped>
@import "@/scss/blog.css";
.bd-placeholder-img {
  font-size: 1.125rem;
  text-anchor: middle;
  -webkit-user-select: none;
  -moz-user-select: none;
  user-select: none;
}

@media (min-width: 768px) {
  .bd-placeholder-img-lg {
    font-size: 3.5rem;
  }
}

.b-example-divider {
  width: 100%;
  height: 3rem;
  background-color: rgba(0, 0, 0, .1);
  border: solid rgba(0, 0, 0, .15);
  border-width: 1px 0;
  box-shadow: inset 0 .5em 1.5em rgba(0, 0, 0, .1), inset 0 .125em .5em rgba(0, 0, 0, .15);
}

.b-example-vr {
  flex-shrink: 0;
  width: 1.5rem;
  height: 100vh;
}

.bi {
  vertical-align: -.125em;
  fill: currentColor;
}

.nav-scroller {
  position: relative;
  z-index: 2;
  height: 2.75rem;
  overflow-y: hidden;
}

.nav-scroller .nav {
  display: flex;
  flex-wrap: nowrap;
  padding-bottom: 1rem;
  margin-top: -1px;
  overflow-x: auto;
  text-align: center;
  white-space: nowrap;
  -webkit-overflow-scrolling: touch;
}

.btn-bd-primary {
  --bd-violet-bg: #712cf9;
  --bd-violet-rgb: 112.520718, 44.062154, 249.437846;

  --bs-btn-font-weight: 600;
  --bs-btn-color: var(--bs-white);
  --bs-btn-bg: var(--bd-violet-bg);
  --bs-btn-border-color: var(--bd-violet-bg);
  --bs-btn-hover-color: var(--bs-white);
  --bs-btn-hover-bg: #6528e0;
  --bs-btn-hover-border-color: #6528e0;
  --bs-btn-focus-shadow-rgb: var(--bd-violet-rgb);
  --bs-btn-active-color: var(--bs-btn-hover-color);
  --bs-btn-active-bg: #5a23c8;
  --bs-btn-active-border-color: #5a23c8;
}
.bd-mode-toggle {
  z-index: 1500;
}
</style>
