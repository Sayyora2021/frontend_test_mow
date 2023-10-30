<template>
  <div class="body">
    <h1>Rechercher par activité</h1>
    <div class="boxes">
      <div
        class="card"
        v-for="(activity, index) in activities"
        :key="index"
        @click="toggleHighlight(index)"
        :class="{ highlighted: activity.highlighted }"
      >
        <font-awesome-icon :icon="activity.icon" class="icon" />
        <p>{{ activity.name }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activities: [
        { name: 'Sport d\'hiver', icon: ['fas', 'skiing'], highlighted: false },
        { name: 'Aquatique', icon: ['fas', 'swimmer'], highlighted: false },
        { name: 'Randonnée', icon: ['fas', 'hiking'], highlighted: false },
        { name: 'Aérien', icon: ['fas', 'parachute-box'], highlighted: false },
        { name: 'Sport d\'équipe', icon: ['fas', 'volleyball-ball'], highlighted: false },
      ],
    };
  },
  methods: {
    toggleHighlight(index) {
      this.activities[index].highlighted = !this.activities[index].highlighted;
    },
  },
};
</script>

<style scoped>
h1 {
  font-family: 'Railway', sans-serif;
  padding: 50px;
}

.card {
  width: 190px;
  height: 190px;
  border-radius: 30px;
  background: #e0e0e0;
  box-shadow: 15px 15px 30px #bebebe;
  border: 5px solid transparent;
  transition: border-color 0.3s;
  padding: 15px;
}

.card.highlighted {
  border-color: rgb(8, 188, 8);
  box-shadow: 10px 10px 10px rgb(187, 238, 187);
}

.icon {
  width: 50px;
  height: 50px;
  color: rgb(8, 188, 8);
  padding: 60px;
}

.boxes {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  margin: 30px;
  gap: 10px;
}

p {
  font-family: 'Railway', sans-serif;
  font-size: 16px;
  display: flex;
  justify-content: space-around;
}

.body {
  background-color: #e6e3e3;
  height: auto;
  padding: 20px;
}
</style>
