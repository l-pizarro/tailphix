<template>
  <div id="app">
    <Checkbox :showLabel="true" label="Mostrar solo lo indicado" />
  </div>
</template>

<script>
import Checkbox from "./components/Checkbox.vue"
export default {
  name: 'app',
  components: {
    Checkbox
  }
}
</script>
