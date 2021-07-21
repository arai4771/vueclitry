<template>
  <div>
   <a  id="active"></a>
   <h1 class="text-center my-15">ACTIVE</h1>

<v-timeline :dense="$vuetify.breakpoint.smAndDown"
>
    <v-timeline-item
      v-for="(time, i) in times"
      :key="i"
      :color="time.color"
      fill-dot
    >
      <v-card
        :color="time.color"
        dark
      >
        <v-card-title class="text-h6">{{time.tama}}
        </v-card-title>
        <v-card-text class="white text--primary">
      <p>{{time.text}}</p>
        </v-card-text>
      </v-card>
    </v-timeline-item>
  </v-timeline>
<a id="now"></a>
  </div>
</template>

<script>
export default {
  data () {
    return {
      times: [
        {
          color: 'red lighten-2',
          icon: 'mdi-star',
          tama: '体操インストラクター',
          text: '大学卒業後、半年間体操インストラクターとして従事'
        },
        {
          color: 'purple darken-1',
          icon: 'mdi-book-variant',
          tama: 'SES社員',
          text: 'プログラミングの研修と独学で複数のポートフォリオを作成'
        },
        {
          color: 'green lighten-1',
          icon: 'mdi-airballoon',
          tama: 'シェアハウスHP',
          text: 'Wordpressを用いてHPをリニューアル制作を行いました'
        },
        {
          color: 'indigo',
          icon: 'mdi-buffer',
          tama: '簡易自己紹介サイト',
          text: 'Vueを用いて簡単な自己紹介サイトを制作'
        },
        {
          color: 'deep-orange accent-2',
          icon: 'mdi-buffer',
          tama: 'ブログ設立',
          text: 'Wordpressを用いてブログ設立'
        },
        {
          color: 'yellow darken-4',
          icon: 'mdi-buffer',
          tama: '日本一周者向けの試作品アプリ',
          text: 'railsを用いて個人的に作りたいと考えているアプリの試作品制作'
        },
        {
          color: 'cyan accent-3',
          icon: 'mdi-buffer',
          tama: '簡易自己紹介サイト②',
          text: 'vue.cli/vuetifyを用いて簡易自己紹介サイトを制作'
        }
      ]
    }
  }
}
</script>
