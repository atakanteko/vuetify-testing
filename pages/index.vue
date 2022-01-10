<template>
  <div>
    <SideBar />
    <SideBarRight />
  </div>
</template>

<script>
import SideBar from "../components/SideBar";
import SideBarRight from "../components/SideBarRight";
export default {
  name: 'IndexPage',
  components: {SideBarRight, SideBar}
}
</script>
