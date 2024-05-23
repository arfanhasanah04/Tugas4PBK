<template>
    <div class="child-component">
      <button class="send-button" @click="sendDataToParent">Kirim Data dari B</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ChildComponentB',
    methods: {
      sendDataToParent() {
        this.$emit('data-from-b', 'Data dari Komponen B');
      }
    }
  };
  </script>
  
  <style scoped>
  .child-component {
    margin: 10px;
    padding: 15px;
    background-color: #e0ffff;
    border-radius: 8px;
    text-align: center;
  }
  
  .send-button {
    padding: 10px 20px;
    background-color: #20b2aa;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .send-button:hover {
    background-color: #008b8b;
  }
  </style>
  