<script src="https://unpkg.com/vue/dist/vue.js"></script>
<script src="https://unpkg.com/vue-router/dist/vue-router.js"></script>

<template>
  <v-app>
    <v-navigation-drawer app v-model="drawer" clipped>
      <v-container>

    <v-list-item>
      <v-list-item-content>
        <v-list-item-title class="title grey--text text--darken-2">
          Navigation lists
        </v-list-item-title>
      </v-list-item-content>
    </v-list-item>

    <v-divider></v-divider>

    <v-list dense nav>
      <v-list-item v-for="nav_list in nav_lists" :key="nav_list.id" v-scroll-to="nav_list.id" :href="nav_list.href">
        <v-list-item-icon>
          <v-icon>{{ nav_list.icon }}</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
          <v-list-item-title>{{ nav_list.name }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-container>
  </v-navigation-drawer>

  <v-app-bar color="light-blue lighten-3 "  yellow  app clipped-left>
      <v-app-bar-nav-icon @click="drawer=!drawer" ></v-app-bar-nav-icon>
      <v-tabs
    icons-and-text
    centered>

      <div v-for="nav_list in nav_lists" :key="nav_list.id" v-scroll-to="nav_list.id" class="tablink">
    <a :href="nav_list.href"><v-tab   class="d-none d-sm-flex">
    {{nav_list.name}}
    <v-icon>{{ nav_list.icon }}</v-icon>
    </v-tab></a>
    </div>
    </v-tabs>
  </v-app-bar>

<v-main>
<Aboutme/>
  <v-container class="main1">
<Skill/>
<Journey/>
<Active/>
<Now/>

  </v-container>
</v-main>

  </v-app>
</template>

<style>
html { scroll-behavior: smooth;}

.v-responsive__content{
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
}

.v-responsive__content img{
width:80%;
height:500px;
border:solid 10px #0093E9;
}

@media screen and (max-width: 900px){
.v-responsive__content img{
width:100%;
height:auto;
}
}

.about{
  display: flex;
  text-align: center;

}
.about ul{
  list-style: none;
}
.tablink a{
text-decoration:none;
display: block;
padding-top:6px;
}
.top{
  height:100vh;
  background-color: #0093E9;
background-image: linear-gradient(160deg, #0093E9 0%, #80D0C7 100%);
text-align: center;
line-height: 300px;
color: #FFF;
}
.main1 h1{
  font-size:40px;
  border-bottom: solid 2px #0093E9;
  color: #0093E9;
  width:70%;
  margin:0 auto;
}
</style>
<script>
import Aboutme from '@/views/Aboutme.vue'
import Skill from '@/views/Skill.vue'
import Journey from '@/views/Journey.vue'
import Active from '@/views/Active.vue'
import Now from '@/views/Now.vue'

export default {
  name: 'app',
  components:{
    Aboutme,
    Skill,
    Journey,
    Active,
    Now
  },
  data () {
    return {
      drawer: null,
      nav_lists: [
        { name: 'TOP', icon: 'mdi-home', href: '#', id: '#' },
        { name: 'ABOUT ME', icon: 'mdi-account-circle-outline', href: '#about', id: '#about' },
        { name: 'SKILL', icon: 'mdi-monitor', href: '#skill', id: '#skill' },
        { name: 'JOURNEY', icon: 'mdi-racing-helmet', href: '#journey', id: '#journey' },
        { name: 'ACTIVE', icon: 'mdi-tablet-android', href: '#active', id: '#active' },
        { name: 'NOW', icon: 'mdi-cards-heart', href: '#now', id: '#now' }
      ]
    }
  }
}
</script>
