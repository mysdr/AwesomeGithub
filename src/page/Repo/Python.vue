<template>
  <div id="app">
    <user v-bind:query="query" :type="type"></user>
  </div>
</template>

<script>
    import User from "@/components/Repo"
    export default {
        name: 'app',
        data(){
            return {
                query:"https://api.github.com/search/repositories?q=language:Python&sort=stars&order=desc", //查询全球用户排名 query of global ranking.
                type:"Python"
            }
        },
        components: {
            "user":User,
        }
    }
</script>

<style>

</style>
