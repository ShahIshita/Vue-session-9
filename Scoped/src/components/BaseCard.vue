<template>
    <div>
        <header v-if="$slots.header">
            <slot name="header">
                <!-- <h2>Default </h2> -->
            </slot>
        </header>
    <slot></slot>
    </div>
</template>


<script>


export default {
   mounted() {
       console.log(this.$slots.header);
   }
};
</script>


<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: rgb(248, 248, 248);
}
div {
  margin: 2rem auto;
  max-width: 30rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(241, 223, 223, 0.26);
  padding: 1rem;
  
}
</style>