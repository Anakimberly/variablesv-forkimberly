<template>
    <div class="container"> 
      <h3 class="mt-4">HORARIO DE CLASES DE SISTEMAS 6BS</h3>
      <table class="table ">
    <thead>
      <tr>
        <th scope="col">Hora</th>
        <th scope="col">Lunes</th>
        <th scope="col">Martes</th>
        <th scope="col">Miercoles</th>
        <th scope="col">Jueves</th>
        <th scope="col">Viernes</th>
        <th scope="col">Docentes</th>
        <th scope="col">Aulas</th>
        
      </tr>
    </thead>
    <tbody>
     <tr v-for="(h, index) in horario" :key="index">
      <td>{{ h.hora }}</td>
      <td>{{ h.lunes }}</td>
      <td>{{ h.martes }}</td>
      <td>{{ h.miercoles }}</td>
      <td>{{ h.jueves }}</td>
      <td>{{ h.viernes }}</td>
      <td>{{ h.docentes }}</td>
      <td>{{ h.Aulas }}</td>
     </tr>
    </tbody>
  </table>
    </div>
     
  </template>
  
  <script setup>
  import {h, ref} from 'vue';
  const horario = ref ([
      {hora:'12:00-13:00',lunes: 'Libre',martes: 'libre',miercoles:'Libre',jueves:'libre',viernes:'Lenguajes Y Automatas I',docentes:'Cruz Perez Jorge',Aulas:'LDS'},
      {hora:'11:00 - 13:00',lunes: 'Lenguajes Y Automatas',martes: 'Lenguajes De Interfaz',miercoles:'Lenguajes Y Automatas I',jueves:'libre',viernes:'movil',docentes:'Solano Hernandez Miguel Angel',Aulas:'LC3-4-RDS'},
      {hora:'13:00 - 14:00',lunes: 'Libre',martes: 'Libre',miercoles:'Libre',jueves:'libre',viernes:'Programacion Web',docentes:'Roman Cruz Jose Alfredo',Aulas:'LDS-RDS'},
      {hora:'14:00 - 15:00',lunes: 'Libre',martes: 'Libre',miercoles:'Libre',jueves:'libre',viernes:'Administracion De Bases De Datos',docentes:'Sanchez Vasquez Lucia',Aulas:' LDS-RDS'},
      {hora:'13:00-15:00',lunes: 'Taller De Sistemas Operativos',martes: 'Redes De Computadoras',miercoles:'Taller De Sistemas Operativos',jueves:'Redes De Computadoras',viernes:'movil',docentes: 'Garcia Hernandez Hilario Vidal',Aulas: 'RDS- LDS'},
      {hora:'15:00 - 16:00',lunes: 'Libre',martes: 'Libre',miercoles:'Libre',jueves:'libre',viernes:'Ingenieria De Software',docentes:'Vasquez Martínez Josué Israel',Aulas:'ACS'},
      {hora:'16:00 - 17:00',lunes: 'Libre',martes: 'Libre',miercoles:'Libre',jueves:'libre',viernes:'Redes De Computadoras'},
      {hora:'15:00-17:00',lunes: 'Ingenieria De Software',martes: 'Administracion De Bases De Datos',miercoles:'Administracion De Bases De Datos',jueves:'Ingenieria De Software',viernes:'Libre'},
      {hora:'17:00-19:00',lunes: 'Lenguajes De Interfaz',martes: 'Programacion Web',miercoles:'Lenguajes De Interfaz',jueves:'Programacion Web',viernes:'Libre'},
  ])
  </script> 