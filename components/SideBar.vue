<template>
  <v-navigation-drawer v-model="drawer" color="white" app mini-variant mini-variant-width="80">
      <v-avatar class="d-block text-center mx-auto mt-4">
        <v-icon color="#49D9A0" large>mdi-atlassian</v-icon>
      </v-avatar>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: 'SideBar',
  components: {},
  data(){
    return{
      selectItem: 0,
      drawer: null,
      items: [
        {icon:'plus'},
        {icon:'th-large'},
        {icon:'align-center'},
        {icon:'gitter'},
        {icon:'chart-line'},
      ]
    }
  }
}
</script>

<style>
.border  {
  margin-left: 12px;
  margin-right: 12px;
  background: #49D9A0 ;
  border-radius: 50%;
  text-decoration: none;

}
.v-list-item-group .v-list-item--active {
  color: white !important;
}
</style>

