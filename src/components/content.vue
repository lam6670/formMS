<template>
  <div class="content">
    <div class="contenttop">
      <div class="contenttopleft">
        <p>Danh sách nhân viên</p>
      </div>
      <div class="contenttopright a-right"><button>Thêm nhân viên</button></div>
    </div>
    <div class="contentmid">
      <div class="contentmid1">
        <div class="contentmid1left">
          <input type="text" />hâhha <input type="text" />hâhha
          <input type="text" />hâhha
        </div>
        <div class="contentmid1right">
          <p>xoay xoay xoay</p>
        </div>
      </div>
      <div class="contentmid2">
        <table style="border-collapse: collapse">
          <thead>
            <tr>
              <th>Mã nhân viên</th>
              <th>Họ và tên</th>
              <th>Giới Tính</th>
              <th>Ngày Sinh</th>
              <th>Điện thoại</th>
              <th>Email</th>
              <th>Chức vụ</th>
              <th>Phòng ban</th>
              <th>Mức lương cơ bản</th>
              <th>Tình trạng công việc</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(Employees, index) in Employees" :key="index">
              <th>{{ Employees.EmployeeCode }}</th>
              <th>{{ Employees.FullName }}</th>
              <th>{{ Employees.Gender }}</th>
              <th>{{ Employees.DateOfBirth }}</th>
              <th>{{ Employees.PhoneNumber }}</th>
              <th>{{ Employees.Email }}</th>
              <th>{{ Employees.IdentityPlace }}</th>
              <th>{{ Employees.DepartmentName }}</th>
              <th>{{ Employees.Salary }}</th>
              <th>{{ Employees.WorkStatus }}</th>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
    <div class="contentbot"></div>
  </div>
</template>

<script>
const axios = require("axios");

export default {
  data() {
    return {
      Employees: [],
    };
  },
  created: async function () {
    // fetch data from a url endpoint
    const data = await axios.get("http://cukcuk.manhnv.net/v1/Employees");
    console.log(data);
    this.Employees = data.data;
    return data;
  },
};
</script>

<style scoped>

/*table */
table tr {
  height: 30px;
}

table tr:nth-child(even){
  background-color: #dddddd;
}

/*chia và style cho content */
.content {
  position: absolute;
  top: 51px;
  right: 0;
  bottom: 0;
  left: 0;
}

.contenttop {
  width: 100%;
  height: 50px;
  line-height: 50px;
  display: flex;
}

.contenttopleft {
  width: 80%;
  height: 50px;
}
.contenttopright {
  flex: 1;
  height: 50px;
}

.contentmid {
  width: 100%;
  height: 800px;
}
.contentmid1 {
  width: 100%;
  height: 60px;
  display: flex;
}
.contentmid1left {
  width: 80%;
  height: 60px;
}
.contentmid1right {
  width: 20%;
  height: 60px;
  flex: 1;
}
.contentmid2 {
  width: 100%;
  height: 740px;
  overflow: scroll;
}
.contentmid2 table {
  padding: 10px;
  width: 100%;
  text-align: left;
}

.contentbot {
  width: 100%;
  height: 50px;
}

/*dùng chung */
.a-right {
  right: 0px;
  position: absolute;
}

.p-right-30 {
  padding-right: 30px;
}
</style>