<template>
  <layout-wrapper>
    <div>
      <layout-visual
        title="NUXT SAMPLE SITE"
        message="お知らせとメニューにheadlessCMSを導入したサイト"
      ></layout-visual>

      <div class="w-full md:max-w-3xl mx-auto pt-20 px-6 md:px-0">
        <base-heading> おすすめメニュー </base-heading>
        <layout-menu-list 
          wrap-class="flex md:flex-wrap justify-between mb-20 md:mb-0" 
          item-class="md:w-56 mb-20 shadow-lg bg-gray-200"
          block-class="max-w"
          image-class="w-full"
          data-class="px-6 py-4"
          :flag-body="false"
        />
        <base-button name="メニューの一覧" link="/mane/" />
      </div>
      <base-heading>お知らせ</base-heading>
      <layoutinformation-list />
      <base-button name="お知らせ一覧" link="/information/" />
    </div>

  </layout-wrapper>
</template>
