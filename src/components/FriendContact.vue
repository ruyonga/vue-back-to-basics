<template>
  <li>
    <h2>{{ friend.name }}</h2>
    <button @click="toggleDetails"> {{ detailsAreVisible ? 'Hide' : 'Show' }} Details </button>
  </li>
  <ul v-if="detailsAreVisible">
    <li>
      <strong>Phone:</strong>
      {{ friend.phone }}
    </li>
    <li>
      <strong>Email:</strong>
      {{ friend.email }}
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      detailsAreVisible: false,
      friend: {
        id: "dan",
        name: "Ruyonga Daniel",
        phone: "+25670345343443",
        email: "dan@tehe.com",
      },
    };
  },
  methods: {
    toggleDetails() {
      this.detailsAreVisible = !this.detailsAreVisible;
    },
  },
};
</script>

<style>
</style>