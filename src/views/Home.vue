<template>
  <div>
    <table-c :assets="assets" />
  </div>
</template>

<script>
import api from "../api";
import TableC from "@/components/TableC";
export default {
  name: "Home",
  components: { TableC },
  data() {
    return {
      assets: []
    };
  },
  created() {
    api.getAssets().then(assets => (this.assets = assets));
  }
};
</script>
