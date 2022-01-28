<template>
  <div id="app">
    <ButtonStyle border textColorHover="#fff" backgroundColorHover="blue" transition=".2s" text="Привет!"/>

    <ButtonStyle backgroundColor="blue" backgroundColorHover="blue" text="Привет!"/>

    <ButtonStyle small text="Привет!"/>

    <ButtonStyle medium text="Привет!"/>

    <ButtonStyle large text="Привет!"/>

    <ButtonStyle width="80%" text="Привет!"/>

    <ButtonStyle text="Не Привет!"/>

    <ButtonStyle radius="30px" text="Привет!"/>

    <ButtonStyle textColor="blue" textColorHover="blue" text="Привет!"/>

    <ButtonStyle backgroundColorHover="blue" transition=".2s" text="Привет!"/>

    <ButtonStyle textColorHover="blue" transition=".2s" text="Привет!"/>

    <ButtonStyle disabled transition=".2s" text="Привет!"/>
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
