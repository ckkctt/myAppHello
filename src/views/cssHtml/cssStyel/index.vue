<template>
  <div class="cssStyelWarp">
    <div class="cssStyel1">
      <!-- 圆形 -->
      <section id="circle"></section>
      <!-- 上三角 -->
      <section id="triangle-up"></section>
      <!-- 左上角 -->
      <section id="triangle-topleft"></section>
      <!-- 梯型 -->
      <section id="trapezoid"></section>
      <!-- 平行四边形 -->
      <section id="parallelogram"></section>

    </div>
    <div class="cssStyel2">
      <!-- 星星 (5角) -->
      <section id="star-five"></section>
       <!-- 爱心 -->
      <section id="heart"></section>
    </div>
  </div>
</template>

<style scoped>
.cssStyelWarp {
  padding: 20px;
}
.cssStyel1 {
  display: flex;
  justify-content: flex-start;
  /* background: rgb(138, 136, 134); */
}
.cssStyel2 {
  display: flex;
  margin-top: 20px;
  justify-content: flex-start;
  /* background: rgb(111, 131, 221); */
}
section:nth-child(n) {
  margin-left: 10px;
}
#circle {
  width: 20px;
  height: 20px;
  background: rgb(40, 100, 12);

  border-radius: 50%;
}
#triangle-up {
  width: 0;
  height: 0;
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  border-bottom: 20px solid rgb(40, 100, 12);
}
#triangle-topleft {
  width: 0;
  height: 0;
  border-top: 20px solid rgb(40, 100, 12);
  border-right: 20px solid transparent;
}
#trapezoid {
  border-bottom: 20px solid rgb(40, 100, 12);
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  height: 0;
  width: 20px;
}

#parallelogram {
  width: 30px;
  height: 20px;
  transform: skew(15deg);
  background: rgb(40, 100, 12);
}

/* 五角星 */
#star-five {
  margin: 50px 0;
  position: relative;
  display: block;
  color: red;
  width: 0px;
  height: 0px;
  border-right: 100px solid transparent;
  border-bottom: 70px solid red;
  border-left: 100px solid transparent;
  transform: rotate(35deg);
}
#star-five:before {
  border-bottom: 80px solid red;
  border-left: 30px solid transparent;
  border-right: 30px solid transparent;
  position: absolute;
  height: 0;
  width: 0;
  top: -45px;
  left: -65px;
  display: block;
  content: "";
  transform: rotate(-35deg);
}
#star-five:after {
  position: absolute;
  display: block;
  color: red;
  top: 3px;
  left: -105px;
  width: 0px;
  height: 0px;
  border-right: 100px solid transparent;
  border-bottom: 70px solid red;
  border-left: 100px solid transparent;
  transform: rotate(-70deg);
  content: "";
}
/* 爱心 */
#heart {
  position: relative;
  width: 100px;
  height: 90px;
}
#heart:before,
#heart:after {
  position: absolute;
  content: "";
  left: 50px;
  top: 0;
  width: 50px;
  height: 80px;
  background: red;
  border-radius: 50px 50px 0 0;
  transform: rotate(-45deg);
  transform-origin: 0 100%;
}
#heart:after {
  left: 0;
  transform: rotate(45deg);
  transform-origin: 100% 100%;
}
</style>
