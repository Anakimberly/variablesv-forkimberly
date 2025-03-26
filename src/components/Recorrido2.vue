<script>
export default{
    data(){
        return{
            //DATOS DEL ALUMNO
            alumnos:[
                {nc:22620053, nombre: 'Ana Kimberly', carrera: 'ISC'},
                {nc:22620053, nombre: 'Efren', carrera: 'IC'},
                {nc:22620053, nombre: 'Brenda', carrera: 'ADMON'},
            ]
        }
    }
}
</script>
<template>
<div class="container">
    <h3 class="mt-4">Lista de alumnos</h3>
    <ul>
        <li v-for="alumno in alumnos" :key="alumno.nc">
            <strong>{{ alumno.nombre }} </strong> -
            <strong>{{ alumno.carrera }} </strong>
        </li>
    </ul>
</div>
</template>
 <style>
 h3{
    color:black;
    background-color:rgb(237, 182, 114);
    border-radius: 15px;
    padding: 10px;
    text-align: center;
 }
 ul {
    list-style-type: none;
    padding: 0%;
 }
 li {
    color:blue;
    background-color:bisque;
    border-radius: 15px;
    padding: 10px;
    margin: 10px;
 }
</style>