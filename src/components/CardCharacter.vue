<template>
  <div class="character" :class="[getStatus]">
    <img :src="character.image" :alt="character.name" />
    <div class="character__info">
      <h2>{{ character.name }}</h2>
      <span>{{ character.status }} - {{ character.species }}</span>
      <div class="origen">
        <span>
          Origin:
          {{ character.origin.name }}
        </span>
      </div>
      <div class="location">
        <span>
          Location:
          {{ character.location.name }}
        </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["character"],
  computed : {
    getStatus: function (){
      if(this.character?.status == 'Alive'){
        console.log("this.character.status ",this.character.status)
        return 'bg-green';
      }
      else if (this.character?.status == 'unknown') {
        return 'bg-blue';
      }
      else {
        return 'bg-red';
      }
    },
  },
};
</script>

<style lang="scss">
.character {
  background-color: var(--background-card);
  border-radius: 20px;
  box-shadow: 0 0 10px 1px var(--background-body);
  overflow: hidden;
  cursor: pointer;
  transition: transform 200ms ease-in-out;
  height: 100%;
  &:hover {
    transform: scale(1.05);
    h3 {
      color: var(--text-orange);
    }
  }
  span {
    color: var(--text-white);
  }
  h3 {
    margin-bottom: 0.5rem;
  }
  &__info {
    padding: 1.5rem;
    .origen {
      margin-bottom: 0.5rem;
    }
  }
}
.bg-green {
  background-color: rgb(48 179 0 / 80%);
}
.bg-red {
  background-color: rgb(239 68 68 / 1)
}
.bg-blue { 
  background-color: rgb(82 121 167);
}
</style>
