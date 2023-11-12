<template>

  <h1>Lista de Compras</h1>
<div class="list">
  <shopping_list class="list-content"
    v-for="(item, index) in shopping.length"
    :key="item.name"
    :index="index"
    :required="item.required"
    :names-array="shopping.map(a => a.name)"
  />
</div>
</template>

<script>
import shopping_list from './components/list.vue'

export default {
name: 'list_array',

components: {
  shopping_list
},

data () {
  return {
    shopping: [
      {
        name: 'Platano Chiapas',
        required: 1,
        
      },
      {
        name: 'Huevos Verdes',
        required: 3,
        
      },
      {
        name: 'Jamon',
        required: 1,
        
      }
    ]
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

  display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	padding: 0.1rem;
	background-color: #FFF;
	border-radius: 0.5rem;
	box-shadow: var(--shadow);
	cursor: pointer;
}

:root {
	--primary: #150b49;
	--business: #3A82EE;
	--personal: var(--primary);
	--light: #EEE;
	--grey: #888;
	--dark: #313154;
	--danger: #ff5b57;

	--shadow: 0 1px 3px rgba(0, 0, 0, 0.1);

	--business-glow: 0px 0px 4px rgba(58, 130, 238, 0.75);
	--personal-glow: 0px 0px 4px rgba(5, 107, 31, 0.589);
}
.list{
    display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	padding: 1rem;
	background-color: var(--business);
	border-radius: 0.8rem;
	box-shadow: var(--shadow);
	cursor: pointer;
}
.list .list-content{
  color: var(--dark);
	font-size: 1rem;
	font-weight: 400;
	margin-bottom: 0.1rem;
}

h1 {
	color: var(--dark);
	font-size: 1.8rem;
	font-weight: 400;
	margin-bottom: 0.5rem;
}
</style>
