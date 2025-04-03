
    <script setup>
import { ref } from 'vue'
import Hijo1 from './Hijo1.vue'
import Hijo2 from './Hijo2.vue'


defineProps({
  nombre: String,
})

const count = ref(0)
</script>

<template>
    
    <div class ="container mt-4">
      <div class="card" style=" background-color:burlywood;">
        <h2 class ="text-center"> EJEMPLO PROPS</h2>
            <div class="row mt-4">
          <div class="col-md-4 ">
            <div class="card"  style=" background-color:wheat;">
                <img src="https://us.123rf.com/450wm/notkoo2008/notkoo20081503/notkoo2008150304225/37166388-elemento-de-tema-de-oso.jpg?ver=6" class="card-img-top" alt="...">
                <h4 class="text-center">Hola! Soy el oso padre</h4>
            </div>
          </div>
          <div class="col-md-4">
            <div class="card " style="width: 18rem; background-color:wheat; ">
                <img src="https://i.pinimg.com/736x/8f/97/9f/8f979f9887bed060e1a10b7af31bfe8d.jpg" class="card-img-top" alt="...">
                <Hijo1 class="mt-4" edad="Tengo 10 años"/>
            </div>
          </div>
          <div class="col-md-4">
            <div class="card" style="width: 18rem;  background-color:wheat;">
                <img src="https://i.pinimg.com/736x/a7/6d/8b/a76d8b61b636ac44c039c9de0c259b67.jpg" class="card-img-top" alt="...">
                <Hijo2 class="mt-4" edad=" Tengo 2 añitos"/>
            </div>
          </div>
        </div>
      </div>
       
        </div>


</template>

<style scoped>
h2{
    background-color:rgb(182, 153, 101);
}

</style>

