<template>
  <div id="app">
    <header-component msg="This is Modern WorldClock with Alarm Setter"/>
    <clock-component />
    <alarm-setter-component />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent';
import ClockComponent from './components/ClockComponent';
import AlarmSetterComponent from './components/AlarmSetterComponent.vue';


export default {
  name: 'App',
  components: {
    HeaderComponent,
    ClockComponent,
    AlarmSetterComponent
   
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
