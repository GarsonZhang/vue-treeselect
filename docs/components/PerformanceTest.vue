<template>
<div>
  
  <treeselect :options="gzoptions" v-model="value" unknownText="(没有找到)" :multiple="false" />
  <treeselect :options="options" :multiple="true" />

  </div>
</template>

<script>
  import { generateOptions } from './utils'

  export default {
    data: () => ({
      options: generateOptions(1, 500),
       value: '',
        // define options
        gzoptions: [ {
          id: 'a',
          label: 'a',
          children: [ {
            id: 'aa',
            label: 'aa',
          }, {
            id: 'ab',
            label: 'ab',
          } ],
        }, {
          id: 'b',
          label: 'b',
        }, {
          id: 'c',
          label: 'c',
        } ],
    }),
  }
</script>
