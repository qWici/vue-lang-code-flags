<template>
    <span v-if="iso" class="fi" :class="flagIconClass" :title="title || iso"></span>
</template>
<script>
import "flag-icons/css/flag-icons.css";
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
          (!!this.squared ? "fis " : "") +
          "fi-" +
          this.flagCode
        );
      },
      flagCode: function () {
        return relation[this.iso.toLowerCase()];
      }
    }
};
</script>
