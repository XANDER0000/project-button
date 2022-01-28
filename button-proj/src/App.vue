<template>
  <div id="app">
    <ButtonStyle border text="Привет!"/>

    <ButtonStyle BackColor="blue" BackColorHover="blue" text="Привет!"/>

    <ButtonStyle small text="Привет!"/>

    <ButtonStyle medium text="Привет!"/>

    <ButtonStyle large text="Привет!"/>

    <ButtonStyle width="80%" text="Привет!"/>

    <ButtonStyle text="Не Привет!"/>

    <ButtonStyle radius="30px" text="Привет!"/>

    <ButtonStyle color="blue" ColorHover="blue" text="Привет!"/>

    <ButtonStyle BackColorHover="blue" animate=".2s" text="Привет!"/>

    <ButtonStyle ColorHover="blue" animate=".2s" text="Привет!"/>

    <ButtonStyle disabled animate=".2s" text="Привет!"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import ButtonStyle from './components/button'

export default {
  name: 'App',
  components: {
    HelloWorld,
    ButtonStyle,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}

#app button {
  margin-bottom: 20px;
}
</style>
