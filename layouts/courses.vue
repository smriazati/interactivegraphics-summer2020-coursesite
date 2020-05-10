<template>
  <div>
    <SiteHeader />
      <nuxt />
    <SiteFooter />
  </div>
</template>

<script>
import SiteHeader from '~/components/SiteHeader.vue'
import SiteFooter from '~/components/SiteFooter.vue'

export default {
  components: {
    SiteHeader,
    SiteFooter
  }

}
</script>



<style lang="scss">
$dark: #000;

@import url("https://use.typekit.net/ouk1trd.css");

$dark: #000;
$light: #fff;
$green: #69e642;
$purple: #667aff;
$highlight: $purple;
$width: 720px;
$spacer: 15px;

::selection {
  background: $green;
  color: $light;
}
* {
  box-sizing: border-box;
  margin: 0;
  border: 0;
  outline: none;
  transition: .3s ease all;
}
html,body {
  width: 100%;
  min-height: 100%;
  min-height: 100vh;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

iframe {
  background: $light;
}

.container {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center; 
  min-height: 100%;
  min-height: 100vh;
  .bg-full {
    position: relative;
    overflow: hidden;
    > iframe {
      width: $width;
      height: $width;
      max-width: $width;
      max-height: $width;
      @media only screen and (max-width: $width) {
        max-width: 100%;
      }
    }


    &.overlay:after {
      display: block;
      position: absolute;
      background: rgba(0,0,0,.8);
      width: 100%;
      max-width: 100%;
      height: 100%;
      top: 0;
      content: '';
    }
  }
  
  main {
    margin-top: $spacer*2;
    padding: $spacer*2;
    p {
      margin-bottom: $spacer;
      &:last-child {
        margin-bottom: 0;
      }
    }

    iframe {
      overflow-y: scroll;
    }
  }

}

.dark {
  background: $dark;
  color: $light;
}


.light {
  background: $light;
  color: $dark;
}
header {
  width: 100%;
  margin: 0 auto;
  text-align: center;

  .Home & {
    h1 {
      font-size: 3rem;
    }
  }

  h1 {
    font-size: 1rem;
    margin-bottom: $spacer;
  }

  nav {
    ul {
      display: flex;
      flex-wrap: wrap;
      list-style: none;
      justify-content: space-between;
    } 
  }
}
 

// type

html {
  font-size: 18px;
}
body {
  font-family: trade-gothic-next, sans-serif;
} 

a {
  text-decoration: none;
  color: $highlight;
  padding: $spacer;
  display: block;
  &:hover {
    background: $highlight;
    color: $light;
  }

  nav & {
    text-transform: uppercase;
    font-weight: 700;
    letter-spacing: 0.05em;
    font-size: 2rem;
  }
}


h1, h2, h3, h4, h5, h6 {
  font-size: 1rem;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}
</style>
