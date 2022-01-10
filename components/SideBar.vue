<template>
  <v-navigation-drawer v-model="drawer" color="white" app stateless permanent mini-variant mini-variant-width="80">
      <v-avatar class="d-block text-center mx-auto mt-4" color="" size="40">
        <v-icon color="#49D9A0" large>mdi-atlassian</v-icon>
      </v-avatar>
      <v-divider class="mx-3 my-5" style="border-color: #e1e1e1"></v-divider>
      <v-list flat class="mt-5">
        <v-list-item-group v-model="selectItem">
          <v-list-item active-class="border" :ripple="false" v-for="(item,index) in items" :key="index">
            <v-list-item-icon>
              <v-icon v-text="item.icon" color="#818384"></v-icon>
            </v-list-item-icon>
          </v-list-item>
        </v-list-item-group>
      </v-list>
      <div id="bell">
        <v-btn icon :ripple="false">
          <v-badge
            bordered
            overlap
            color="red"
            dot
          >
            <v-icon color="#818384">mdi-bell</v-icon>
          </v-badge>
        </v-btn>
      </div>
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
        {icon:'mdi-plus'},
        {icon:'mdi-grid-large'},
        {icon:'mdi-set-center'},
        {icon:'mdi-ballot'},
        {icon:'mdi-chart-line'},
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
<style scoped>
#bell{
  position: absolute;
  bottom: 20px;
  margin-left: auto;
  margin-right: auto;
  left: 0;
  right: 0;
  text-align: center
}
</style>

