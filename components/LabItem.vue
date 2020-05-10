<template>
 <section :class="isCollapsed ? 'collapsed' : 'expanded' ">
    <div class="collapse-area">
      <h2 class="lab-title"> {{ labData.name }} </h2>
<!--       <a @click="expandAccordion">Open lab</a>
 -->    </div>
    <div class="expand-area">

      <div v-if="labData.mission">
        <h3> Mission: {{ labData.mission }} </h3>
      </div>

      <div v-if="labData.labVideo" class="lab-video">
        <a :href="labData.courseVideo" target="_blank">Course video with Sarah</a></p>
      </div>

      <div v-if="labData.tutorials" class="tutorials">
        <h3>Tutorials</h3>
        <ul v-for="item in labData.tutorials"> 
          <li>
            <a :href="item.link">
              <p>{{ item.name }}</p>
              <p>{{ item.series }}</p>
              <p v-if="item.notes" class="small">{{ item.notes }}</p>
            </a>
          </li>
        </ul>
     </div>

      <div v-if="labData.quizzes" class="quizzes">
        <h3>Quiz</h3>
        <ul v-for="item in labData.quizzes"> 
          <li>
            <a :href="item.link">
              <p>{{ item.name }}</p>
              <p><strong>Due: {{ item.due }}</strong></p>
              <p v-if="item.notes" class="small">{{ item.notes }}</p>
            </a>
          </li>
        </ul>        
      </div>

      <div v-if="labData.response" class="responses">
        <h3>Reflection</h3>
      </div>


      <div v-if="labData.sketch" class="sketch">
        <h4>Sketch</h4>
        <p>{{ labData.sketch.name }}</p>
        <p><strong>Due: {{ labData.sketch.due }}</strong>{</p>
        <div v-html="labData.sketch.instructions"></div>        
      </div>

     

    </div>
 </section>

</template>


<script>
  export default {
    props: {
      labData: Object
    },
    data() {
      return {
        isCollapsed: false,
      }
    },
    methods: {
      expandAccordion: function(event) {
          this.isCollapsed != this.isCollapsed;

      }
    }
  }
</script>
<style lang="scss" scoped>
$spacer: 15px;
section {
  &.collapsed {
    .expand-area {
      display: none;
    }
  }
  &.expanded {
    .expand-area {
      display: flex;
      flex-direction: column;
      ul {
        list-style: none;
      }
    }
  }
}

.collapse-area {
  padding: $spacer*2 0;
}

h2.lab-title {
  font-size: 3rem;
}

.expand-area {
  > * {
    display: flex;
    margin: $spacer*2 0;
    padding: $spacer*2;
    background: #eaeaea;
  }
}

</style>
