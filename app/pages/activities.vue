<script setup>
const featuredActivities = [
  {
    title: '家庭教育与青少年成长讲座',
    category: '讲座 / 沙龙',
    date: '持续开展',
    place: '学校与教育机构',
    desc: '围绕亲子沟通、青春期发展、学习压力与家庭互动模式开展主题讲座，帮助家长从关系系统中理解孩子的情绪与行为。',
    tags: ['家庭教育', '亲子沟通', '青少年成长'],
  },
  {
    title: '正念减压课程与团体练习',
    category: '正念课程',
    date: '2023-2024',
    place: '今心空间 / 中加正念协会',
    desc: '结合 MBCT 受训背景与正念减压课程经验，带领参与者通过身体觉察、呼吸练习与团体分享建立更稳定的自我觉察。',
    tags: ['MBCT', '正念减压', '团体支持'],
  },
  {
    title: '高校心理支持与团体辅导项目',
    category: '高校项目',
    date: '2021 至今',
    place: '西南大学 / 四川大学心理中心',
    desc: '在高校心理中心场域中参与学生心理支持、个体咨询与团体项目，关注青年学生在学业、人际关系与自我发展中的真实困境。',
    tags: ['高校心理', '团体辅导', '学生支持'],
  },
]

const archiveItems = [
  ['讲座与沙龙', '家庭教育、亲子沟通、青春期发展、压力管理等主题活动。'],
  ['团体辅导', '面向学校、机构或社群的心理主题团体与成长小组。'],
  ['正念课程', 'MBCT、八周正念课程、28 天正念减压等课程记录。'],
  ['论文与文章', '论文、文章、项目报告、媒体报道或公开发表内容。'],
]

const maintainNotes = [
  '活动封面：public/images/activities/活动名称/cover.jpg',
  '活动照片：public/images/activities/活动名称/01.jpg',
  '论文 PDF：public/files/papers/论文名称.pdf',
]
</script>

<template>
  <main class="min-h-screen bg-[#f7f3ec] text-stone-800 antialiased">
    <header class="sticky top-0 z-50 border-b border-stone-200/70 bg-[#f7f3ec]/90 backdrop-blur-md">
      <div class="mx-auto flex max-w-6xl items-center justify-between px-5 py-4 md:px-6">
        <NuxtLink to="/" class="text-base font-medium tracking-wide text-stone-900">
          石婷 Sting
        </NuxtLink>

        <nav class="flex items-center gap-5 text-sm text-stone-500 md:gap-7">
          <NuxtLink to="/" class="transition hover:text-stone-900">首页</NuxtLink>
          <a href="#featured" class="transition hover:text-stone-900">精选活动</a>
          <a href="#archive" class="transition hover:text-stone-900">成果归档</a>
        </nav>
      </div>
    </header>

    <section class="border-b border-stone-200 bg-[#edf0e9]">
      <div class="reveal mx-auto grid max-w-6xl gap-8 px-5 py-14 md:grid-cols-[0.95fr_1.05fr] md:px-6 md:py-16">
        <div>
          <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#a47c2b]">Activities</p>
          <h1 class="mt-5 max-w-3xl text-4xl font-light leading-tight text-stone-900 md:text-6xl">
            活动经历与成果展示
          </h1>
        </div>

        <div class="self-end">
          <p class="max-w-2xl text-lg leading-8 text-stone-600">
            这里用于展示讲座、团体辅导、正念课程、学校项目与论文成果。后续有真实照片或 PDF 时，可以逐步替换当前的活动卡片。
          </p>
          <div class="mt-7 flex flex-wrap gap-2">
            <span class="border border-stone-300 bg-white/50 px-3 py-1.5 text-sm text-stone-600">讲座</span>
            <span class="border border-stone-300 bg-white/50 px-3 py-1.5 text-sm text-stone-600">团辅</span>
            <span class="border border-stone-300 bg-white/50 px-3 py-1.5 text-sm text-stone-600">正念课程</span>
            <span class="border border-stone-300 bg-white/50 px-3 py-1.5 text-sm text-stone-600">论文成果</span>
          </div>
        </div>
      </div>
    </section>

    <section id="featured" class="reveal py-20 md:py-24">
      <div class="mx-auto max-w-6xl px-5 md:px-6">
        <div class="mb-10 flex flex-col justify-between gap-5 md:flex-row md:items-end">
          <div>
            <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#a47c2b]">Featured</p>
            <h2 class="mt-5 text-3xl font-light text-stone-900 md:text-5xl">精选活动</h2>
          </div>
          <p class="max-w-md leading-7 text-stone-600">
            先保留清爽的展示结构，真实图片上传后可以自然变成图文活动页。
          </p>
        </div>

        <div class="grid gap-5 md:grid-cols-3">
          <article
            v-for="(activity, index) in featuredActivities"
            :key="activity.title"
            class="group overflow-hidden border border-stone-200 bg-white transition duration-300 hover:border-stone-300"
          >
            <div class="aspect-[4/3] bg-[#dfe5dc] p-5">
              <div class="flex h-full flex-col justify-between border border-white/70 bg-[#edf0e9]/70 p-5">
                <p class="text-xs font-medium uppercase tracking-[0.22em] text-[#a47c2b]">
                  Activity 0{{ index + 1 }}
                </p>
                <p class="text-sm leading-6 text-stone-500">封面照片待上传</p>
              </div>
            </div>

            <div class="p-6">
              <div class="flex flex-wrap gap-2 text-sm">
                <span class="bg-[#edf0e9] px-3 py-1.5 text-[#5f766f]">{{ activity.category }}</span>
                <span class="px-1.5 py-1.5 text-stone-400">{{ activity.date }}</span>
              </div>

              <h3 class="mt-5 text-xl font-medium leading-8 text-stone-900">{{ activity.title }}</h3>
              <p class="mt-2 text-sm text-stone-500">{{ activity.place }}</p>
              <p class="mt-5 leading-7 text-stone-600">{{ activity.desc }}</p>

              <div class="mt-6 flex flex-wrap gap-2">
                <span
                  v-for="tag in activity.tags"
                  :key="tag"
                  class="border border-stone-200 px-3 py-1.5 text-sm text-stone-500"
                >
                  {{ tag }}
                </span>
              </div>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="archive" class="reveal bg-[#e9e4db] py-20 md:py-24">
      <div class="mx-auto max-w-6xl px-5 md:px-6">
        <div class="mb-10 max-w-3xl">
          <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#a47c2b]">Archive</p>
          <h2 class="mt-5 text-3xl font-light text-stone-900 md:text-5xl">成果归档方向</h2>
        </div>

        <div class="grid gap-px overflow-hidden border border-stone-300 bg-stone-300 md:grid-cols-4">
          <article
            v-for="[title, desc] in archiveItems"
            :key="title"
            class="bg-[#f7f3ec] p-6"
          >
            <h3 class="text-lg font-medium text-stone-900">{{ title }}</h3>
            <p class="mt-4 text-sm leading-7 text-stone-600">{{ desc }}</p>
          </article>
        </div>
      </div>
    </section>

    <section class="reveal py-14">
      <div class="mx-auto max-w-6xl px-5 md:px-6">
        <details class="border border-stone-200 bg-white p-5">
          <summary class="cursor-pointer text-sm font-medium text-stone-700">
            维护提示：后续素材放置位置
          </summary>
          <ul class="mt-4 space-y-2 text-sm leading-6 text-stone-500">
            <li v-for="note in maintainNotes" :key="note">{{ note }}</li>
          </ul>
        </details>
      </div>
    </section>
  </main>
</template>
