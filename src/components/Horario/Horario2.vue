<template>

    <div class="container"> 
      <h3 class="mt-4">CARGA ACADEMICA</h3>
      <!-- TABLA 1 -->
      <table class="table table-success table-striped">
          <thead>
              <tr>
                  <td scope="col" class="ncontrol">N° control</td>
                  <td scope="col">Nombre</td>
                  <td scope="col">Grado</td>
                  <td scope="col">Periodo</td>
              </tr>
          </thead>
          <tbody>
              <tr v-for="(h, index) in cabecera" :key="index">
                  <td>{{ h.Ncontrol }}</td>
                  <td>{{ h.Nombre }}</td>
                  <td>{{ h.Grado }}</td>
                  <td>{{ h.Periodo }}</td>
              </tr>
          </tbody>
      </table>
      <!-- TABLA 2 -->
      <table class="table table-success table-striped">
          <thead>
              <tr>
                  <td scope="col">Carrera</td>
                  <td scope="col">Especialidad</td>
                  <td scope="col">Creditos</td>
                  <td scope="col">Plan de estudios</td>
              </tr>
          </thead>
          <tbody>
              <tr v-for="(h, index) in cabecera2" :key="index">
                  <td>{{ h.carrera }}</td>
                  <td>{{ h.especialidad }}</td>
                  <td>{{ h.creditos }}</td>
                  <td>{{ h.Plandeestudios }}</td>
              </tr>
          </tbody>
      </table>
      <!-- TABLA3 -->
      <table class="table table-success table-striped">
    <thead>
      <tr>
        <th scope="col">Materia</th>
        <th scope="col">Rep</th>
        <th scope="col">Cr</th>
        <th scope="col">Lunes</th>
        <th scope="col">Martes</th>
        <th scope="col">Miercoles</th>
        <th scope="col">Jueves</th>
        <th scope="col">Viernes</th>
        <th scope="col">Sabado</th>
        <th scope="col">Domingo</th>
        <!-- <th scope="col">Docentes</th>
        <th scope="col">Aulas</th>
         -->
      </tr>
    </thead>
    <tbody>
     <tr v-for="(h, index) in horario" :key="index">
      <td>{{ h.materia }}</td>
      <td>{{ h.rep }}</td>
      <td>{{ h.cr}}</td>
      <td>{{ h.lunes }}</td>
      <td>{{ h.martes }}</td>
      <td>{{ h.miercoles }}</td>
      <td>{{ h.jueves }}</td>
      <td>{{ h.viernes }}</td>
      <td>{{ h.sabado }}</td>
      <td>{{ h.domingo }}</td>
      <!-- <td>{{ h.docentes }}</td>
      <td>{{ h.Aulas }}</td> -->
     </tr>
    </tbody>
  </table>
    </div>
     
  </template>
  
  <script setup>
  const cabecera = ref([
  { Ncontrol: '22620053', Nombre: 'Ana Kimberly Hernandez Perez', Grado: '6', Periodo: 'ENE-JUN 25' }
]);
const cabecera2 = ref([
  { carrera: 'Ingenieria en sistemas computacionales', especialidad: '', creditos: '33', plandeestudios: 'ISIC-2010-224' }
]);
  import {h, ref} from 'vue';
  const horario = ref ([
    {materia:'6BS  / Lenguajes Y Automatas I / Solano Hernandez Miguel Angel',rep:'N',cr:'5',lunes:'11:00-13:00/LC3',martes:'',miercoles:'11:00-13:00/4',jueves:'',viernes:'12:00-13:00/RDS',sabado:'',domingo:''},
    {materia:'6BS  / Redes De Computadoras / Sanchez Vasquez Lucia',rep:'N',cr:'5',lunes:'',martes:'13:00-15:00/RDS',miercoles:'',jueves:'13:00-15:00/LDS',viernes:'16:00-17:00/LDS',sabado:'',domingo:''},
    {materia:'6BS  / Programacion Web /  Vasquez Martínez Josué Israel',rep:'N',cr:'5',lunes:'',martes:'17:00-19:00/ ACS',miercoles:'',jueves:' 17:00-19:00/ ACS',viernes:'13:00-14:00/ ACS',sabado:'',domingo:''},
    {materia:'6BS  /Taller De Sistemas Operativos  /  Cruz Perez Jorge',rep:'N',cr:'4',lunes:'13:00-15:00',martes:'',miercoles:'13:00-15:00',jueves:'',viernes:'',sabado:'',domingo:''},
    {materia:'6BS  /Administracion De Bases De Datos   /   Garcia Hernandez Hilario Vidal',rep:'N',cr:'5',lunes:'',martes:'15:00-17:00/RDS',miercoles:'15:00-17:00/LDS',jueves:'',viernes:'14:00-15:00/LDS',sabado:'',domingo:''},
    {materia:'6BS  /Lenguajes De Interfaz   /  Sanchez Vasquez Lucia',rep:'N',cr:'4',lunes:'',martes:'11:00-13:00/MAG 2',miercoles:'17:00-19:00/RDS',jueves:'',viernes:'',sabado:'',domingo:''},
    {materia:'6BS  /Ingenieria De Software   /  Roman Cruz Jose Alfredo',rep:'N',cr:'5',lunes:'15:00-17:00/LDS',martes:'',miercoles:'',jueves:'15:00-17:00/LDS',viernes:'15:00-16:00/RDS',sabado:'',domingo:''},
    
      // {hora:'12:00-13:00',lunes: 'Libre',martes: 'libre',miercoles:'Libre',jueves:'libre',viernes:'Lenguajes Y Automatas I',docentes:'Cruz Perez Jorge',Aulas:'LDS'},
      // {hora:'11:00 - 13:00',lunes: 'Lenguajes Y Automatas-Miguel angel solano hernandez ',martes: 'Lenguajes De Interfaz',miercoles:'Lenguajes Y Automatas I',jueves:'libre',viernes:'movil',docentes:'Solano Hernandez Miguel Angel',Aulas:'LC3-4-RDS'},
      // {hora:'13:00 - 14:00',lunes: 'Libre',martes: 'Libre',miercoles:'Libre',jueves:'libre',viernes:'Programacion Web',docentes:'Roman Cruz Jose Alfredo',Aulas:'LDS-RDS'},
      // {hora:'14:00 - 15:00',lunes: 'Libre',martes: 'Libre',miercoles:'Libre',jueves:'libre',viernes:'Administracion De Bases De Datos',docentes:'Sanchez Vasquez Lucia',Aulas:' LDS-RDS'},
      // {hora:'13:00-15:00',lunes: 'Taller De Sistemas Operativos',martes: 'Redes De Computadoras',miercoles:'Taller De Sistemas Operativos',jueves:'Redes De Computadoras',viernes:'movil',docentes: 'Garcia Hernandez Hilario Vidal',Aulas: 'RDS- LDS'},
      // {hora:'15:00 - 16:00',lunes: 'Libre',martes: 'Libre',miercoles:'Libre',jueves:'libre',viernes:'Ingenieria De Software',docentes:'Vasquez Martínez Josué Israel',Aulas:'ACS'},
      // {hora:'16:00 - 17:00',lunes: 'Libre',martes: 'Libre',miercoles:'Libre',jueves:'libre',viernes:'Redes De Computadoras'},
      // {hora:'15:00-17:00',lunes: 'Ingenieria De Software',martes: 'Administracion De Bases De Datos',miercoles:'Administracion De Bases De Datos',jueves:'Ingenieria De Software',viernes:'Libre'},
      // {hora:'17:00-19:00',lunes: 'Libre',martes: 'Programacion Web',miercoles:'Lenguajes De Interfaz',jueves:'Programacion Web',viernes:'Libre'},
  ])
  </script> 
<style>
h3{
  background-color: rgb(62, 141, 111);
}
</style>