<template>
    <p> Reaction Time was : {{score}} ms! </p>
    <p class="rank">{{rank}}</p>
</template>

<script>
export default {
    props: ["score"],
    data() {
    return {
    rank: null
    }
    },
    mounted() {
        if(this.score < 250) {
        this.rank = "WTF...Hot Fingers Reaction :)"
        } else if(this.score < 400) {
        this.rank = "Rapid Reflexes"
        } else {
        this.rank = "Hmmm was a normal reaction...!"
        }
    },
}
</script>

<style scoped>
.rank {
 font-size: 1.4em;
 color: green;
 font-weight: bold;
}
</style>