<template>
  <layout-wrapper>
    <layout-visual title="concept" :height="40" visual="visual-concept" />
    <div class="container w-full mx-auto pt-20 pb-20 px-6 md:px-0">
      <h3 class="text-2xl text-red-800 font-extrabold mb-5 text-center">
        落ち着く空間
      </h3>
      <div class="clearfix p-4 mb-10">
        <img class="float-right ml-4 my-2 h-56" src="~/assets/img/menu01.jpg" />
        <div>
          <p class="mb-5">
            このカフェでは、リモートワークや会社の打ち合わせなどが快適に行える空間を提供する空間です。
            <br />
            リモートワークや打ち合わせを快適するため席は完全個室にしています。
            <br />
            オンラインでの作業ができるようにWiFiも完備しています。また週末は勉強会の場所としても提供しています。
          </p>
          <p class="mb-5">
            お食事は天然素材を使ったドーナッツパンケーキを開発しています。<br />
            シンプルな素材と調理法で食事本来の味を引き立てる自慢のドーナッツパンケーキをご提供しています。<br />
            コーヒーはブラジル産の豆をしようして、酸味とすっきりとして苦みのあるコーヒーになります。
          </p>
        </div>
      </div>
      <base-button name="トップへ戻る" link="/" />
    </div>
  </layout-wrapper>
</template>

<script>
export default {
  head() {
    return {
      title: 'コンセプト',
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: 'コンセプトページの説明',
        },
      ],
    }
  },
}
</script>
