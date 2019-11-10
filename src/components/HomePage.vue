<template>
  <div class="home-container">
    <div class="dott"></div>
    <div class="picture-wall">
      <div class="wall-content">
        <img src="../../assets/images/homepage/avator.jpeg" alt="">
        <h3 class="username" style="color: #fff;">
          <span>{{userinfo.prename}}</span>
          <span>{{userinfo.name}}</span>
        </h3>
       <!--  <p class="subtitle">para</p> -->
      </div>
    </div>
    <div class="text-container">
      <div class="introduction">
        <h3 class="introduce-title">{{userinfo.introTitle}}</h3>
        <p class="introduce-content">喜欢写代码喜欢写代码喜欢写代码喜欢写代码喜欢写代码</p>
      </div>
      <div class="contact-info">
        <ul class="info-list">
          <li class="list-item" v-for="(intro, key) in userinfo.introduceList" :key="key">
            <ul class="item-detail">
              <li class="detail-title"><b>{{intro.title}}</b></li>
              <li class="detail-content">
                <span>:</span>
                <a :href="intro.content" target="_blank" style="text-decoration: none;">{{intro.content}}</a></li>
            </ul>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data () {
    return {
      userinfo: {
        prename: '杨',
        name: '林',
        introTitle: '我的介绍',
        introduceList: [
          {
            title: 'Email',
            content: 'nefu_yanglin@163.com'
          },
          {
            title: 'Github',
            content: 'https://github.com/AdamLambet'
          },
          {
            title: 'CSDN',
            content: 'https://blog.csdn.net/weixin_44153194'
          }
        ]
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@media screen and (min-width: 820px){
  .home-container {
      font-size: 1em;
      flex-direction: row;
  }
  .home-container .picture-wall {
    flex: 1;
  }
  .home-container .text-container {
    flex: 1;
  }
  .wall-content{
      width: 250px;
      height: 250px;
      padding: 80px;
  }
  .home-container .picture-wall {
    padding: 9em 0 0 0;
  }
  .wall-content .username{
    font-size: 2.2em;
  }
  .home-container .picture-wall .wall-content img {
    width: 180px;
  }
  .home-container .introduction {
    padding: 9em 0 0 0;
  }
}
@media screen and (max-width: 820px){
  .home-container {
      font-size: 1em;
      flex-direction: column;
  }
  .home-container .picture-wall {
    flex: 1;
  }
  .home-container .text-container {
    flex: 9;
  }
   .wall-content{
      width: 150px;
      height: 150px;
      padding: 20px;
  }
  .home-container .picture-wall {
    padding: 2em 0 0 0;
  }
  .wall-content .username{
    font-size: 1.5em;
  }
  .home-container .picture-wall .wall-content img {
    width: 100px;
  }
  .home-container .introduction {
    padding: 2em 2em 0 2em;
  }
  .home-container .contact-info {
    padding: 0 2em 0 2em;
  }
}
.dott {
  position: absolute;
  height: 100%;
  width: 100%;
  background-image: url(../../assets/images/homepage/dott.png);
  opacity: 0.4;
  z-index: 1;
}
.home-container {
  position: relative;
  height: 100%;
  width: 100%;
  background-image: url(../../assets/images/homepage/pagebg1.jpg);
  background-size: cover;
  display: flex;
  display: -webkit-flex;
}
.home-container .picture-wall {
  z-index: 2;
}
.home-container .picture-wall .wall-content {
  margin: 0 auto;
  text-align: center;
  border: 5px solid rgba(238, 238, 238, 0.53);
  font-family: 'Raleway', sans-serif;
}
.home-container .picture-wall .wall-content img {
  border-radius: 50%;
}
.home-container .text-container {
  z-index: 2;
  display: flex;
  flex-direction: column;
}
.text-container .introduction {
  flex: 2;
}
.text-container .introduction .introduce-title {
  font-size: 2em;
  letter-spacing: 2px;
  color: #fff;
  font-family: 'Yanone Kaffeesatz', sans-serif;
}
.text-container .introduction .introduce-content {
  color: #c5c2c2;
  font-size: 1em;
  line-height: 1.8em;
  letter-spacing: 1px;
  text-indent: 2em;
}
.text-container .contact-info {
  flex: 3;
}
.text-container .contact-info .info-list {
  border-top: 2px dotted #00bcd4;
  padding-top: 0.5em;
}
.text-container .contact-info .info-list .item-detail {
  margin-top: 1em;
}
.text-container .contact-info .info-list .item-detail li {
  display: inline-block;
  color: #fff;
}
.text-container .contact-info .info-list .item-detail li:nth-child(1) {
  width: 20%;
}
.text-container .contact-info .info-list .item-detail li span {
  margin: 0.2em;
  color: #d9edf7;
}
.text-container .contact-info .info-list  .item-detail b {
  color: #fff;
}
.text-container .contact-info .info-list  .item-detail .detail-content a {
  font-weight: 600;
  color: #fff;
}
</style>
