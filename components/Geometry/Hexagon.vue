<template>
  <div class="mx-[5px]">
    <div class="hexagon-background">
      <div class="hexagon"></div>
    </div>
  </div>
</template>

<script>

</script>

<style lang="scss" scoped>
.hexagon{
  z-index: 2;
  display: flex;
  justify-content: center;
  align-items: center;


  background-color:#ccc;
  height:45px;
  width:78px;
  
  position:relative;
}
.hexagon:before {
  content: '';
  background-color:#ccc;
  height:45px;
  width:78px;
  
  position:absolute;
  top: 0;
  left: 0;
  transform: rotate(120deg);
}
.hexagon:after {
  content: '';
  background-color:#ccc;
  height:45px;
  width:78px;
  
  position:absolute;
  top: 0;
  left: 0;
  transform: rotate(-120deg);
}

.hexagon-background{
  display: flex;
  justify-content: center;
  align-items: center;

  background-color:#ccc;
  height:45px;
  width:78px;
  
  position:relative;
}
.hexagon-background:before {
    content: '';
    background-color:#ccc;
  height:45px;
  width:78px;
  
  position:absolute;
  top: 0;
  left: 0;
  transform: rotate(120deg);
}
.hexagon-background:after {
    content: '';
    background-color:#ccc;
  height:45px;
  width:78px;
  
  position:absolute;
  top: 0;
  left: 0;
  transform: rotate(-120deg);
}

.hexagon-background, .hexagon-background:before, .hexagon-background:after {
  box-shadow: 5px 0px 5px 1px rgba(0, 0, 0, 0.1), -5px 0px 5px 1px rgba(0, 0, 0, 0.1);
  transition: box-shadow 0.35s ease-in-out;
}

.hexagon-background:hover, .hexagon-background:hover:before, .hexagon-background:hover:after {
  box-shadow: 5px 0px 5px 1px rgba(255, 0, 0, 0.5), -5px 0px 5px 1px rgba(255, 0, 0, 0.5);
}
</style>