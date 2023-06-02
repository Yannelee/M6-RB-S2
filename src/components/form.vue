<template>
  <div>
    <h1>Ingresa tus Datos</h1>
    <input type="text" v-model="nombre" placeholder="Nombre">
    <input type="text" v-model="apellido" placeholder="Apellido">
    <input type="text" v-model="correo" placeholder="Correo">
    <button @click="sendForm">Enviar</button>

    <h1>Ingresa tu edad en años</h1>
    <input type="number" v-model="edad" placeholder="Edad">
    <h2 v-if="edad===''"></h2>
    <h2 v-else-if="edad<13">Niñez</h2>
    <h2 v-else-if="edad<17">Adolescencia</h2>
    <h2 v-else-if="edad<35">Adulto Joven</h2>
    <h2 v-else-if="edad<64">Adulto</h2>
    <h2 v-else>Tercera Edad</h2>
  </div>
</template>

<script>
export default {
  name: 'uno-component',
  data: function(){
    return{
      nombre:'',
      apellido:'', 
      correo:'',
      edad:'',
    }
  },
  methods:{
    sendForm(){
      alert(`Saludos ${this.nombre} ${this.apellido}, tu correo es: ${this.correo}`)
    }
  }
}
</script>

<style>
input{
  width: 25%;
  margin: .5rem;
}
button{
  display: block;
  margin: auto;
}

</style>