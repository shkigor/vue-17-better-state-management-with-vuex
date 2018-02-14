<template>
  <div>
    <p>Counter is: {{ doubleCounter }}</p>
    <p>Number of Clicks: {{ stringCounter }}</p>
  </div>
</template>

<script>
  import { mapGetters } from 'vuex';
  import * as types from '../store/types';

  export default {
    computed: {
      ...mapGetters(
        // [ 'doubleCounter', 'stringCounter' ]
        // we can also pass an Object and map the Getters to different Names
        {
          doubleCounter: types.DOUBLE_COUNTER,
          stringCounter: types.CLICK_COUNTER
        })
    }
  }
</script>
