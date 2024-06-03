<template>
  <div class="container mt-5 pb-5" style="background-color: #f0f0f0;">
    <h1 class="mb-4 text-primary">Preguntas de Opción Múltiple</h1>
    
    <div class="card mb-4">
      <div class="card-body">
        <p class="mb-1 font-weight-bold">Pregunta 1/3</p>
        <p class="mb-3">¿Cómo es la forma reducida de v-on:click?</p>
        <ul class="list-group mb-0">
          <li class="list-group-item bg-light border-0">a) v-on@click</li>
          <li class="list-group-item bg-light border-0">b) #click</li>
          <li class="list-group-item bg-light border-0">c) @click <span class="text-success font-weight-bold">(Respuesta Correcta)</span></li>
          <li class="list-group-item bg-light border-0">d) :click</li>
          <li class="list-group-item bg-light border-0">e) v-bind#click</li>
        </ul>
      </div>
    </div>

    <div class="card mb-4">
      <div class="card-body">
        <p class="mb-1 font-weight-bold">Pregunta 2/3</p>
        <p class="mb-3">El modificador trim recorta...</p>
        <ul class="list-group mb-0">
          <li class="list-group-item bg-light border-0">a) Los espacios puestos adelante en una entrada de texto</li>
          <li class="list-group-item bg-light border-0">b) Los espacios puestos atrás en una entrada de texto</li>
          <li class="list-group-item bg-light border-0">c) Los espacios adelante y atrás en una entrada de texto <span class="text-success font-weight-bold">(Respuesta Correcta)</span></li>
          <li class="list-group-item bg-light border-0">d) Saca los espacios intermedios puestos en una entrada de texto</li>
        </ul>
      </div>
    </div>

    <div class="card">
      <div class="card-body">
        <p class="mb-1 font-weight-bold">Pregunta 3/3</p>
        <p class="mb-3">La propiedad routes en la definición del router de Vue.js tiene como función:</p>
        <ul class="list-group mb-0">
          <li class="list-group-item bg-light border-0">a) Definir el path y el componente activo para esa ruta <span class="text-success font-weight-bold">(Respuesta Correcta)</span></li>
          <li class="list-group-item bg-light border-0">b) Define la barra de navegación a utilizar</li>
          <li class="list-group-item bg-light border-0">c) Define sólo todos los componentes activos en el router</li>
          <li class="list-group-item bg-light border-0">d) Definir el modo de trabajo de las rutas</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MultipleChoiceView'
};
</script>

<style scoped>
/* Estilos específicos para esta vista */

.card {
  border: 2px solid #007bff;
  border-radius: 10px;
}

.card-body {
  background-color: #f8f9fa;
}

.list-group-item {
  background-color: #e9ecef;
}

.text-success {
  color: #28a745;
}

.font-weight-bold {
  font-weight: bold;
}
</style>
