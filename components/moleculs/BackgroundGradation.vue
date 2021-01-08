<template>
<div>
    <div class="grad1"></div>
    <div class="grad2"></div>
    <div class="grad3"></div>   
</div>
</template>

<style lang="scss">
.grad1,
.grad2,
.grad3 {
  width: 100%;
  height: 100%;
  position: absolute;
}
.grad2,
.grad3 {
  opacity: 0;
}
.grad1 {
  background: linear-gradient(#3d3d3d40, #b3b0b040);
  animation: grad1 5s infinite;
}
.grad2 {
  background: linear-gradient(#2e2e2e40, #64636340);
  animation: grad2 5s infinite;
  animation-delay: 5s;
}
.grad3 {
  background: linear-gradient(#72727240, #10111140);
  animation: grad3 5s infinite;
  animation-delay: 3s;
}
@keyframes grad1 {
  0% {
    opacity: 1;
  }
  10% {
    opacity: 0.8;
  }
  20% {
    opacity: 0.6;
  }
  30% {
    opacity: 0.4;
  }
  40% {
    opacity: 0.2;
  }
  50% {
    opacity: 0.1;
  }
  60% {
    opacity: 0.2;
  }
  70% {
    opacity: 0.4;
  }
  80% {
    opacity: 0.6;
  }
  90% {
    opacity: 0.8;
  }
  100% {
    opacity: 1;
  }
}
@keyframes grad2 {
  0% {
    opacity: 0;
  }
  10% {
    opacity: 0.2;
  }
  20% {
    opacity: 0.4;
  }
  30% {
    opacity: 0.6;
  }
  40% {
    opacity: 0.8;
  }
  50% {
    opacity: 1;
  }
  60% {
    opacity: 0.8;
  }
  70% {
    opacity: 0.6;
  }
  80% {
    opacity: 0.4;
  }
  90% {
    opacity: 0.2;
  }
  100% {
    opacity: 0;
  }
}
@keyframes grad3 {
  0% {
    opacity: 1;
  }
  10% {
    opacity: 0.8;
  }
  20% {
    opacity: 0.6;
  }
  30% {
    opacity: 0.4;
  }
  40% {
    opacity: 0.2;
  }
  50% {
    opacity: 0.1;
  }
  60% {
    opacity: 0.2;
  }
  70% {
    opacity: 0.4;
  }
  80% {
    opacity: 0.6;
  }
  90% {
    opacity: 0.8;
  }
  100% {
    opacity: 1;
  }
}

</style>