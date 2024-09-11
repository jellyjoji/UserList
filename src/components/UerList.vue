
<template>
  <div class="containers">

    <header>
      <div class="containerHeader">

        <div class="breadcrumbs">Account  &nbsp;  &nbsp;/ <span> &nbsp; &nbsp; User</span> </div>

        <div class="isTitle">
          <div class="isAdd">
            <h1>User</h1>
            <img src="../assets/Button.svg" alt="plus" style="cursor: pointer; height: 2.5rem;">
          </div>

          <button  type="button" class="buttonStart" style="font-size: 15px;">
            <i class="bi bi-trash"></i>
            Delete
            <span class="badge" style=" color: var(--black); background-color:var(--white); border-radius: 50px">
              5
            </span>
          </button>
        </div>
      </div>
    </header>

    <main>

      <nav>
        <div id="nav-tab" class="nav nav-tabs" role="tablist">
          <button id="nav-user-tab" class="tabs">
            User
          </button>
          <button id="nav-invite-tab" class="tabs">
            Invitation
          </button>
        </div>
      </nav>
      <div id="nav-tabContent" class="tab-content">
        <div id="nav-user" class="tab-pane fade show active" role="tabpanel" aria-labelledby="nav-user-tab">

          <div class="total">
            Total
<!--            <span class="badge number">{{ totalCount }}</span>-->
            <span class="badge number">29</span>
          </div>

          <table>
            <thead >
              <!--              <tr></tr>-->
              <tr >
                <!--                <th>-->
                <!--                  <input v-model="selectAll" type="checkbox" @change="toggleAllCheck">-->
                <!--                </th>-->
                <th scope="col">
                  Name
                </th>
                <th  scope="col">ID</th>
                <th scope="col">Email</th>
                <th scope="col">Group</th>
                <th scope="col">Register</th>
                <th scope="col">Status</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(user, index) in userList" :key="user.id">
                <!--                <td>-->
                <!--                  <input v-model="user.selected" type="checkbox" @change="updateCount">-->
                <!--                </td>-->
                <td :id="user.id + index">{{ user.name }}</td>

                <td>{{ user.id }}</td>
                <td>{{ user.email }}</td>
                <td>
                  <span v-for="group in user.groups" class="badge badges" :class="getGroup(group)">{{ group }}</span>
                </td>
                <td>
                  {{ user.registerDate }}
                </td>
                <td>
<!--                  <span class="badges" :class="isBlocked? 'error':'inUse'">-->
<!--                  {{ user.block }}-->
<!--                  </span>-->
                                    <div v-if="user.block" class="badge blocked">Blocked</div>
                                    <div v-else class="badge unBlocked">In use</div>
                </td>
              </tr>
            </tbody>
          </table>
          <div class="showOlder" style="font-size: 15px; font-weight: 500;">
            <img src="../assets/chevron-down.svg" alt="show older" style="width: 1.5rem ; height: 1.5rem;">
            Show Older</div>
        </div>
      </div>
    </main>

  </div>
</template>

<script>

