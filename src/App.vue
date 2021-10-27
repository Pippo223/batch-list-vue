<template>
  <div>
    <!-- <the-header></the-header> -->
    <TheHeader/>
    <button @click="setSelectedComponent('active-goals')">Active Goals</button>
    <button @click="setSelectedComponent('manage-goals')">Manage Goals</button>
    
    <!-- <ActiveGoals v-if="selectedComponent === 'active-goals'"/>
    <ManageGoals v-if="selectedComponent === 'manage-goals'"/> -->

  <keep-alive>
    <component :is="selectedComponent"></component>  
  </keep-alive>
    
    <!-- <badge-list></badge-list>
    <user-info
      :full-name="activeUser.name"
      :info-text="activeUser.description"
      :role="activeUser.role"
    ></user-info> -->
    <!-- <course-goals #default="slotProps">
      <h2>{{ slotProps.item }}</h2>
      <p>{{ slotProps.another }}</p>
    </course-goals> -->

  </div>
</template>

<script>
// import CourseGoals from './components/CourseGoals.vue';
import TheHeader from './components/TheHeader.vue';
import ActiveGoals from './components/ActiveGoals.vue';
import ManageGoals from './components/ManageGoals.vue';
// import BadgeList from './components/BadgeList.vue';
// import UserInfo from './components/UserInfo.vue';


export default {
  components: {
    //'the-header': TheHeader
    TheHeader,
    ManageGoals,
    ActiveGoals
    // BadgeList,
    // UserInfo,
  // CourseGoals
  },

  data() {
    return {
      selectedComponent: 'active-goals',

      activeUser: {
        name: 'Maximilian Schwarzmüller',
        description: 'Site owner and admin',
        role: 'admin',
      },
    };
  },

methods: {
  setSelectedComponent(cmp) {
    this.selectedComponent = cmp;
  }
}

};
</script>

<style>
html {
  font-family: sans-serif;
}

body {
  margin: 0;
}
</style>