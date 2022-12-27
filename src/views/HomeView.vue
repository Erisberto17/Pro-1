
<template>
  <main>
    <Nav/>
    <Dashboard/>
    <Plusbutton/>
  </main>
</template>
<script>
 import Nav from "../components/nav.vue"
 import Dashboard from "../components/Dashboard.vue"
 import Plusbutton from "../components/Plusbutton.vue"
 
export default {
  name:"HomeView",
  components:{
    Nav,
    Dashboard,
    Plusbutton
  }
}
</script>