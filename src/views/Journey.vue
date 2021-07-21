<template>
  <div>
    <a id="journey"></a>
<h1 class="text-center my-15">JOURNEY</h1>

  <v-carousel hide-delimiters>
        <v-carousel-item
          v-for="(item,i) in items"
          :key="i"
          reverse-transition="fade-transition"
          transition="fade-transition"
        ><img :src="item.src"></v-carousel-item>
    </v-carousel>

    <div class="text-center">
      <v-card class="ma-5">
          <v-card-text class="justify-center">大学４年次に大学を休学し、バイクで3ヶ月かけて日本一周を行いました。<br>
      宿泊場所は主にキャンプ場・ネカフェ・ゲストハウスに泊まっていました。<br>
      日本一周に関してはブログや<a href="http://pepe-blog.her.jp/myintro/">こちら</a>で紹介しています<br>
      </v-card-text>
        </v-card>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          src: require('@/assets/images/yuhi.jpg')
        },
        {
          src: require('@/assets/images/A4A03FEC-5FB6-40E8-8463-3A17F4082F99_1_105_c.jpeg')
        },
        {
          src: require('@/assets/images/CAE6AD32-ABD0-46F5-8C70-416A4E0B8F3D_1_105_c.jpeg')
        },
        {
          src: require('@/assets/images/F4637739-5E74-4488-8562-0A9D1CD598E3_1_105_c.jpeg')
        }
      ]
    }
  }
}
</script>
