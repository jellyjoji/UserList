<script>
export default {
  name: "NaviBar"
}
</script>

<template>
  <nav>
    <div>
    <div class="logo">
      <img src=".././assets/logo.svg" alt="logo" style="width: 24px; height: 24px; margin-right: 1rem;">
      <h1>ArkData</h1>
    </div>
    <div class="profile">
     <div class="profileLeft">
       <i class="bi bi-bell" style="font-size: 24px; padding-left: 4px;"></i>
       <div class="badge number">2</div>
       Jihyun Jojina
     </div>
      <div class="profileRight">
        <i class="bi bi-list"></i>
      </div>
    </div>
    <div class="category">
      <div class="list">
<!--      <i class="bi bi-house-door"></i>-->
        <img src="../assets/icons/dashboard.svg" alt="dashboard">
        Dashboard
      </div>
      <div class="list">
<!--        <i class="bi bi-bar-chart"></i>-->
        <img src="../assets/icons/overview.svg" alt="overview">
        Overview
      </div>
      <div class="list">
        <div class="subTitle">
        Configuration
        <i class="bi bi-chevron-down"></i>
        </div>
        <div class="subList">
          <div>
<!--            <i class="bi bi-database"></i>-->
            <img src="../assets/icons/agent.svg" alt="agent">
            Agent
          </div>
          <div>
<!--            <i class="bi bi-database"></i>-->
            <img src="../assets/icons/module.svg" alt="module">
            Module
          </div>
          <div>
<!--            <i class="bi bi-diagram-3"></i>-->
            <img src="../assets/icons/pipeline.svg" alt="pipeline">
            Pipeline
          </div>
        </div>
      </div>

      <div class="list">
        <div class="subTitle">
          Account
          <i class="bi bi-chevron-down"></i>
        </div>
        <div class="subList">
          <div>
<!--            <i class="bi bi-person"></i>-->
            <img src="../assets/icons/user.svg" alt="user">
            User
          </div>
          <div>
<!--            <i class="bi bi-person-bounding-box"></i>-->
            <img src="../assets/icons/group.svg" alt="group">
            Group
          </div>
          <div>
<!--            <i class="bi bi-person-check"></i>-->
            <img src="../assets/icons/permission.svg" alt="permission">
            Permission
          </div>
        </div>
      </div>

      <div class="list">
        <div class="subTitle">
          Admin
          <i class="bi bi-chevron-down"></i>
        </div>
        <div class="subList">
          <div>
<!--            <i class="bi bi-gear"></i>-->
            <img src="../assets/icons/user.svg" alt="user">
            Server settings
          </div>
          <div>
<!--            <i class="bi bi-person-gear"></i>-->
            <img src="../assets/icons/group.svg" alt="group">
            User settings
          </div>
          <div>
<!--            <i class="bi bi-clock-history"></i>-->
            <img src="../assets/icons/permission.svg" alt="permission">
            Login history
          </div>
        </div>
      </div>

    </div>
    </div>
    <footer>
      <div class="list">
        <div class="footerList">
          <div>
            <div class="badge extract" style="color: var(--color-primary); border-radius: 50px; padding: 0.4rem">V 2.2.0</div>
          </div>
          <i class="bi bi-arrow-bar-left"></i>
        </div>
      </div>
      <small>Copyrights(C) 2019 Arkdata Ltd.</small>
    </footer>
  </nav>
</template>

<style scoped>

nav{
  width: 294px;
  padding: 3px 20px 20px 28px;
  border: 1px solid var(--gray7);
  font-size: 14px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
img{
  width: 20px;
  height: 20px;
  margin-right: 0.5rem;
}

.logo{
  display: flex;
  //justify-content: space-around;
  align-items: center;
  height: 4rem;
}
h1{
  font-size: 26px;
  font-weight: 700;
  height: 24px;
}
.profile{
  display: flex;
  justify-content: space-between;
  border-top: 1px solid var(--gray7);
  border-bottom: 1px solid var(--gray7);
  line-height: 3.5rem;
}
.category{
  display: flex;
  flex-direction: column;
  //border: 1px solid crimson;
}
.list{
  line-height: 2.6rem;
  //border-left: var(--gray7);
}
.subTitle{
  display: flex;
  justify-content: space-between;
  cursor: pointer;
}
.subList{
  padding-left: 1rem;
  margin-left: 1rem;
  border-left: 2px solid var(--gray6);
}
.bi{
  margin-right: 0.5rem;
}
.number{
  background-color: var(--red700);
  font-weight: 300;
  border-radius: 50px;
  position: absolute;
  left: 46px;
  top: 82px;
}

.footerList{
  display: flex;
  align-items: center;
  justify-content: space-between;
}
small{
  color: var(--gray4);
  font-size: 14px;
}

</style>