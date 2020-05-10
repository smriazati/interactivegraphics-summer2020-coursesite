<template>
  <div class="container" :class="pageTitle">

  	<div class="page-title">
  		<h1>{{ pageTitle }}</h1>
  	</div>

    <div class="lab-grid">
      <div class="lab-item" v-for="item in labs">
        <LabItem :lab-data="item" />
      </div> 
    </div>

  
  </div>

</template>

<script>

import LabItem from '~/components/LabItem.vue'

export default {
  layout: 'courses',


 head () {
    return {
      title: `Labs | Interactive Graphics Summer 2020`,
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        { hid: 'description', name: 'description', content: 'My custom description' }
      ]
    }
  },
  data() {
    return {
      pageTitle: 'Labs',
      labs: {
        lab0: {
          name: 'Lab 0 - Onboarding',
          mission: 'Misison here',
          courseVideo: 'link',
          quizzes: {
            quiz1: {
              name: 'quiz1',
              link: 'link',
              due: 'date',
              notes: 'notes'
            },
            quiz2: {
              name: 'quiz2',
              due: 'date',
              link: 'link',
              notes: 'notes'
            }
          }
        },
        lab1: {
          name: 'Lab 1 - Drawing with Code',
          mission: 'Misison here',
          courseVideo: 'link',
          quizzes: {
            quiz1: {
              name: 'quiz1',
              link: 'link',
              due: 'date',
              notes: 'notes'
            },
            quiz2: {
              name: 'quiz2',
              due: 'date',
              link: 'link',
            }
          },
          tutorials: {
            tutorial1: {
              name: 'Introduction, 1.1 - 1.2',
              series: 'Code! Programming with p5.js',
              link: 'link'
            },
            tutorial2: {
              name: 'Drawing, 1.3 - 1.6',
              series: 'Code! Programming with p5.js',
              link: 'link'
            }
          },
          sketch: {
            name: 'Drawing with Algorithms',
            due: 'date',
            instructions: `<p>Part 1: Inspired by Sol Lewitt’s wall drawing series, write an algorithm for drawing. Give your algorithm a name using camelCase, and post your instructions to Piazza.</p> 
              <p>Part 2: Pick at least 3 of your classmates’ algorithms & create drawings according to the instructions. Your drawings can be on paper, or you can use a digital software tool to create them. Take a picture of each of your drawings & post them in reply to the original algorithm post. Include a brief summary of your experience following the algorithm’s instructions. `
          }
        }
      }
    }
  },
  components: {
    LabItem
  }
}

</script>


<style lang="scss" scoped >
$spacer: 15px;

.container {
  padding-top: $spacer*4;
}

.Labs h1 {
  font-size: 3rem;
  margin-bottom: $spacer*2;
}

.lab-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  width: 70vw;
  @media only screen and (max-width: 800px) {
    width: 90vw;
  }
  > * {
  background: #eaeaea;
    flex: 1 0 100%;
    //border: 1px solid #000;
    margin: $spacer*2 0;
    padding: $spacer*2;
  }
}
	
</style>