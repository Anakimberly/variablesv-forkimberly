<script>
export default{
    data(){
        return{
        display:'',
        currentValue:0,
    }
    },
    methods:{
        agregarNumero(numero) {
            this.display += numero;
        },
      
        calculo(){
        try{
            this.currentValue = eval(this.display);
            this.display = this.currentValue.toString();
        }catch(error){
           this.display = 'Error';
        }
        
         
        },
        LimpiarDisplay(){
            this.display= '';
        },
        eliminarNumero(){
            this.display = this.display.slice(0, -1);
        }
    }
}
</script>
<template>
<div class="container d-flex justify-content-center mt-4" style="height: 400px; ">
    <div class="card p-3" style="width: 300px; background-color: #D2B4DE;">
        <div class="car-body">
            <h6 class="text-center" style="color: black;"> CALCULADORA V2</h6>
            <!-- DISPLAY DE LA CALCULADORA -->
             <div class="mb-3">
                <input type="text" class="form-control" v-model="display" disabled>
             </div>
             <!-- BOTONES DE PORCENTAJE Y ESO -->
             <div class="d-flex justify-content-between">
                <button class="btn btn-light" style="height: 50px; width: 50px;" @click="" >%</button>
                <button class="btn btn-light"style="height: 50px; width: 50px;" @click="LimpiarDisplay" >CE</button>
                <button class="btn btn-light"style="height: 50px; width: 50px;" @click="LimpiarDisplay" >C</button>
                <button class="btn btn-danger"style="height: 50px; width: 50px;" @click="eliminarNumero" >B</button>
              </div>
             <!-- BOTONES DE LA CALCULADORA -->
              <div class="d-flex justify-content-between mt-2">
                <button class="btn btn-light"style="height: 50px; width: 50px;" @click="agregarNumero(9)" >9</button>
                <button class="btn btn-light" style="height: 50px; width: 50px;"@click="agregarNumero(8)" >8</button>
                <button class="btn btn-light" style="height: 50px; width: 50px;"@click="agregarNumero(7)" >7</button>
                <button class="btn btn-danger" style="height: 50px; width: 50px;"@click="agregarNumero('/')" >/</button>
              </div>
              <!-- SEGUNDA FILA DE BOTONES -->
              <div class="d-flex justify-content-between mt-2">
                <button class="btn btn-light"style="height: 50px; width: 50px;" @click="agregarNumero(4)" >4</button>
                <button class="btn btn-light" style="height: 50px; width: 50px;"@click="agregarNumero(5)" >5</button>
                <button class="btn btn-light"style="height: 50px; width: 50px;" @click="agregarNumero(6)" >6</button>
                <button class="btn btn-danger"style="height: 50px; width: 50px;" @click="agregarNumero('*')" >x</button>
              </div>
              <!-- TERCERA FILA DE BOTONES -->
              <div class="d-flex justify-content-between mt-2">
                <button class="btn btn-light"style="height: 50px; width: 50px;" @click="agregarNumero(1)" >1</button>
                <button class="btn btn-light"style="height: 50px; width: 50px;" @click="agregarNumero(2)" >2</button>
                <button class="btn btn-light"style="height: 50px; width: 50px;" @click="agregarNumero(3)" >3</button>
                <button class="btn btn-danger"style="height: 50px; width: 50px;" @click="agregarNumero('-')" >-</button>
              </div>
              <!-- cuarta fila de botones -->
              <div class="d-flex justify-content-between mt-2">
                <button class="btn btn-warning"style="height: 50px; width: 50px;" @click="calculo" >=</button>
                <button class="btn btn-light" style="height: 50px; width: 50px;"@click="agregarNumero(0)" >0</button>
                <button class="btn btn-light" style="height: 50px; width: 50px;"@click="agregarNumero()" >.</button>
                <button class="btn btn-danger" style="height: 50px; width: 50px;"@click="agregarNumero('+')" >+</button>
              </div>
        </div>
    </div>
</div>
</template>