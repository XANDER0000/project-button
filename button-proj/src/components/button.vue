<template>
    <div class="input__slot">

        <button @mouseover="onHover"  @mouseleave="onLeave" class="style__button"
        
        :style="{
            'padding': small ? '10px 15px' : large ? '18px 30px' : '15px 20px' ,
            'width': width ? `${width}` : 'auto',
            ///////////
            'border': border ? `1.5px solid ${backgroundColor}` : 'none',
            'border-radius': radius ? `${radius}` : 'none',
            ///////////
            'transition': transition ? `${transition} all ease-in-out` : 'none',
            ///////////
            'cursor': disabled ? 'not-allowed' : 'pointer',
            'all': disabled ? 'property' : 'pointer',
            ///////////
            'color': textColor,
            'background': !border ? backgroundColor : border && backgroundColorHover ? backgroundColor: 'none',
            ///////////
        }"
        >{{ text }}</button>
      
  </div>

</template>

<script>
export default {
  name: 'ButtonStyle',
  props: {
    text: {
      type: String,
      default: 'Готово'
    },

    width: {
      type: String,
      default: ''
    },

    transition: {
      type: String,
      default: ''
    },

    radius: {
      type: String,
      default: ''
    },

    textColor: {
        type: String,
        default: ''
    },

    textColorHover: {
        type: String,
        default: '',
    },

     textColorHover2: {
        type: String,
        default: 'red',
    },

    backgroundColorHover2: {
      type: String,
      default: 'red',
    },

    backgroundColor: {
        type: String,
        default: ''
    },

    backgroundColorHover: {
      type: String,
      default: ''
    },

    small: {
        type: Boolean,
        default: false
    },

    medium: {
        type: Boolean,
        default: false
    },

    large: {
        type: Boolean,
        default: false
    },

    border: {
      type: Boolean,
      default: false
    },

    transition: {
        type: Boolean,
        default: false
    },

    disabled: {
        type: Boolean,
        default: false
    },
  },
  data: () => ({
    text: '',
    textColor: '',
    backgroundColor: '',
    backgroundColorHover: '',
    textColorHover: '',
    width: '',
    radius: '',
  }),
  methods: {
    getSize (type) {
      if(type === 'large') {
        return 'padding: 15px'
      }
    },
    handleEmitInput(e) {
      this.$emit('input', e.target.value)
    },

    handleSubmitEvent() {
      this.$emit('submitEvent')
    },

    onHover() {
      this.textColorHover2 = this.textColor,
      this.backgroundColorHover2 = this.backgroundColor,
      this.textColor = this.textColorHover,
      this.backgroundColor = this.backgroundColorHover
    },

    onLeave() {
      this.textColor = this.textColorHover2,
      this.backgroundColor = this.backgroundColorHover2
    },
  }
}
</script>

<style scoped>
</style>
