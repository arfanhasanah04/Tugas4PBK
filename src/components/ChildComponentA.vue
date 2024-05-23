<template>
    <div class="child-component">
      <button class="send-button" @click="sendDataToParent">Kirim Data dari A</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ChildComponentA',
    methods: {
      sendDataToParent() {
        this.$emit('data-from-a', 'Data dari Komponen A');
      }
    }
  };
  </script>
  
  <style scoped>
  .child-component {
    margin: 10px;
    padding: 15px;
    background-color: #ffefd5;
    border-radius: 8px;
    text-align: center;
  }
  
  .send-button {
    padding: 10px 20px;
    background-color: #ff6347;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  .send-button:hover {
    background-color: #ff4500;
  }
  </style>
  