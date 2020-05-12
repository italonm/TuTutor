<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
import Vue from 'vue'
import VueRouter from 'vue-router'
import Login from './pages/Login'
import TuTutor from './pages/TuTutor'
import Alumnos from './pages/components/Tutor/Alumnos'
import Asignaciones from './pages/components/Tutor/Asignaciones'
import Citas from './pages/components/Tutor/Citas'
import Sesiones from './pages/components/Tutor/Sesiones'
import Solicitudes from './pages/components/Tutor/Solicitudes'
import Plantilla from './pages/components/Plantilla'
import ElementUI  from 'element-ui'
import 'element-ui/lib/theme-chalk/index.css'
import locale from 'element-ui/lib/locale/lang/en'

Vue.use(ElementUI )
Vue.use(ElementUI, { locale })
Vue.use(VueRouter)

export const routes = [
  {path:'', component: TuTutor,
    children: [
      { path: '/Alumnos', component: Alumnos }, 
      { path: '/Asignaciones', component: Asignaciones },
      { path: '/Citas', component: Citas },
      { path: '/Sesiones', component: Sesiones },
      { path: '/Solicitudes', component: Solicitudes },
      { path: '/Plantilla', component: Plantilla }
    ]},
  {path:'/TuTutor',component: Login},
]
const router = new  VueRouter({
  routes: routes
})

export default {
  name: 'App',
  router
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
</style>
