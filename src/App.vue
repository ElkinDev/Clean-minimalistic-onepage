<template>
  <div id="app">
      <headerc/>

    <div class="content">
     <router-view/>
    </div>

 
    <footerc/>

  </div>
</template>


<script>
import headerc from '@/components/header.vue'
import footerc from '@/components/footer.vue'

export default {
    components: {
      headerc,
      footerc,
    }
}
</script>

<style>

</style>
