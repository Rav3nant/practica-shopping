<template>
    <div class="list">
      <div class="list content">Indice: {{ index }}</div>
      <div class="list content">Producto: {{ namesArray[index] }}</div>
    </div>
  </template>
  
  <script>
  export default {
    name: "shopping_list",
    props: ["names-array", "required", "index"]
  };
  </script>