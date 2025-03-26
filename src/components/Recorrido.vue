<script>
export default{
    data(){
        return{
            //DATOS DEL ALUMNO
            alumnos:[
                {nc:22620053, nombre: 'Ana Kimberly', apellidos: 'Hernandez Perez', le_gusta: 'Dormir', carrera: 'ISC'},
                {nc:22620053, nombre: 'Efren', apellidos: 'Garcia Ramirez', le_gusta: 'Manejar moto', carrera: 'IC'},
                {nc:22620053, nombre: 'Brenda', apellidos: 'Silva Damian', le_gusta: 'Viajar', carrera: 'ADMON'},
                {nc:22620053, nombre: 'Liliel', apellidos: 'Vazquez Hernandez', le_gusta: 'Escuchar musica', carrera: 'IM'},
                {nc:22620053, nombre: 'Celeste', apellidos: 'Rosas Cruz', le_gusta: 'Jugar Basquetbol', carrera: 'LARQ'},
                {nc:22620053, nombre: 'Ameli', apellidos: 'Reyes Hernandez', le_gusta: 'Dormir', carrera: 'ISC'},
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
            <strong>{{ alumno.apellidos }}</strong> -
            <strong>{{ alumno.le_gusta }}</strong> -
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
    text-align: center;
 }
</style>