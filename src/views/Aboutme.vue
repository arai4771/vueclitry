<template>
<div>
  <div class="top">
    <h1>Welcome my portfolio</h1>
  </div>

<v-container class="main1">
  <a id="about"></a>
  <h1 class="text-center my-15">ABOUT ME</h1>

  <div class="about">
    <v-row justify="center">
      <div>
          <v-img height="200px" width="200px" src="@/assets/images/pepeicon (1).png"></v-img>
      </div>
      <div class="my-5">
        <ul>
          <li>
            <p><strong>名前：</strong>福本隼平</p>
          </li>
          <li>
          <p><strong>趣味：</strong>旅行・筋トレ・ブレイクダンス</p>
          </li>
          <li>
            <p><strong>作品集：</strong><a href="http://pepe-blog.her.jp/pepe.portforio/">http://pepe-blog.her.jp/pepe.portforio/</a></p>
          </li>
        </ul>
      </div>
    </v-row>
  </div>
</v-container>
</div>

</template>

<script>

export default {
  name: 'Aboutme',
  data () {
    return {

    }
  }
}
</script>
<style scoped>
.main1 h1{
  font-size:40px;
  color: #0093E9;
}
.about{
  display: flex;
  text-align: center;

}
</style>
