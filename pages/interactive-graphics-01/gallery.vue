<template>
  <div class="container dark" :class="pageTitle">

  	<div class="page-title">
  		<h1>{{ pageTitle }}</h1>
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
      title: `Gallery | Interactive Graphics Summer 2020`,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        { hid: 'description', name: 'description', content: 'My custom description' }
      ]
    }
  },
  data() {
    return {
      pageTitle: 'Gallery',
      bgSketchId: '', //Ai5TqjjqV
      bgSketchWidth: 0,
      bgSketchHeight: 0
    }
  }
}

</script>


<style lang="scss">


	
</style>