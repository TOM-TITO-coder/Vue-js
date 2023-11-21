
<template>
  <div class="container" style="display: flex; flex-direction: column;">
    <div class="header">Header</div>
    <div class="border-wrap" style="display: flex; gap: 10px;">
      <div class="side-1" style="width: 50%; text-align: center;">1</div>
      <div class="side-2" style="display: flex; flex-direction: column; width: 50%; text-align: center;">
        <RouterLink :to="{name: 'page1'}" class="com">2</RouterLink>
        <RouterLink to="/profile" class="com">3</RouterLink>
        <div class="com" @click="navigateTo('/about')">4</div>
      </div>
    </div>
  </div>
</template>

<script>
   export default {
    methods: {
      navigateTo(to){
        this.$router.push(to)
      }
    }
   }
</script>

<style>
.container {
  height: 500px;
  width: 500px;
}

.header {
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid black;
  height: 50px;
  margin: 10px;
}

.side-1 {
  margin: 10px;
  border: 1px solid black;
}

.com {
  margin: 10px;
  border: 1px solid black;
  height: 100%;
  padding: 5px;
}


</style>