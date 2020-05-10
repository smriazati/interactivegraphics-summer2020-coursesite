<template>
  <div class="container dark" :class="pageTitle">

  	<div class="page-title">
  		<h1>{{ pageTitle }}</h1>
  	</div>

    <main class="light">
      <iframe src="https://docs.google.com/document/d/e/2PACX-1vR_BDbAMtkHwpjrLSyhejeFv7eobLAaAha0MsZF5LVc_7RrDnod0XY2B9yHerPH4boAiMsqBCwef85b/pub?embedded=true" width="1000" height="720"></iframe>
    </main>
  
  </div>

</template>

<script>
	
export default {
  layout: 'courses',

 head () {
    return {
      title: `Syllabus | Interactive Graphics Summer 2020`,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        { hid: 'description', name: 'description', content: 'My custom description' }
      ]
    }
  },
  data() {
    return {
      pageTitle: 'Syllabus',
      bgSketchId: '', //Ai5TqjjqV
      bgSketchWidth: 0,
      bgSketchHeight: 0
    }
  }
}

</script>


<style lang="scss">


	
</style>