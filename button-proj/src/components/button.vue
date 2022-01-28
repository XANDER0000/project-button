<template>
    <div class="input__slot">

        <button @mouseover="onHover"  @mouseleave="onLeave" class="style__button"
        
        :style="{
            'padding': small ? '10px 15px' : large ? '18px 30px' : '15px 20px' ,
            'width': width ? `${width}` : 'auto',
            ///////////
            'border': border ? `1.5px solid ${BackColor}` : 'none',
            'border-radius': radius ? `${radius}` : 'none',
            ///////////
            'transition': animate ? `${animate} all ease-in-out` : 'none',
            ///////////
            'cursor': disabled ? 'not-allowed' : 'pointer',
            'all': disabled ? 'property' : 'pointer',
            ///////////
            'color': color,
            'background': !border ? BackColor : 'none',
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

    animate: {
      type: String,
      default: ''
    },

    radius: {
      type: String,
      default: ''
    },

    color: {
        type: String,
        default: ''
    },

    ColorHover: {
        type: String,
        default: '',
    },

     TextColorHover2: {
        type: String,
        default: 'red',
    },

    BackColorHover2: {
      type: String,
      default: 'red',
    },

    BackColor: {
        type: String,
        default: ''
    },

    BackColorHover: {
      type: String,
      default: ''
    },

    size: {
        type: Boolean,
        default: false
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

    stat_small: {
        type: Boolean,
        default: false
    },

    stat_medium: {
        type: Boolean,
        default: false
    },

    stat_large: {
        type: Boolean,
        default: false
    },

    full_width: {
        type: Boolean,
        default: false
    },

    border: {
      type: Boolean,
      default: false
    },

     radius: {
      type: Boolean,
      default: false
    },

    animate: {
        type: Boolean,
        default: false
    },

    disabled: {
        type: Boolean,
        default: false
    },

    id: {
      type: String
    },
   
    readonly: {
      type: Boolean,
      default: false
    },
    type: {
      type: String,
      default: 'text'
    },
    isActive: {
      type: Boolean,
      default: false
    }
  },
  data: () => ({
    text: '',
    color: '',
    BackColor: '',
    BackColorHover: '',
    ColorHover: '',
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
      this.TextColorHover2 = this.color,
      this.BackColorHover2 = this.BackColor,
      this.color = this.ColorHover,
      this.BackColor = this.BackColorHover
    },

    onLeave() {
      this.color = this.TextColorHover2,
      this.BackColor = this.BackColorHover2
    },
  }
}
</script>

<style scoped>
</style>
