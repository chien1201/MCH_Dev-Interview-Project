<template>
  <div class="historical-websites">
    <h2>歷年梅竹黑客松網站</h2>

    <div class="websites-grid">
      <div v-for="website in websites" :key="website.id" class="website-card">
        <img
          :src="website.image_url"
          :alt="website.name"
          class="website-image"
        />
        <div class="website-info">
          <h3>{{ website.name }}</h3>
          <p>{{ website.description }}</p>
          <a :href="website.link" target="_blank" class="view-button"
            >查看網站</a
          >
        </div>
      </div>
    </div>
  </div>
</template>


<script>
// TODO: Fetch websites data from API

import axios from "axios";

export default{
  data(){
    return {
      websites: [],
      loading : true,
      error : null,
    }
  },

  methods: {
    async fetchWebsites(website_id) {
      try {
        const response = await axios.get("https://mch-dev.userwei.com/api/websites");
        this.websites = response.data;
      } catch (err) {
        this.error = "can't fetch website";
      } finally {
        this.loading = false;
      }
    },
  },

  mounted() {
    this.fetchWebsites();
  },
};

</script>

<style scoped>
.historical-websites {
  padding: 40px 20px;
  max-width: 1200px;
  margin: 0 auto;
}

.historical-websites h2 {
  text-align: center;
  margin-bottom: 40px;
  font-size: 2rem;
  color: #333;
}

.loading,
.error {
  text-align: center;
  font-size: 1.2rem;
  color: #ff0000;
}

.websites-grid {
  /* TODO: Add styles for a responsive grid layout */
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  justify-contents: center;
}

.website-card {
  background-color: #f9f9f9;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s;
}

.website-card:hover {
  transform: translateY(-5px);
}

.website-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.website-info {
  padding: 20px;
}

.website-info h3 {
  margin: 0 0 10px 0;
  font-size: 1.5rem;
  color: #333;
}

.website-info p {
  font-size: 1rem;
  color: #666;
  margin-bottom: 15px;
}

.view-button {
  display: inline-block;
  padding: 8px 16px;
  background-color: #656d73;
  color: #fff;
  border-radius: 5px;
  text-decoration: none;
}

.view-button:hover {
  background-color: #36383a;
}
</style>