export default {
  data() {
    return {
      isBlocked:true,
      isVisible: false,
      totalCount: 0,
      selectedCount: 0,
      selectAll: false,
      items: [],
      // userList: null,
      userList:
          [
            {
              "id": "Userid1",
              "name": "Name1",
              "email": "user@gmail.com",
              "confirm": true,
              "block": "Blocked",
              "groups": ["Admin","Users"],
              "role": "User",
              "lastLogin": "2023-11-15 18:25:24",
              "registerDate": "2023-08-11 14:47:19",
              "modifyDate": "2023-10-31 13:40:38",
              "config": {
                "landing": "Overview",
                "language": "ko_KR",
                "notify_push": "Info",
                "notify_email": "Off",
                "dashboard_range": 3600000,
                "dashboard_interval": 10000
              }
            },
            {
              "id": "Userid1",
              "name": "Name1",
              "email": "user@gmail.com",
              "confirm": true,
              "block": "Blocked",
              "groups": ["Admin","Users"],
              "role": "User",
              "lastLogin": "2023-11-15 18:25:24",
              "registerDate": "2023-08-11 14:47:19",
              "modifyDate": "2023-10-31 13:40:38",
              "config": {
                "landing": "Overview",
                "language": "ko_KR",
                "notify_push": "Info",
                "notify_email": "Off",
                "dashboard_range": 3600000,
                "dashboard_interval": 10000
              }
            },
            {
              "id": "Userid1",
              "name": "Name1",
              "email": "user@gmail.com",
              "confirm": true,
              "block": "",
              "groups": ["Admin","Users"],
              "role": "User",
              "lastLogin": "2023-11-15 18:25:24",
              "registerDate": "2024-03-21 12:34:56",
              "modifyDate": "2023-10-31 13:40:38",
              "config": {
                "landing": "Overview",
                "language": "ko_KR",
                "notify_push": "Info",
                "notify_email": "Off",
                "dashboard_range": 3600000,
                "dashboard_interval": 10000
              }
            },
            {
              "id": "Userid1",
              "name": "Name1",
              "email": "user@gmail.com",
              "confirm": true,
              "block": "",
              "groups": ["Admin","Users"],
              "role": "User",
              "lastLogin": "2023-11-15 18:25:24",
              "registerDate": "2024-03-21 12:34:56",
              "modifyDate": "2023-10-31 13:40:38",
              "config": {
                "landing": "Overview",
                "language": "ko_KR",
                "notify_push": "Info",
                "notify_email": "Off",
                "dashboard_range": 3600000,
                "dashboard_interval": 10000
              }
            },
            {
              "id": "Userid1",
              "name": "Name1",
              "email": "user@gmail.com",
              "confirm": true,
              "block": "Blocked",
              "groups": ["Admin","Users"],
              "role": "User",
              "lastLogin": "2023-11-15 18:25:24",
              "registerDate": "2023-08-11 14:47:19",
              "modifyDate": "2023-10-31 13:40:38",
              "config": {
                "landing": "Overview",
                "language": "ko_KR",
                "notify_push": "Info",
                "notify_email": "Off",
                "dashboard_range": 3600000,
                "dashboard_interval": 10000
              }
            },
            {
              "id": "Userid1",
              "name": "Name1",
              "email": "user@gmail.com",
              "confirm": true,
              "block": "Blocked",
              "groups": ["Admin","Users"],
              "role": "User",
              "lastLogin": "2023-11-15 18:25:24",
              "registerDate": "2023-08-11 14:47:19",
              "modifyDate": "2023-10-31 13:40:38",
              "config": {
                "landing": "Overview",
                "language": "ko_KR",
                "notify_push": "Info",
                "notify_email": "Off",
                "dashboard_range": 3600000,
                "dashboard_interval": 10000
              }
            },
            {
              "id": "Userid1",
              "name": "Name1",
              "email": "user@gmail.com",
              "confirm": true,
              "block": "Blocked",
              "groups": ["Admin","Users"],
              "role": "User",
              "lastLogin": "2023-11-15 18:25:24",
              "registerDate": "2023-08-11 14:47:19",
              "modifyDate": "2023-10-31 13:40:38",
              "config": {
                "landing": "Overview",
                "language": "ko_KR",
                "notify_push": "Info",
                "notify_email": "Off",
                "dashboard_range": 3600000,
                "dashboard_interval": 10000
              }
            },
            {
              "id": "Userid1",
              "name": "Name1",
              "email": "user@gmail.com",
              "confirm": true,
              "block": "Blocked",
              "groups":["Admin","Users"],
              "role": "User",
              "lastLogin": "2023-11-15 18:25:24",
              "registerDate": "2023-08-11 14:47:19",
              "modifyDate": "2023-10-31 13:40:38",
              "config": {
                "landing": "Overview",
                "language": "ko_KR",
                "notify_push": "Info",
                "notify_email": "Off",
                "dashboard_range": 3600000,
                "dashboard_interval": 10000
              }
            },
            {
              "id": "Userid1",
              "name": "Name1",
              "email": "user@gmail.com",
              "confirm": true,
              "block": "Blocked",
              "groups": ["Admin"],
              "role": "User",
              "lastLogin": "2023-11-15 18:25:24",
              "registerDate": "2023-08-11 14:47:19",
              "modifyDate": "2023-10-31 13:40:38",
              "config": {
                "landing": "Overview",
                "language": "ko_KR",
                "notify_push": "Info",
                "notify_email": "Off",
                "dashboard_range": 3600000,
                "dashboard_interval": 10000
              }
            },
            {
              "id": "Userid1",
              "name": "Name1",
              "email": "user@gmail.com",
              "confirm": true,
              "block": "Blocked",
              "groups": ["Users"],
              "role": "User",
              "lastLogin": "2023-11-15 18:25:24",
              "registerDate": "2023-08-11 14:47:19",
              "modifyDate": "2023-10-31 13:40:38",
              "config": {
                "landing": "Overview",
                "language": "ko_KR",
                "notify_push": "Info",
                "notify_email": "Off",
                "dashboard_range": 3600000,
                "dashboard_interval": 10000
              }
            },
          ]
      ,
      newUser: {
        id: "",
        name: "",
        password: "",
        email: "",
        role: "User",
        config: {
          landing: "Overview",
          language: "en_US",
          notify_email: "Off",
          notify_push: "Info",
          dashboard_interval: 10,
          dashboard_timeRange: 3600000
        },
      },
      newUserString: null,
    }
  },
  computed: {

  },
  created() {
    this.getUser()
    this.items = [
      {
        text: 'account',
        path: 'Users'
      },
      {
        text: 'user',
        path: 'Users'
      },
    ]
  },
  methods: {
    open() {
      this.isVisible = !this.isVisible
    },
    // convertTime(value, zone) {
    //   return utils.convertTimeToString(value, zone)
    // },
    async getUser() {
      // let response = await api.findUserList()
      // if (response && response.status === 200) {
      //   this.userList = response.data.data
        this.totalCount = this.userList.length
        console.log(this.userList)
      // }
    },
    toggleAllCheck() {
      this.userList.forEach(user => (user.selected = this.selectAll));
      this.updateCount()
    },
    updateCount() {
      this.selectedCount = this.userList.filter(user => user.selected).length
    },
    getGroup(group) {
      if (group === 'Admin') {
        return 'admin'
      } else if (group === 'Users') {
        return 'users'
      } else {
        return 'optional'
      }
    },
  }
}
</script>

