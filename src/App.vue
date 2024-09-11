<script setup>
import "bootstrap/dist/js/bootstrap.min.js"
import "bootstrap/dist/css/bootstrap.min.css"
import "bootstrap-icons/font/bootstrap-icons.css";

import NaviBar from "@/components/NaviBar.vue";
import UerList from "@/components/UerList.vue";
import UserDetail from "@/components/UserDetail.vue";
</script>

<template>
  <div class="containerMain">
    <NaviBar></NaviBar>
    <UerList></UerList>
    <UserDetail></UserDetail>
  </div>
</template>

<style scoped>

.containerMain{
  //background-image: url("assets/background.png");
}
</style>
