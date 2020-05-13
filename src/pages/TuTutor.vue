<template>
  <el-container style="height: 100%; border: 1px solid #eee">
      <!-- Barra de navegación -->
      <el-menu :router="true" default-active="2" @open="handleOpen" @close="handleClose" :collapse="isCollapse" background-color="#1e2129" text-color="#fff" active-text-color="#ffd04b">
        <el-menu-item :router="false" index="Plantilla" @click="display">
          <i class="fas fa-university icon-4x"></i>&nbsp;
          <span slot="title">TuTutor</span>
        </el-menu-item>
        <!--Alumno FACI-->
        <!-- <el-menu-item index="2" disabled>
          <i class="el-icon-document"></i>
          <span>Alumno FACI</span>
        </el-menu-item>
        <el-menu-item index="3">
          <i class="el-icon-menu"></i>
          <span slot="title">Inicio</span>
        </el-menu-item>
        <el-menu-item index="4">
          <i class="el-icon-menu"></i>
          <span slot="title">Agenda</span>
        </el-menu-item>
        <el-menu-item index="5">
          <i class="el-icon-menu"></i>
          <span slot="title">Tutor asignado</span>
        </el-menu-item> -->

        <!--Alumno Generales-->
        <!-- <el-menu-item index="2" disabled>
          <i class="el-icon-document"></i>
          <span>Alumno Generales</span>
        </el-menu-item>
        <el-menu-item index="3">
          <i class="el-icon-menu"></i>
          <span slot="title">Agenda</span>
        </el-menu-item>
        <el-menu-item index="4">
          <i class="el-icon-menu"></i>
          <span slot="title">Solicitar sesión</span>
        </el-menu-item>
        <el-menu-item index="5">
          <i class="el-icon-menu"></i>
          <span slot="title">Tutor asignado</span>
        </el-menu-item> -->

        <!--Tutor-->
        <el-menu-item index="2" disabled>
          <i class="el-icon-document"></i>
          <span>Tutor</span>
        </el-menu-item>
        <el-menu-item index="Asignaciones">
          <i class="el-icon-menu"></i>
          <span slot="title">Asignaciones</span>
        </el-menu-item>
        <el-menu-item index="Citas">
          <i class="el-icon-date"></i>
          <span slot="title">Citas</span>
        </el-menu-item>
        <el-menu-item index="Sesiones">
          <i class="el-icon-menu"></i>
          <span slot="title">Sesiones</span>
        </el-menu-item>
        <el-menu-item index="Solicitudes">
          <i class="el-icon-menu"></i>
          <span slot="title">Solicitudes</span>
        </el-menu-item>
        <el-menu-item index="Alumnos">
          <i class="el-icon-menu"></i>
          <span slot="title">Alumnos</span>
        </el-menu-item>

        <!--Soporte-->
        <!-- <el-menu-item index="10" disabled>
          <i class="el-icon-document"></i>
          <span>Soporte</span>
        </el-menu-item>
        <el-menu-item index="3">
          <i class="el-icon-menu"></i>
          <span slot="title">Pagina principal</span>
        </el-menu-item>
        <el-menu-item index="4">
          <i class="el-icon-menu"></i>
          <span slot="title">Agregar alumnos</span>
        </el-menu-item>
        <el-menu-item index="5">
          <i class="el-icon-menu"></i>
          <span slot="title">Generar citas</span>
        </el-menu-item> -->

         <!--Coordinador-->
         <!-- <el-menu-item index="2" disabled>
          <i class="el-icon-document"></i>
          <span>Coordinador</span>
        </el-menu-item>
        <el-menu-item index="2">
          <i class="el-icon-menu"></i>
          <span slot="title">Pagina principal</span>
        </el-menu-item>
        <el-menu-item index="3">
          <i class="el-icon-menu"></i>
          <span slot="title">Miembros</span>
        </el-menu-item>
        <el-menu-item index="4">
          <i class="el-icon-menu"></i>
          <span slot="title">Tutorias activas</span>
        </el-menu-item>
        <el-menu-item index="5">
          <i class="el-icon-menu"></i>
          <span slot="title">Reportes</span>
        </el-menu-item> -->
        
        <!--Administrador-->
        <!-- <el-menu-item index="2" disabled>
          <i class="el-icon-document"></i>
          <span>Administrador</span>
        </el-menu-item>
        <el-menu-item index="2">
          <i class="el-icon-menu"></i>
          <span slot="title">Principal</span>
        </el-menu-item>
        <el-menu-item index="3">
          <i class="el-icon-menu"></i>
          <span slot="title">Errores</span>
        </el-menu-item>
        <el-menu-item index="4">
          <i class="el-icon-menu"></i>
          <span slot="title">Auditoria</span>
        </el-menu-item> -->
  
        </el-menu> 
    
    <el-container>
      <!-- Cabecera -->
      <el-header class="headerfooter" style="text-align: right; font-size: 12px ;height:15%">
        <el-row :gutter="20" style="height:100%">
            <el-col :span="6" style="height:100%;padding-top:5px;padding-bottom:5px;">
              <div class="grid-content bg-purple " style="height:100%;">
                <el-image style="height:100%;" :src="tututor" :fit="fill"></el-image>
              </div>
            </el-col>
            <el-col :span="8" style="height:100%;">
              <div class="grid-content bg-purple" style="height:100%;">
                <label class="usuario">Bienvenido Alumno<br>&nbsp;Nuñez Munaylla Italo</label>
              </div>
            </el-col>
            <el-col :span="3" style="height:100%;">
              <div class="grid-content bg-purple" style="height:100%;position:relative">
                <el-dropdown class="intermedio">
                  <span class="el-dropdown-link"><i class="fas fa-list-ul" style="color:white;font-size: 1.3rem;"></i></span>
                  <el-dropdown-menu slot="dropdown">
                    <el-dropdown-item icon="el-icon-user-solid">Mi cuenta</el-dropdown-item>
                    <el-dropdown-item icon="el-icon-circle-close">Cerrar sesión</el-dropdown-item>
                  </el-dropdown-menu>
                </el-dropdown>

              </div>
            </el-col>
            <el-col :span="7" style="height:100%;border-radius: 25px 0px 0px 25px;background-color:white;padding-top:5px;padding-bottom:5px;">
              <div class="grid-content bg-purple" style="height:100%;">
                <el-image style="height:100%;" :src="pucp" :fit=fill></el-image>
              </div>
            </el-col>
        </el-row>

      </el-header>

      <!-- Contenido -->
      <el-container style="height:75%">
        <router-view style="height:100%"></router-view>
      </el-container>

      <el-footer class="headerfooter" style="height:10%">
        <el-row :gutter="20"  style="height:100%">
          <el-col :span="6" style="height:100%"><div class="grid-content bg-purple" style="height:100%">
            <label class="usuario" style="font-size:x-small !important;">© Pontificia Universidad Católica del Perú<br>Lima-32 PERU Telf. (511) 6262000</label>
          </div></el-col>
          <el-col :span="6" :offset="12" style="height:100%"><div class="grid-content bg-purple" style="height:100%">
            <label class="usuario" style="font-size:x-small !important;">consultas a: <a href="https://www.w3schools.com" style="color:white">asistencia-dti@pucp.edu.pe</a><br>Dirección de Tecnologías de Información</label>
          </div></el-col>
        </el-row>
      </el-footer>
    </el-container>
  </el-container>
