<template>
  <div id="app">
    <Leftsizebar />
    <div class="body-right">
      <Header />
      <Content />
    </div>
    <div id="form" class="Tittle2">
      <Forminsize />
    </div>
  </div>
</template>

<script>
import Content from "./components/content";
import Header from "./components/header";
import Leftsizebar from "./components/leftsizebar";
import Forminsize from "./components/forminside";


export default {
  name: "app",
  components: {
    Leftsizebar,
    Header,
    Content,
    Forminsize,
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
}

#app {
  font-family: MISA-Regular, MISA-Bold, MISA-Italic;
  font-size: 13px;
  margin: 0px;
  padding: 0px;
  height: 100vh;
  display: flex;
}

@font-face {
  font-family: "MISA-Regular";
  src: url("./font/GoogleSans-Regular.otf") format("opentype");
}

@font-face {
  font-family: "MISA-Bold";
  src: url("./font/GoogleSans-Bold.otf") format("opentype");
}

@font-face {
  font-family: "MISA-Italic";
  src: url("./font/GoogleSans-Italic.otf") format("opentype");
}

.body-right {
  position: absolute;
  left: 201px;
  top: 0;
  right: 0;
  bottom: 0;
  height: 100vh;
  flex: 1;
}
#form {
  width: 100%;
  height: 100%;
  background-color: rgba(128, 128, 128, 0.5);
  position: absolute;
  z-index: 1000;
  display: none;
}

/*font chữ */
.Headerding {
  font-size: 24px;
  color: #000000;
  font-weight: bold;
}
.Tittle {
  font-size: 20px;
  color: #000000;
  font-weight: bold;
}
.Tittle2 {
  font-size: 15px;
  color: #000000;
  font-weight: bold;
}
.Label-i {
  font-size: 13px;
  color: #000000;
  font-weight: normal;
}

/*border radius 4px */
input {
  border-radius: 4px;
  height: 40px;
  padding: 0px 16px 4px 16px;
  margin-bottom: 16px;
  font-size: 13px;
  border: solid 1px #bbbbbb;
  outline: none;
  box-sizing: border-box;
}
</style>
