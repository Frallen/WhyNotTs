<template>

  <div>
    <Error v-if="isError"></Error>
    <div v-else>
      <Navigation></Navigation>
      <router-view v-slot="{ Component }">
        <suspense>
          <component :is="Component"/>
        </suspense>
      </router-view>
    </div>
  </div>

</template>
<script setup lang="ts">
const {isError} = storeToRefs(useMain())

</script>
<style lang="less">

</style>
