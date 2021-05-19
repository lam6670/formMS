<template>
  <div class="forminside">
    <div class="forminsidetop">
      <div class="forminsidetopleft">Thông tin nhân viên</div>
      <div class="forminsidetopright"></div>
    </div>
    <div class="forminsidemid1">
      <div class="forminsidemid1left">
        <img src="../assets/default-avatar.jpg" alt="" />
        <p>Vui lòng chọn ảnh có định dạng</p>
        <p>.jpg, .jpeg, .png, .gif</p>
      </div>
      <div class="forminsidemid1mid">
        <p>Mã khách hàng <span class="redtxt">(*)</span></p>
        <input type="text" />
        <p>Mã thẻ thành viên</p>
        <input type="text" />
        <p>Ngày sinh</p>
        <input type="text" />
      </div>
      <div class="forminsidemid1right">
        <p>Mã khách hàng <span class="redtxt">(*)</span></p>
        <input type="text" />
        <p>Ma thẻ thành viên</p>
        <input type="text" />
        <p>Giới tính</p>
        <input type="radio" name="gender" />Nam
        <input type="radio" name="gender" />Nữ
        <input type="radio" name="gender" />Khác
      </div>
    </div>
    <div class="forminsidemid2">
      <div class="forminsidemid2top">
        <div class="forminsidemid2topleft">
          <p>Email</p>
          <input type="text">
          <p>Tên công ty</p>
          <input type="text">
        </div>
        <div class="forminsidemid2topright">
          <p>Số điện thoại <span class="redtxt">(*)</span></p>
          <input type="text">
          <p>Mã số thuế</p>
          <input type="text" placeholder="Mã số thuế của công ty">
        </div>
      </div>
      <div class="forminsidemid2bot">
          <p>Địa chỉ</p>
          <input type="text">
      </div>
    </div>
    <div class="forminsidebot">
      <div class="forminsidebotright">Lưu</div>
      <div class="forminsidebotleft">Hủy</div>
    </div>
  </div>
</template>

<script>

export default {

};
</script>

<style scoped>
.forminside {
  width: 800px;
  height: 650px;
  background: white;
  z-index: 10000;
  margin: 8% auto;
}

/*Chia layout cho form  - 3 Phần*/
/*Trên */
.forminside .forminsidetop {
  width: 100%;
  height: 50px;
  line-height: 50px;
  display: flex;
}
.forminside .forminsidetop .forminsidetopleft {
  flex: 1;
  height: 50px;
  padding-left: 20px ;
}
.forminside .forminsidetop .forminsidetopright {
  background-image: url("../assets/x.svg");
  width: 24px;
  background-repeat: no-repeat;
  height: 24px;
  opacity: 0.9;
}
.forminsidetopright:hover {
  opacity: 0.5 !important;
  cursor: pointer;
}

/*Giữa */
.forminsidemid1 {
  width: 100%;
  height: 300px;
  display: flex;
  justify-content: space-around;
}
.forminsidemid1 .forminsidemid1left {
  width: 30%;
  height: 250px;
  align-items: center;
  text-align: center;
}
.forminsidemid1 .forminsidemid1left img {
  width: 70%;
  margin-left: 5%;
  border-radius: 50%;
  border: solid 1px rgb(219, 219, 219);
}
.forminside .forminsidemid1mid {
  width: 30%;
  height: 250px;
}
.forminside .forminsidemid1right {
  width: 30%;
  height: 250px;
}

/*giữa 2 */
.forminside .forminsidemid2{
  width: 100%;
  height: 225px;
  padding: 0 16px;
  box-sizing: border-box;
  
}

.forminside .forminsidemid2 .forminsidemid2top{
  width: 100%;
  display: flex;
}

.forminside .forminsidemid2 .forminsidemid2topleft{
  width: 70%;
  height: 150px;
}

.forminside .forminsidemid2 .forminsidemid2topleft input{
  width: 90%!important;
}

.forminside .forminsidemid2 .forminsidemid2topright{
  width: 30%;
  height: 150px;
}

.forminside .forminsidemid2 .forminsidemid2bot{
  width: 100%;
  height: 75px;
}

.forminside .forminsidemid2 .forminsidemid2bot input{
  width: 96%;
}

/*Cuối */

.forminside .forminsidebot{
  width: 100%;
  height: auto;
  box-sizing: border-box;
  padding: 16px 24px;
  text-align: center;
  line-height: 40px;
}

.forminside .forminsidebot .forminsidebotright{
  width: 100px;
  height: 40px;
  background: #019160;
   float: right;
   color: white;
}

.forminside .forminsidebot .forminsidebotleft{
  width: 100px;
  height: 40px;
   float: right;
   margin-right: 12px;
}
/*chữ đỏ */
.redtxt {
  color: red;
}

/*Đổi màu border khi nhập ô input */
input:focus{
  border: 1px red solid;
}
</style>
