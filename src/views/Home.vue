<template>
  <form >
    <input type="text"
    class="form-control mt-2"
    placeholder="Nombre"
    v-model="tarea.nombre">

    <div class="my-2">
      <div class="form-group form-check-inline">
        <input type="checkbox" class="form-check-input" id="check-1" value="JavaScript" v-model="tarea.categories">
        <label class="form-check-label" for="check-1">JavaScript</label>
      </div>
      <div class="form-group form-check-inline">
        <input type="checkbox" class="form-check-input" id="check-2" value="Desarrollo" v-model="tarea.categories">
        <label class="form-check-label" for="check-2">Desarrollo Web</label>
      </div>
    </div>

    <div class="my-2">
      <div class="form-check form-check-inline">
        <input 
          class="form-check-input" 
          type="radio" 
          id="inlineRadio1" 
          value="urgente"
          v-model="tarea.estado"
        >
        <label class="form-check-label" for="inlineRadio1">
          Urgente
        </label>
      </div>

      <div class="form-check form-check-inline">
        <input 
          class="form-check-input" 
          type="radio" 
          id="inlineRadio2" 
          value="relax"
          v-model="tarea.estado"
        >
        <label class="form-check-label" for="inlineRadio2">
          Relax
        </label>
      </div>
    </div>

    <div class="my-2">
      <input 
          class="form-control" 
          type="Number"  
          placeholder="Número"
          v-model.number="tarea.numero"
        >
    </div>}

    <input 
      type="text" 
      placeholder="Nombre Tarea"
      class="form-control"
      v-model.trim="tarea.nombre"
    >

    <button 
      class="btn btn-block btn-dark" 
      type="submit"
    >
      Enviar
    </button>

  </form>
  <p>{{tarea}}</p>
</template>

<script>


export default {
  name: 'Home',
  components: {
    
  },
  data() {
    return {
      tarea: {nombre: '', categories: [], estado: '', numero: 0},
    }
  },
  methods: {
    procesarFormulario() {
      if(this.tarea.nombre.trim() === ''){
        console.log('Nombre vacío');
        return;
      }
    }
  }
}
</script>
