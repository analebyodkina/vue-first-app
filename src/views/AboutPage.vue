<template>
  <div>
    <h1>aboutttt</h1>
    <p>Welcome to aboutpage </p>
    
    <button v-on:click="toggleClass">Click</button>

    <div class="item" :class="{ 'active': isActive }"></div>

    <div class="pink" v-if="isActive"></div>

      {/* :style="{width: width}" */}
  </div>
</template>


<script>
export default {
  name: 'AboutPage',
  data() {
    return {
        isActive: false,
    };
  },
  methods: {
    toggleClass() {
      this.isActive = !this.isActive;
    },
  },
};
</script>