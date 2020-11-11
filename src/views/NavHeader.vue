<template>
  <div id="nav">
    <router-link to="/">Investment Dashboard</router-link> |
    <router-link to="/about">Explore</router-link>
    <button @click="createPortfolio">Create Portfolio</button>
    <CreatePortfolio v-if="showPortfolioForm"/>
  </div>
  <router-view/>
</template>

<script>

//import CreatePortfolio from '../components/CreatePortfolio';
import CreatePortfolio from '@/components/CreatePortfolio.vue'
    
export default {
  name: 'NavHeader',
  data: function() {
        return {
            showPortfolioForm: false
        }
    },
  components: {
    CreatePortfolio
  },
   methods: {
    createPortfolio: function() {
      console.log('inside create portfolio');
     this.showPortfolioForm  = true;
    }}
}

</script>