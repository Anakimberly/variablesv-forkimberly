<template >
    <div class="container" >
       <div class="row mt-4">
        <div>
            <h4>Evento click</h4>
            <button @click="clic" class="btn btn-danger" type="button">Dale clic</button>
            <button @click="soyButon" class="btn btn-warning mx-2" type="button">Presiona</button>
        </div>
        <div>
            
            <h4>Evento Change</h4>
            <label class="input-group-text" for="">ingresa tu Color favorito</label>
            <input class="form-control mt-2" type="text" id="color" @change="colorE">
           <p>El color ingresado es:<strong>{{ color }}</strong></p> 
        </div>

        <h3>Evento de Mouseenter y Mouseleave</h3>
        <div> 
        <div class="text-center"
        style= "color: #ffff;width: 300px; height: 200px; background-color: purple; text-align: center; padding: 15px; border-radius: 15px;"
         @mouseenter="mostrarMensaje" @mouseleave="ocultarMensaje">
<p>pasa el mouse</p>
<p>{{ mensaje }}</p>

</div> 
        </div>
       </div> 
    </div>
</template> 
<script>
export default {   
    data(){
        return{
            color: '',
            mensaje:'',

        }
    },
    methods:{
        clic(){
            alert("Bienvenid@")
        },
        soyButon(){
            alert("Sigue adelante, lo estas haciendo bien :3")
        },
        colorE(event){
            this.color = event.target.value

        },
        mostrarMensaje(){
           this.mensaje="Hola,estoy dentro del rectangulo" 
        },
        ocultarMensaje(){
            this.mensaje="Ups, ahora me sali del rectangulo" 
        }
    }
    
}
</script>
<style >
    
</style>