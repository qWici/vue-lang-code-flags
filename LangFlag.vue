<template>
    <span v-if="iso" class="flag-icon" :class="flagIconClass" :title="title || iso"></span>
</template>
<script>
import "flag-icon-css/css/flag-icon.css";
import relation from "./relation";

export default {
    name: "LangFlag",

    props: {
      iso: { type: String, required: true },
      title: { type: String, default: null },
      squared: { type: Boolean, default: true }
    },

    computed: {
      flagIconClass: function () {
        return (
          (!!this.squared ? "flag-icon-squared " : "") +
          "flag-icon-" +
          this.flagCode
        );
      },
      flagCode: function () {
        return relation[this.iso.toLowerCase()];
      }
    }
};
</script>
