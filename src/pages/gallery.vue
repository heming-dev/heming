<script setup lang="ts">
const openInfo = ref([
  {
    title: 'DiyFile',
    desc: '一款好看的在线文件列表程序，由 Spring Boot 3 和 Vue 驱动。',
    href: 'https://demo.besscroft.com/',
    github: 'https://github.com/besscroft/diyfile',
  },
  {
    title: 'HeMing Fast',
    desc: '基于 SpringBoot3 + Nuxt 3 + Vuetify 3 的脚手架！',
    href: 'https://fast.heming.dev/',
    github: 'https://github.com/besscroft/heming-fast',
  },
  {
    title: '嗯学英语',
    desc: '嗯学英语，学英语，就嗯学！',
    href: 'https://enstudy.heming.dev/',
    github: 'https://github.com/besscroft/enstudy',
  },
  {
    title: 'Pisces-Cloud',
    desc: '一站式微服务解决方案，基于 openJDK 17、Spring Cloud 2021.0.1 & Alibaba 2021.0.1.0 + Spring Security OAuth2 + PostgreSQL + Mybatis-Plus 构建。',
    href: 'https://pisces.besscroft.com/',
    github: 'https://github.com/besscroft/pisces-cloud',
  },
  {
    title: 'nuxt-h5',
    desc: 'Nuxt 3 H5 Starter',
    href: 'https://nuxt-h5.vercel.app/',
    github: 'https://github.com/besscroft/nuxt-h5',
  },
  {
    title: 'kamera',
    desc: '一款专供摄影佬使用的记录网站，基于 Nuxt 3 开发。可读取 EXIF 信息并上传、管理维护图片数据，首页精品照片展示，子页分类展示等功能。',
    href: 'https://kamera.heming.dev/',
    github: 'https://github.com/besscroft/kamera',
  },
])

const noOpenInfo = ref([
  {
    title: 'GAI4J',
    desc: '生成式创作管理平台，AI 模型接入、Prompt、创作管理、热点指数、爆文分析、爆文重写、运营、数据分析等。',
    href: '#',
    github: 'N/A',
  },
  {
    title: '如意面板',
    desc: '现代、简约、节约内存的 Linux 管理面板，抽空开发中...',
    href: '#',
    github: 'N/A',
  },
])

const openArchiveInfo = ref([
  {
    title: 'heming-rss',
    desc: '一款 Material Design 风格的 RSS 阅读器，支持 ChatGPT 和自定义订阅。',
    href: 'https://heming-rss.vercel.app/',
    github: 'https://github.com/besscroft/heming-rss',
  },
])
</script>

<template>
  <div>
    <div w-full text-center h-12 text-xl>开源</div>
    <div md:px-4 lg:px-8 xl:px-12 grid md:gap-2 lg:gap-4 xl:gap-6 grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4>
      <div
        :key="item.title"
        v-for="item in openInfo"
        flex flex-col items-center h-48 rounded-md border-green-400 border-4 px-4 my-1
        hover:-translate-y-1 hover:scale-105 hover:transition duration-300
      >
        <div h-12 flex items-center><p text-xl>{{ item.title }}</p></div>
        <div h-24 p-1><p>{{ item.desc }}</p></div>
        <div h-12 p-2 space-x-2>
          <a icon-btn v-if="item.href !== '#'" rel="noreferrer" :href="item.href" target="_blank" title="Website">
            <div animate-bounce scale-150 i-carbon-send-alt />
          </a>
          <a icon-btn v-if="item.github !== 'N/A'" rel="noreferrer" :href="item.github" target="_blank" title="GitHub">
            <div animate-bounce scale-150 i-carbon-logo-github />
          </a>
        </div>
      </div>
    </div>
    <div w-full text-center h-12 text-xl>闭源</div>
    <div md:px-4 lg:px-8 xl:px-12 grid md:gap-2 lg:gap-4 xl:gap-6 grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4>
      <div
        :key="item.title"
        v-for="item in noOpenInfo"
        flex flex-col items-center h-48 rounded-md border-green-400 border-4 px-4 my-1
        hover:-translate-y-1 hover:scale-105 hover:transition duration-300
      >
        <div h-12 flex items-center><p text-xl>{{ item.title }}</p></div>
        <div h-24 p-1><p>{{ item.desc }}</p></div>
        <div h-12 p-2 space-x-2>
          <a icon-btn v-if="item.href !== '#'" rel="noreferrer" :href="item.href" target="_blank" title="Website">
            <div animate-bounce scale-150 i-carbon-send-alt />
          </a>
          <a icon-btn v-if="item.github !== 'N/A'" rel="noreferrer" :href="item.github" target="_blank" title="GitHub">
            <div animate-bounce scale-150 i-carbon-logo-github />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>

<route lang="yaml">
meta:
  layout: default
</route>
