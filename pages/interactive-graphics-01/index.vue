<template>
  <div class="container dark" :class="pageTitle">
    <div class="bg bg-full overlay">
      <iframe :src="'https://editor.p5js.org/sarahriazati/embed/' + bgSketchId" :width="bgSketchWidth" :height="bgSketchHeight"></iframe>
    </div>
  
    <main class="light">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. In nec mattis lectus. Nunc fermentum mi nisl, in dictum lacus faucibus nec. Cras scelerisque fringilla eros. Mauris dignissim vitae ex sit amet pretium. Duis faucibus ultricies lacus eu mattis. Donec risus elit, venenatis mollis elit eu, facilisis ullamcorper sem. Duis vel elit lacinia, pretium magna et, lobortis quam. Suspendisse tincidunt dui elit, eget maximus libero finibus non. Praesent vitae malesuada augue. Cras ipsum tellus, lacinia tristique condimentum sed, dictum et libero. Donec venenatis tincidunt interdum.</p>
      <p>Fusce convallis pharetra velit, a suscipit elit sollicitudin sit amet. Duis ac pretium erat. Etiam suscipit malesuada elit sed pellentesque. Pellentesque eu pellentesque mi, vel sagittis quam. Nam mattis in justo id porta. Curabitur urna lacus, mattis sed efficitur id, faucibus a arcu. Aenean ac egestas orci. Etiam eget suscipit enim. Vivamus at ante sed risus finibus vehicula ac in nunc. Pellentesque eu felis eu eros dictum auctor in ut enim. Morbi mattis blandit finibus. Quisque sed vestibulum est. Proin ut diam a ipsum feugiat hendrerit in facilisis orci.</p>
    </main>
  
  </div>

</template>

<script>

export default {
  layout: 'courses',

  head () {
    return {
      title: `Home | Interactive Graphics Summer 2020`,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        { hid: 'description', name: 'description', content: 'My custom description' }
      ]
    }
  },
  data() {
    return {
      pageTitle: 'Home',
      bgSketchId: '', //Ai5TqjjqV
      bgSketchWidth: 720,
      bgSketchHeight: 720
    }
  }
}
</script>

<style lang="scss">

$dark: #000;
$light: #fff;
$green: #69e642;
$highlight: $green;
$width: 720px;
$spacer: 15px;


// home layout
.Home {
background: rgb(102,122,255);
background: linear-gradient(180deg, rgba(102,122,255,1) 0%, rgba(231,133,231,1) 100%);

  display: grid;
  grid-template-columns: 1fr $width 1fr;
  grid-template-rows: $width/6 $width/6 $width/6 ($width/6)*3 auto;

  .bg {
    grid-row: 1 / 5;
    grid-column: 2 / 3;
    z-index: 0;
  }



  header {
    width: 100%;
    align-self: start;
    padding: $spacer*2;
    grid-row: 2 / 4;
    grid-column: 1 / 4;
    z-index: 10;
  }


  main {
    grid-row-start: 4;
    grid-column: 1 / 4;
    z-index: 10;
    max-width: $width;
    max-height: $width;
    margin: 0 auto;
    @media only screen and (max-width: $width) {
      max-width: 100%;
    }
  }

  footer {
    grid-column: 1 / 4;
    grid-row-end: 6;
    align-self: end;
    justify-self: center;
    padding: $spacer*2;
  }

}

</style>