<template>
  <header class="header">
    <h1 v-if="$slots.title"
        class="title">
        <slot name="title" />
    </h1>
    <div v-if="$slots.description"
            class="description">
        <slot name="description" />
    </div>
    <div class="content">
        <slot/>
    </div>
</header>
</template>

<script>

export default {

  mounted(){
    console.log(this.$el);
    console.log(this.$slots);
  },  

  methods: {
  }
};
</script>

<style>
.header {
  background-color: blueviolet;
  color: #fff;
}
</style>