<style scoped>

.isGroup span {
  margin-right: var(--padding-small);
}

tr {
  border-top: 1px solid var(--gray7);
  border-bottom: 1px solid var(--gray7);
}

th, td {
  //width: 4rem;
  padding-left: 1rem;
  //border: 1px solid red;
  //background-color: pink;
}

th:first-child, td:first-child {
  color: var(--black);
  width: 420px;
  font-weight: 600;
}
th:nth-child(2), td:nth-child(2){
  width: 200px;
}
th:nth-child(3), td:nth-child(3){
  width: 200px;
}

th:nth-child(4), td:nth-child(4){
  width: 180px;
}
th:nth-child(5), td:nth-child(5){
  width: 200px;
}
th:nth-child(6), td:nth-child(6){
  width: 60px;
}
#nav-user-tab {
  color: var(--color-primary);
  border-bottom: 0.2rem solid var(--color-primary);
}
#nav-invite-tab{
  color: var(--black);
}

table {
  color: var(--gray3);
  //opacity: 0.3;
}

.number{
  color: var(--color-primary);
  border-radius: 50px;
  font-weight: 400;
}
h1{
  font-weight: 500;
  font-size: 60px;
}
.showOlder{
  line-height: 3rem;
  text-align: center;
}
.breadcrumbs{
  line-height: 1rem ;
  color: #6B7280;
}
.breadcrumbs span{
  color: var(--black);
}

.blocked{
  color: var(--red700);
}
.unBlocked, .admin{
  color: var(--green700);
}
.users{
  color: var(--color-primary);
}
.optional{
  color: var(--gray3);
}
.badge{
  font-size: 12px;
  font-weight: 500;
  padding: var(--padding-xsmall);
}
.badges{
  padding: var(--padding-small);
  border-radius: 100px;
  margin-right: 0.4rem;
  font-weight: 500;
}
.bi{
  margin-right: 0.5rem;
}
.tabs{
  padding: 0 1rem;
  font-size: 14px;
}
</style>
