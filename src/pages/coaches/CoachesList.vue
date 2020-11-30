<template>
  <section>Filter</section>
  <section>
    <div class="controls">
      <button>Refresh</button>
      <router-link to="/register">Register </router-link>
    </div>
    <ul>
      <li v-for="coach in filteredCoaches" :key="coach.id">
        {{ coach.firstName }}
      </li>
    </ul>
  </section>
</template>
<script>
export default {
  computed: {
    filteredCoaches() {
      debugger;
      const data = this.$store.getters.coaches;
      return data;
    },
  },
};
</script>
