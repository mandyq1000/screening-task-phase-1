<template>
<v-app>

    <navbar></navbar>
  
     <router-view></router-view>
     
</v-app>
</template>

  <script>
  import navbar from '@/components/navbar'
   

  export default {
  components: { navbar, 
                }
  }
  </script>
