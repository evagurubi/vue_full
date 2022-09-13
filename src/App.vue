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
  

    <h1>{{title}}</h1>
    <input type="text" ref="name">
   
    <button @click="handleClick">CLICK ME</button> 
    <p>Welcome...</p>
   
    <div v-if="showModal">
      <Modal theme="sale" @close="toggleModal">
      <!-- slots pass templates to components so they're not a replacement for props -->
      <template v-slot:links>
        <a href="#">sign up now</a>
        <a href="#">more info</a>
      </template>
      <h1>Modal Title</h1>
      <p>Additional remarks</p>
      </Modal>
    </div>
    <div v-if="showModalTwo">
      <Modal @close="toggleModalTwo">
      <!-- slots pass templates to components so they're not a replacement for props -->
      <template v-slot:links>
        <a href="#">sign up now 2</a>
        <a href="#">more info 2</a>
      </template>
      <h1>Modal Two Title</h1>
      <p>Additional remarks for Modal Two</p>
      </Modal>
    </div>
    <button @click.alt="toggleModal">OPEN MODAL (alt)</button>
    <br/>
    <button @click="toggleModalTwo">OPEN MODAL TWO</button>
  
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
      showModal: false, 
      showModalTwo: false,
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
},
toggleModalTwo() {
  this.showModalTwo = !this.showModalTwo
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
