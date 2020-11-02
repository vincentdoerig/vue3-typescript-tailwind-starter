<template>
  <div class="prose max-w-none">
    <h1>{{ msg }}</h1>
    <span class="inline-flex rounded-md shadow-sm">
      <button
        type="button"
        class="inline-flex items-center px-4 py-2 text-sm font-medium leading-5 text-white transition duration-150 ease-in-out bg-red-600 border border-transparent rounded-md hover:bg-red-500 focus:outline-none focus:border-red-700 focus:shadow-outline-red active:bg-red-700"
        @click="count++"
      >
        you clicked me {{ count }} times
      </button>
    </span>
    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Molestiae beatae velit aliquam reiciendis. Tenetur veritatis rem, minima magni amet aut sit adipisci ab minus fuga error dolores accusantium quia assumenda officia ratione sapiente provident voluptatem reiciendis deleniti nam! Voluptas quia quasi totam architecto molestias ullam veritatis necessitatibus fugit placeat repudiandae, soluta eos assumenda minima id debitis, praesentium itaque beatae! Deserunt ad cumque autem unde enim, perspiciatis distinctio consectetur, doloremque sit earum veniam debitis et magnam obcaecati. Mollitia voluptates ea expedita distinctio eaque consequatur quae, consequuntur, provident quos veniam libero est culpa saepe ex dolorem laborum quam, quasi illo! Veniam, necessitatibus.</p>
  </div>
</template>

<script lang="ts">
import { defineComponent, toRef } from 'vue'
import { globalState } from '../store'

export default defineComponent({
  props: {
    msg: {
      type: String,
      default: '',
    },
  },

  setup() {
    return {
      count: toRef(globalState, 'count'),
    }
  },
})
</script>
