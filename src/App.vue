<template>
  <div id="app">
    <img class="logo" alt="logo" src="data:image/png;base64,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">
    <div class="flipper">
      <div class="front">
        <div class="card">
          <div class="subtitle">个人高级版</div>
          <div class="title">{{type}}</div>
          <img class="ribbon img-front" alt="ribbon" src="data:image/png;base64,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">
        </div>
      </div>
      <div class="back">
        <div class="card">
          <div class="subtitle">兑换码</div>
          <div class="title">{{code}}</div>
          <img class="ribbon img-back" alt="ribbon" src="data:image/png;base64,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">
        </div>
      </div>
    </div>
    <transition name="fade">
      <div class="intro" v-if="showCode">
        <div class="tip"><span class="icon"></span>已复制到剪贴板</div>
        <div class="help">
          <div class="title">使用方式</div>
          <ol>
            <template v-if="isPC">
              <li>点击打开<a href="https://www.shimo.im/pricing" target="_blank">石墨文档官网定价页</a></li>
            </template>
            <template v-else>
              <li>使用电脑登录网址 www.shimo.im</li>
              <li>点击上方菜单栏的「定价」页面</li>
            </template>
            <li>选择「高级版」输入兑换码，获得高级版使用权限</li>
          </ol>
        </div>
      </div>
    </transition>
    <div class="info" v-if="!showCode">
      <p>感谢你之前填写了石墨文档的问卷，表示答谢，石墨文档准备了一张个人高级版{{type}}，赠送给你。</p>
      <button @click="getCode" ref="copyCode" :data-clipboard-text="code">点击领取</button>
    </div>
  </div>
</template>

<script>
import Clipboard from 'clipboard';

export default {
  name: 'shimo-gift-card',
  data() {
    return {
      showCode: false,
    }
  },
  computed: {
    code () {
      var query = window.location.search.substring(1);
      var vars = query.split("&");
      for (var i = 0; i < vars.length; i++) {
        var pair = vars[i].split("=");
        if (pair[0] == 'code') {
          return decodeURI(pair[1])
        }
      }
      return(false);
    },
    type () {
      var query = window.location.search.substring(1);
      var vars = query.split("&");
      for (var i = 0; i < vars.length; i++) {
        var pair = vars[i].split("=");
        if (pair[0] == 'type') {
          if (decodeURI(pair[1]) === "1") {
            return '季卡'
          } else if (decodeURI(pair[1]) === "2") {
            return '半年卡'
          } else if (decodeURI(pair[1]) === "3") {
            return '年卡'
          }
        }
      }
      return(false);
    },
    isPC () {
      var UA = window.navigator.userAgent.toLowerCase();
      if (/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(UA)) {
        return false
      } else {
        return true
      }
    }
  },
  mounted() {
    new Clipboard(this.$refs.copyCode);
  },
  methods: {
    getCode() {
      document.getElementsByClassName('flipper')[0].classList.add('show-back')
      setTimeout(() => {
        this.showCode = true;
      }, 1000);
      if (this.$refs.copyCode) {
        new Clipboard(this.$refs.copyCode);
      }
    }
  }
}
</script>

<style lang="scss">
.fade-enter-active, .fade-leave-active {
  opacity: 1;
  transition: .3s;
}

.fade-enter, .fade-leave-to {
  opacity: 0;
  transform: translate3d(0, -5%, 0);
  transition: .3s;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  position: absolute;
  left: 50%;
  max-width: 300px;
  margin-top: 10vh;
  margin-bottom: 100px;
  transform: translateX(-50%);
  color: #333;

  .logo {
    height: 30px;
  }

  .flipper {
    margin-top: 40px;
    width: 300px;
    height: 180px;
    transition: 1s;
    transform-style: preserve-3d;
    position: relative;

    &.show-back {
      transform: rotateY(180deg);
    }

    .front, .back {
      position: absolute;
      backface-visibility: hidden;
    }

    .back {
      transform: rotateY(180deg);
    }

    .card {
      width: 300px;
      height: 180px;
      margin-left: -1px;
      border-radius: 4px;
      background-image: linear-gradient(225deg,#7d7d7d,#4a4a4a);
      border: 1px solid #2f2f2f;
      box-shadow: 0 10px 20px rgba(0,0,0,0.2);
      color: white;
      text-shadow: 0 1px 1px #2f2f2f;

      .subtitle {
        padding-top: 52px;
        opacity: 0.6; 
      }

      .title {
        margin-top: 5px;
        font-size: 30px;
        font-weight: bold;
      }

      .ribbon {
        position: absolute;
        width: 54px;
        height: 54px;
        top: -4px;

        &.img-front {
          right: -3px;
        }

        &.img-back {
          left: -3px;
        }
      }
    }
  }

  .info {
    margin-top: 40px;

    p {
      padding: 0 20px;
      text-align: left;
      font-size: 15px;
    }

    button {
      margin-top: 20px;
      padding: 10px 0;
      width: calc(100% - 40px);
      border-radius: 2px;
      font-size: 16px;
      color: white;
      background-color: #3f3f3f;
      border: none;
      cursor: pointer;

      &:focus {
        outline: none;
      }
    }
  }

  .intro {
    margin-top: 40px;
    height: 140px;

    .tip {
      padding-left: 12px;
      font-weight: bold;

      .icon {
        position: absolute;
        margin-top: -1px;
        margin-left: -25px;
        transform: rotate(45deg);
        width: 16px;
        height: 16px;

        &:before, &:after {
          content: '';
          position: absolute;
          background-color: #39b339;
        }

        &:before {
          width: 9px;
          height: 3px;
          bottom: 0;
          right: 0;
        }

        &:after {
          width: 3px;
          height: 16px;
          bottom: 0;
          right: 0;
        }
      }
    }

    .help {
      .title {
        position: relative;
        margin-top: 30px;

        &:before, &:after {
          content: '';
          position: absolute;
          top: 10px;
          width: 80px;
          height: 1px;
          background-color: #eee;
        }

        &:before {
          left: 20px;
        }

        &:after {
          right: 20px;
        }
      }

      ol {
        padding-right: 20px;
        text-align: left;

        li {
          margin-bottom: 10px;

          a {
            color: #3397e6;
            text-decoration-line: none;

            &:hover {
              text-decoration-line: underline;
            }
          }
        }
      }
    }
  }
}
</style>
