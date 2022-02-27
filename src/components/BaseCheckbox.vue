<template>
     <div>
        <input
          type="checkbox"
          :checked="modelValue"
          @change="$emit('update:modeValue','$event.target.checked')"
          v-model="event.extras.catering"
          class="field"
        />
        <label v-if="label">{{ label }}</label>
      </div>    
</template>

<script>
export default {
    props: {
        label: {
            type: String,
            default: ''
        }
    },
    modelValue: {
        type: Boolean,
        default: false
    }

}
</script>