</template>

<style >
@import url("//unpkg.com/element-ui@2.13.1/lib/theme-chalk/index.css");
.usuario{
  text-align: left;
  top:50% !important;
  transform: translateY(-50%)!important;
  position: relative !important;
  font-family: Arial, Helvetica, sans-serif;
  font-size:large;
  display: block;
  line-height: 20px;
}
.intermedio{
  top:50% !important;
  transform: translateY(-50%)!important;
  position: relative !important;
}
.el-dropdown-link {
    cursor: pointer;
    color: #409EFF;
}
.el-icon-arrow-down {
  font-size: 12px;
}
.headerfooter {
  background-color: #006181;
  color: rgb(255, 255, 255);
  text-align: center;
  line-height: 60px;
}
.el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 200px !important;
    min-height: 400px;
  }
</style>

<script>
const tututor = require('../assets/tututor.jpeg')
const pucp = require('../assets/pucp.png')
  export default {
    data() {
      const item = {
        date: '2016-05-02',
        name: 'Tom',
        address: 'No. 189, Grove St, Los Angeles'
      };
      return {
        isCollapse: true,
        tututor,
        pucp,
        url:'../assets/tututor.jpeg',
        tableData: Array(20).fill(item)
      }
    },
    methods: {
      display(isCollapse){
        console.log(isCollapse);
        this.isCollapse = !this.isCollapse;
      },
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  };
</script>