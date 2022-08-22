<template>
    <p>Reaction time: {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if(this.score < 200) {
            this.rank = 'Ninga finger'
        } else if (this.score < 400) {
            this.rank = 'Rapid reflexes'
        } else if (this.score < 600) {
            this.rank = 'little finger'
        } else {
            this.rank = 'Snail pace...'
        }
    }
}
</script>

<style>
  .rank {
    font-size: 1.4em;
    color: #0faf87;
    font-weight: bold;
  }
</style>