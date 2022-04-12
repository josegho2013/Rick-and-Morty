<template>
  <div class="container">
    <div class="image">
      <img
        class="w-34 justify-center"
        src="https://occ-0-1722-1723.1.nflxso.net/dnm/api/v6/LmEnxtiAuzezXBjYXPuDgfZ4zZQ/AAAABeJtBpd7gVufNBcVqvz9HPneSuK06oCuSWVIe1rbvL9yoBfZbHbUhjLgU0yv1DoOG8gWtyFUjonoxF132iuRBPNf_LoVM6tKrbKc.png?r=871"
        alt=""
      />
    </div>
    <FilterByStatus />
    <FilterByName />
    <ListCharacters />
  </div>
</template>

<script>
import ListCharacters from "@/components/ListCharacters";
import FilterByStatus from "@/components/FilterByStatus";
import FilterByName from "@/components/FilterByName";
export default {
  name: "App",
  components: {
    ListCharacters,
    FilterByStatus,
    FilterByName,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Sora:wght@300&display=swap");

:root {
  --background-body: #000000;
  --background-card: #52afe1;
  --text-white: #ffffff;
  --text-gray: #161515;
  --text-orange: #161515;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  background-color: var(--background-body);
  color: var(--text-white);
  font-family: "Sora", sans-serif;
}
h1 {
  margin-bottom: 3rem;
  text-align: center;
}
.container {
  width: 70%;
  max-width: 90%;
  margin: 3rem auto;
}
.container h1 {
  font-variant: small-caps;
  font-size: xx-large;
}
img {
  width: 100%;
}
.image {
  display: flex;
  width: 35rem;
  justify-content: center;
  margin: auto;
  margin-bottom: 2rem;
}
</style>
