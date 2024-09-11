<script>
export default {
  name: "UserDetail"
}
</script>

<template>
  <div class="UserDetail">

    <h4>User Detail</h4>

    <div class="row">
      <div class="col-xs-12">
        <div class="switch">
          <input type="radio" name="tripple" value="Y" class="switch-input" id="switch-y">
          <label for="switch-y" class="switch-label switch-label-y">Info</label>
          <input type="radio" name="tripple" value="I" class="switch-input" id="switch-i">
          <label for="switch-i" class="switch-label switch-label-i">Password</label>
          <input type="radio" name="tripple" value="N" class="switch-input" id="switch-n">
          <label for="switch-n" class="switch-label switch-label-n">History</label>

          <span class="switch-selector"></span>
        </div>
      </div>
    </div>
    <div class="infoList">
      <div class="inputGroup">
        <label for="infoId">ID</label>
        <input id="infoId" type="text" value="Userid1" readonly>
      </div>

      <div class="inputGroup">
        <label for="infoName">Name</label>
        <input id="infoName" type="text" value="Userid1" readonly>
      </div>

      <div class="inputGroup">
        <label for="infoEmail">Email</label>
        <input id="infoEmail" type="text" value="user@gmail.com" readonly>
      </div>

      <div class="inputGroup">
        <label for="infoInterval">Default interval</label>
        <input id="infoInterval" type="text" value="9" readonly>
      </div>

      <div class="inputGroup">
        <label for="infoLanguage">Language</label>
        <input id="infoLanguage" type="text" value="English" readonly>
      </div>

      <div class="inputGroup">
        <label for="infoMailing">Notification Mailing</label>
        <input id="infoMailing" type="text" value="Option1" readonly>
      </div>

      <div class="inputGroup">
        <label for="infoPush">Notification Push</label>
        <input id="infoPush" type="text" value="SNS" readonly>
      </div>

      <div class="inputGroup">
        <label for="infoBlock" class="infoBlockLabel">Block user</label>

        <input class="infoBlock" id="infoBlock" type="checkbox" role="switch">
      </div>
    </div>
  </div>
</template>

<style scoped>
.UserDetail{
  position: absolute;
  width: 440px;
  height: 100%;
  background-color: var(--white);
  right: 0;
  padding: var(--padding-xxlarge);
  box-shadow: var(--shadow);
}

.switch {
  position: relative;
  height: 32px;
  width: 360px;
  margin: 20px auto;
  border-radius: var(--radius-small);
  background-color: var(--gray8);
  //box-shadow: var(--shadow);
}
.switch-label {
  //font-weight: bold;
  position: relative;
  z-index: 2;
  float: left;
  width: 120px;
  line-height: 32px;
  font-size: 12px;
  color: var(--gray3);
  text-align: center;
  cursor: pointer;
}

.switch-input {
  display: none;
}

.switch-input:checked + .switch-label {
  color: var(--black);
  transition: 0.15s ease-out;
  transition-property: color, text-shadow;
}

.switch-input:checked + .switch-label-y ~ .switch-selector {
  transform: translateX(0%);
  background-color: var(--white);
}
.switch-input:checked + .switch-label-i ~ .switch-selector {
  transform: translateX(100%);
  background-color: var(--white);
}
.switch-input:checked + .switch-label-n ~ .switch-selector {
  transform: translateX(200%);
  background-color: var(--white);
}
.switch-selector {
  position: absolute;
  z-index: 1;
  //top: 0px;
  //left: 0px;
  display: block;
  width: 120px;
  height: 32px;
  border-radius: var(--radius-small);
  background-color: var(--white);
  transition: all 0.3s cubic-bezier(0.18, 0.89, 0.32, 1.28);
  box-shadow: var(--shadow);
}
input {
  border: none;
}
</style>