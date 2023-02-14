<template>
  <h3>Jobs</h3>
  <div v-for="job in jobs" :key="job.id" class="job">
    <router-link :to="{ name: 'jobsDetails', params: { id: job.id } }">
      <h3>{{ job.title }}</h3>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { title: 'Ninja UX Designer', id: 1, details: 'lorem' },
        { title: 'Ninja WEB Designer', id: 2, details: 'lorem' },
        { title: 'Ninja VUE Designer', id: 3, details: 'lorem' },
      ],
    };
  },
};
</script>

<style>
.job h3 {
  background: #f4f4f4;
  padding: 20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}
.job h3:hover {
  background: #ddd;
}
.job a {
  text-decoration: none;
}
</style>
