<template>
  <div class="container">
    <h1>
      Coding is
      <span class="typed-text">{{ typeValue }}</span>
      <span class="cursor" :class="{ typing: typeStatus }">&nbsp;</span>
    </h1>
  </div>
</template>

<script>
import { setTimeout } from "timers";
export default {
  data: () => {
    return {
      typeValue: "",
      typeStatus: false,
      typeArray: ["fun", "awesome", "a journey", "life"],
      typingSpeed: 200,
      erasingSpeed: 100,
      newTextDelay: 2000,
      typeArrayIndex: 0,
      charIndex: 0,
    };
  },
  methods: {
    typeText() {
      if (this.charIndex < this.typeArray[this.typeArrayIndex].length) {
        if (!this.typeStatus) this.typeStatus = true;
        this.typeValue += this.typeArray[this.typeArrayIndex].charAt(
          this.charIndex
        );
        this.charIndex += 1;
        setTimeout(this.typeText, this.typingSpeed);
      } else {
        this.typeStatus = false;
        setTimeout(this.eraseText, this.newTextDelay);
      }
    },
    eraseText() {
      if (this.charIndex > 0) {
        if (!this.typeStatus) this.typeStatus = true;
        this.typeValue = this.typeArray[this.typeArrayIndex].substring(
          0,
          this.charIndex - 1
        );
        this.charIndex -= 1;
        setTimeout(this.eraseText, this.erasingSpeed);
      } else {
        this.typeStatus = false;
        this.typeArrayIndex += 1;
        if (this.typeArrayIndex >= this.typeArray.length)
          this.typeArrayIndex = 0;
        setTimeout(this.typeText, this.typingSpeed + 1000);
      }
    },
  },
  created() {
    setTimeout(this.typeText, this.newTextDelay + 200);
  },
};
</script>

<style scoped>
.container {
  width: 100%;
  height: 100vh;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
}

h1 {
  font-size: 6rem;
  font-weight: normal;
}

h1 span.typed-text {
  color: #d2b94b;
}

h1 span.cursor {
  display: inline-block;
  margin-left: 3px;
  width: 4px;
  background-color: #fff;
  -webkit-animation: cursorBlink 1s infinite;
  animation: cursorBlink 1s infinite;
}

h1 span.cursor.typing {
  -webkit-animation: none;
  animation: none;
}

@-webkit-keyframes cursorBlink {
  49% {
    background-color: #fff;
  }
  50% {
    background-color: transparent;
  }
  99% {
    background-color: transparent;
  }
}

@keyframes cursorBlink {
  49% {
    background-color: #fff;
  }
  50% {
    background-color: transparent;
  }
  99% {
    background-color: transparent;
  }
}
</style>
