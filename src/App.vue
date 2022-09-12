<!-- <template>
  <div class="firstattempt">

    <h1>{{title}}</h1>
    <input type="text" ref="name">
   
    <button @click="handleClick">CLICK ME</button> 
    <p>Welcome...</p>
   
    <div v-if="showModal">
      <Modal :header="header" :text="text" theme="sale" @close="toggleModal"/>
    </div>
    <button @click.alt="toggleModal">OPEN MODAL (alt)</button>
  </div>
  
</template>

<script>

import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: { Modal },
  data() {
    return {
      title: "My First Vue App :)", 
      header: "Sign up for the Giveaway!",
      text:"Something silly", 
      showModal: false
    }
  },
  methods: {
handleClick() {
  console.log(this.$refs.name)
  this.$refs.name.classList.add('active')
  this.$refs.name.focus()
}, 
toggleModal() {
  this.showModal = !this.showModal
}
  }
  
}
</script>

********************************************************* -->

<template>
  <div class="firstattempt">

    <h1>{{title}}</h1>
    <input type="text" ref="name">
   
    <button @click="handleClick">CLICK ME</button> 
    <p>Welcome...</p>
   
    <div v-if="showModal">
      <Modal :header="header" :text="text" theme="sale" @close="toggleModal"/>
    </div>
    <button @click.alt="toggleModal">OPEN MODAL (alt)</button>
  </div>
  
</template>

<script>

import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components: { Modal },
  data() {
    return {
      title: "My First Vue App :)", 
      header: "Sign up for the Giveaway!",
      text:"Something silly", 
      showModal: false
    }
  },
  methods: {
handleClick() {
  console.log(this.$refs.name)
  this.$refs.name.classList.add('active')
  this.$refs.name.focus()
}, 
toggleModal() {
  this.showModal = !this.showModal
}
  }
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.firstattempt {
  border: 2px solid blue;
  padding: 10px
}
h1 {
  border-bottom: 1px solid #ddd;
  display: block;
  padding-bottom: 10px;

}
</style>
