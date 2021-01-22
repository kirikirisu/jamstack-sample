<template>
  <layout-wrapper>
    <div>
      <layout-visual
        title="NUXT SAMPLE SITE"
        message="お知らせとメニューにheadlessCMSを導入したサイト"
      ></layout-visual>

      <div class="w-full md:max-w-3xl mx-auto pt-20 px-6 md:px-0">
        <base-heading> おすすめメニュー </base-heading>
        <div class="flex md:flex-wrap justify-between mb-20 md:mb-0">
          <layout-menu-list
            v-for="(item, index) in menuItems"
            :key="index"
            :image="item.image"
            :image-url="item.image.url"
            :name="item.name"
            :body="item.body"
            :price="item.price"
            item-class="md:w-56 mb-20 shadow-lg bg-gray-200"
            block-class="max-w"
            image-class="w-full"
            data-class="px-6 py-4"
            :flag-body="false"
          />
        </div>
        <base-button name="メニューの一覧" link="/mane/" />
      </div>
      <base-heading>お知らせ</base-heading>
      <layoutinformation-list />
      <base-button name="お知らせ一覧" link="/information/" />
    </div>
  </layout-wrapper>
</template>

<script>
import axios from 'axios'

export default {
  async asyncData({ $config }) {
    const { data } = await axios.get(`${$config.apiUrl}/menu`, {
      headers: { 'X-API-KEY': $config.apiKey },
    })

    return {
      menuItems: data.contents,
    }
  },
}
</script>
