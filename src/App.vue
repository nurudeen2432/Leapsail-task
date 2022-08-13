<template>
  <div class="app">
    <Router-view/>

 

   <Header/>


    <Modal/>


    
      

 
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";

import Header from "./components/Header.vue";

export default {
  name: "App",
  components: { Modal, Header },

  data() {
    return {
     
    };
  },
  methods: {
   
    },
   
  
};
</script>

<style >

@import './assets/bootstrap.min.css';

@import './assets/font-awesome-4.7.0/css/font-awesome.min.css';

body{
  font-family:  'Roboto', sans-serif;
  color: #000000;
  box-sizing: border-box;
  width: 100%;


}
a{
  color:#333;
text-decoration: none;

}


a:hover{
  color:rgb(189, 189, 145);
  
}

</style>
