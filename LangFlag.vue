<template>
    <span v-if="iso" class="flag-icon" :class="flagIconClass" :title="title || iso"></span>
</template>
<script>
  import 'flag-icon-css/css/flag-icon.css'

  export default {
    name: 'LangFlag',
    props: {
      iso: {type: String, default: null},
      title: {type: String, default: null},
      squared: {type: Boolean, default: true},
    },
    computed: {
      flagIconClass: function () {
        return ((!!this.squared) ? 'flag-icon-squared ' : '') + 'flag-icon-' + this.iso.toLowerCase();
      }
    }
  }
</script>