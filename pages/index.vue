<template>
<v-app>
 <v-parallax src="pig/abc.jpg">
  <div>
    <CENTER> 
       <div>
    <br>
    <br>  
    <br> 
    <br> 
    <br> 
    <br> 
        <br>  
    <br> 
    <br> 
    <br>     <br>  
    <br> 
    <br> 
    <br>     <br>  
    <br> 
    <br> 
    <br>     <br>  
    <br> 
    <br> 
    <br> 
    <a href ="http://localhost:3000/#/table" target = "_blank" ><v-btn color="blue darken-2">เข้าสู่รายการ</v-btn></a><br>
    <nuxt-link to="/seaech"><v-btn color="blue darken-2">ค้าหา</v-btn></nuxt-link><br>
        <nuxt-link to="/login"><v-btn color="blue darken-2">login</v-btn></nuxt-link><br> 
        
    <br> t
    
  23  <br> 
    <br> 
    <br> 
  </div>
   </CENTER></div>
   </v-parallax>
  <v-footer class="red lighten-1">
    <v-spacer></v-spacer>
    <div>&copy; {{ new Date().getFullYear() }}</div>
  </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      id: 1
    };
  }
};
</script>
