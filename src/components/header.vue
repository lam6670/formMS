<template>
  <div class="header Tittle2">
    <div class="headerleft">
      <select class="Tittle2" name="cars" id="cars" style="">
        <option value="volvo">Nhà hàng biển đông</option>
        <option value="saab">Nhà hàng Sao Hỏa</option>
        <option value="mercedes">Nhà hàng Kì Diệu</option>
        <option value="audi">Nhà hàng Thần kì</option>
      </select>
    </div>
    <div class="headerright">
      <img
        src="../assets/avatar-default.png"
        alt=""
        width="24px"
        height="24px"
      />
      nguyễn văn mạnh
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.header {
  width: 100%;
  height: 50px;
  border-bottom: 1px solid #bbbbbb;
  display: flex;
  /*đã padding*/
}

.header .headerleft {
  width: 80%;
  height: 50px;
  line-height: 30px;
}
.header .headerright {
  flex: 1;
  height: 50px;
  line-height: 30px;
  padding-right: 50px;
  text-align: right;
}

select {
  border: none;
  background: white;
  outline: none;
}
</style>