<template>
  <div id="main">
    <div id="js-bgvideowrap" class="bg-video">
      <video
        id="js-bgvideo"
        src="https://d35c6yop31qdi0.cloudfront.net/alter_assets_v2/video/bg.mp4?20210528103515"
        autplay=""
        loop=""
        muted=""
        playsinline=""
      />
    </div>
    <kinesis-container>
      <div v-scroll-reveal class="header">
        <div class="bg">
          <kinesis-element :strength="50">
            <img src="/bg/1.png" class="bg-ele bg-1" />
          </kinesis-element>
          <kinesis-element :strength="30">
            <img src="/bg/3.png" class="bg-ele bg-3" />
          </kinesis-element>
          <kinesis-element :strength="20">
            <img src="/bg/4.png" class="bg-ele bg-4" />
          </kinesis-element>
        </div>
        <div class="content">
          <div class="logo">
            <kinesis-element :strength="10">
              <Logo />
            </kinesis-element>
          </div>
        </div>
      </div>
    </kinesis-container>
    <div v-scroll-reveal class="content-d">
      <div>
        <h1>Story</h1>
        <h1 class="small">
          ヒトやモノ、ケモノなどがイワレを一定以上溜めこむと、それらはやがてこの世ならざる者に変化する。
          アヤカシは「ワザ」と呼ばれる特殊なチカラを使うことができるといい、
          炎を操ったり水を氷に変えたり、あるいはヒトに化けるなど、そのチカラの形は様々であるらしい。
          また、チカラの強いアヤカシほど、強力なワザを操ると言われている。
        </h1>
      </div>
    </div>
    <div v-scroll-reveal class="content-d">
      <div>
        <h1>ティザーPV</h1>
        <iframe
          width="1268"
          height="713"
          src="https://www.youtube.com/embed/3RxlzJWWzdY"
          title="YouTube video player"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen
        />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({});
</script>

<style>
html,
body {
  height: 100%;
  margin: 0;
}

.bg-ele {
  position: absolute;
}

.full-height {
  height: 100%;
}

.header {
  height: 900px;
}

.header .content {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.bg {
  position: absolute;
  z-index: -1;
}

.bg-1 {
  transform: scale(0.5);
  filter: blur(5px);
}

.bg-3 {
  transform: scale(0.5);
  filter: blur(5px);
  left: 376px;
}

.bg-4 {
  transform: scale(0.5);
  filter: blur(3px);
  left: -653px;
  top: 210px;
}

.bg-video {
  position: fixed;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  z-index: -21;
  -ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=0)";
  transition-duration: 0.8s;
  transition-delay: 1.2s;
  overflow: hidden;
}

.content-d {
  display: flex;
  justify-content: center;
  padding: 120px 0px;
}

h1 {
  font-size: 3rem;
  text-align: center;
}

.small {
  width: 800px;
  font-size: 1.5rem;
}
</style>
