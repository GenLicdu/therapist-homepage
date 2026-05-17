<script setup>
import './assets/css/main.css'

const credentials = [
  { value: '1000h+', label: '累计咨询时长' },
  { value: '250h+', label: '持续个体与团体督导' },
  { value: '100h+', label: '个人体验' },
]

const services = [
  {
    title: '成人个体咨询',
    desc: '支持情绪压力、自我探索、关系困扰、边界感与长期重复的内在模式议题。',
  },
  {
    title: '青少年个体咨询',
    desc: '关注学习压力、人际关系、亲子互动、自我认同与成长阶段中的心理支持。',
  },
  {
    title: '家庭教育与亲子沟通',
    desc: '面向家庭系统理解亲子关系，帮助家长看见互动模式与孩子真实的心理需要。',
  },
  {
    title: '正念减压与团体辅导',
    desc: '结合 MBCT 受训背景，开展正念课程、减压练习、主题工作坊与团体支持。',
  },
]

const trainings = [
  ['姚玉红基于系统和依恋理论的家庭治疗督导', '2025.4-2026.1'],
  ['赵旭东姚王红家庭治疗工作坊', '2026.4'],
  ['张新荷焦点解决短期疗法工作坊', '2025.12'],
  ['陈伯炜 OH 卡培训工作坊', '2025.4'],
  ['中德模式家庭治疗刻意练习班', '2024-2025'],
  ['注册系统伦理培训（中阶）', '2024.10'],
  ['多伦多正念研究中心 MBCT 师资培训', '2023-2024'],
  ['和光认知行为疗法两年系统培训', '2021-2023'],
  ['朱旭、王铭人本主义 10 讲', '2023.9'],
  ['吉沅洪绘画心理学', '2022.10'],
  ['周玥八周正念课程', '2022.7'],
  ['高旭滨八周正念课程', '2021.7'],
  ['黄耀光郭海峰五日止语日', '2021.4'],
  ['杨发辉 CBT 系统培训', '2020.2'],
  ['刘兴华八周正念课程', '2019.3'],
  ['北京大学明慧咨询暑期学校 DBT', '2018.7'],
  ['中国农业大学明慧心理高级课程', '2016-2018'],
]

const experience = [
  ['嘉祥教育集团', '2024.10 至今'],
  ['四川大学心理中心', '2024.9 至今'],
  ['鸿鹤高中', '2023.7-2024.10'],
  ['四川和光临床心理研究院', '2022-2024'],
  ['今心空间 / 中加正念协会 28 天正念减压课程', '2023.9'],
  ['西南大学心理中心', '2021.4-2023.6'],
]
</script>

<template>
  <main class="min-h-screen bg-[#f8f5f0] text-stone-800 antialiased">
    <header class="fixed left-0 right-0 top-0 z-50 border-b border-stone-200/70 bg-[#f8f5f0]/90 backdrop-blur-md">
      <div class="mx-auto flex max-w-6xl items-center justify-between px-5 py-4 md:px-6">
        <a href="#" class="text-base font-medium tracking-wide text-stone-900">
          石婷 Sting
        </a>

        <nav class="hidden items-center gap-7 text-sm text-stone-500 md:flex">
          <a href="#about" class="transition hover:text-stone-900">专业背景</a>
          <a href="#services" class="transition hover:text-stone-900">咨询方向</a>
          <a href="#training" class="transition hover:text-stone-900">受训经历</a>
          <a href="#contact" class="transition hover:text-stone-900">预约咨询</a>
        </nav>
      </div>
    </header>

    <section class="min-h-screen pt-24">
      <div class="mx-auto grid min-h-[calc(100vh-6rem)] max-w-6xl items-center gap-12 px-5 py-14 md:grid-cols-[1.05fr_0.95fr] md:px-6 md:py-20">
        <div>
          <p class="mb-5 text-xs font-medium uppercase tracking-[0.28em] text-[#a47c2b]">
            Psychological Counseling
          </p>

          <h1 class="max-w-3xl text-4xl font-light leading-[1.18] text-stone-900 md:text-6xl">
            在关系、情绪与自我之间，陪你慢慢看见内心的需要
          </h1>

          <p class="mt-7 max-w-2xl text-lg leading-8 text-stone-600">
            注册系统心理咨询师，多伦多正念研究中心 MBCT 受训背景。面向成人、青少年与家庭关系议题，提供个体咨询、正念减压与团体心理支持。
          </p>

          <div class="mt-9 grid max-w-2xl grid-cols-3 border-y border-stone-300/80">
            <div
              v-for="item in credentials"
              :key="item.label"
              class="border-r border-stone-300/80 py-5 last:border-r-0"
            >
              <p class="text-2xl font-light text-stone-900 md:text-3xl">{{ item.value }}</p>
              <p class="mt-1 text-xs leading-5 text-stone-500 md:text-sm">{{ item.label }}</p>
            </div>
          </div>

          <div class="mt-9 flex flex-wrap gap-3">
            <a
              href="#contact"
              class="rounded-full bg-stone-900 px-6 py-3 text-sm font-medium text-white transition hover:bg-stone-700"
            >
              预约咨询
            </a>
            <a
              href="#about"
              class="rounded-full border border-stone-300 px-6 py-3 text-sm font-medium text-stone-700 transition hover:border-stone-500 hover:bg-white"
            >
              查看专业背景
            </a>
          </div>
        </div>

        <div class="relative mx-auto w-full max-w-md md:max-w-none">
          <div class="aspect-[4/5] overflow-hidden rounded-lg border border-white bg-stone-200 shadow-[0_24px_70px_rgba(68,64,60,0.16)]">
            <img
              src="/images/profile.jpg"
              alt="石婷个人照片"
              class="h-full w-full object-cover"
            />
          </div>

          <div class="absolute -bottom-6 left-5 right-5 border border-stone-200 bg-white/92 p-5 shadow-lg backdrop-blur md:-left-7 md:right-auto md:w-72">
            <p class="text-xs uppercase tracking-[0.24em] text-[#a47c2b]">Focus</p>
            <p class="mt-2 text-sm leading-6 text-stone-600">
              系统家庭治疗 · 正念减压 · 认知行为疗法 · 青少年成长
            </p>
          </div>
        </div>
      </div>
    </section>

    <section id="about" class="border-t border-stone-200 py-24 md:py-28">
      <div class="mx-auto grid max-w-6xl gap-12 px-5 md:grid-cols-[0.75fr_1.25fr] md:px-6">
        <div>
          <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#a47c2b]">About</p>
          <h2 class="mt-5 text-3xl font-light leading-tight text-stone-900 md:text-5xl">
            稳定、温和，也保持专业边界。
          </h2>
        </div>

        <div class="space-y-8">
          <div class="grid gap-5 text-stone-600 md:grid-cols-2">
            <div class="border-l border-[#c69b3d] pl-5">
              <p class="text-sm text-stone-500">教育背景</p>
              <h3 class="mt-2 text-xl text-stone-900">西南大学 应用心理学硕士</h3>
              <p class="mt-1 text-sm">2020.9-2023.7</p>
            </div>
            <div class="border-l border-[#c69b3d] pl-5">
              <p class="text-sm text-stone-500">本科背景</p>
              <h3 class="mt-2 text-xl text-stone-900">中国农业大学 学士</h3>
              <p class="mt-1 text-sm">2016.9-2019.7</p>
            </div>
          </div>

          <div class="max-w-3xl space-y-5 text-base leading-8 text-stone-600">
            <p>
              石婷长期接受系统家庭治疗、认知行为疗法、正念减压、人本主义、焦点解决短期疗法等方向训练，并持续接受个体与团体督导。
            </p>
            <p>
              她的工作经验覆盖高校心理中心、学校心理项目、家庭教育讲座、正念课程与机构团体辅导，关注人在关系、情绪和成长阶段中的真实处境。
            </p>
          </div>
        </div>
      </div>
    </section>

    <section id="services" class="bg-[#eee8df] py-24 md:py-28">
      <div class="mx-auto max-w-6xl px-5 md:px-6">
        <div class="mb-12 max-w-3xl">
          <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#a47c2b]">Services</p>
          <h2 class="mt-5 text-3xl font-light text-stone-900 md:text-5xl">咨询与支持方向</h2>
        </div>

        <div class="grid gap-px overflow-hidden border border-stone-300/80 bg-stone-300/80 md:grid-cols-2">
          <article
            v-for="service in services"
            :key="service.title"
            class="bg-[#f8f5f0] p-7 md:p-9"
          >
            <h3 class="text-xl font-medium text-stone-900">{{ service.title }}</h3>
            <p class="mt-4 leading-7 text-stone-600">{{ service.desc }}</p>
          </article>
        </div>
      </div>
    </section>

    <section id="training" class="py-24 md:py-28">
      <div class="mx-auto grid max-w-6xl gap-12 px-5 md:grid-cols-[0.8fr_1.2fr] md:px-6">
        <div>
          <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#a47c2b]">Training</p>
          <h2 class="mt-5 text-3xl font-light leading-tight text-stone-900 md:text-5xl">
            持续受训，持续督导。
          </h2>
          <p class="mt-6 max-w-sm leading-8 text-stone-600">
            咨询师的专业性不只来自证书，也来自长期训练、个人体验、督导与真实工作场景中的反思。
          </p>
        </div>

        <div class="divide-y divide-stone-200 border-y border-stone-300">
          <div
            v-for="[name, date] in trainings"
            :key="`${name}-${date}`"
            class="grid gap-2 py-4 text-sm md:grid-cols-[1fr_8rem] md:gap-8 md:text-base"
          >
            <p class="leading-7 text-stone-800">{{ name }}</p>
            <p class="text-stone-500 md:text-right">{{ date }}</p>
          </div>
        </div>
      </div>
    </section>

    <section id="experience" class="bg-white py-24 md:py-28">
      <div class="mx-auto max-w-6xl px-5 md:px-6">
        <div class="mb-10 flex flex-col justify-between gap-5 md:flex-row md:items-end">
          <div>
            <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#a47c2b]">Experience</p>
            <h2 class="mt-5 text-3xl font-light text-stone-900 md:text-5xl">工作与项目经历</h2>
          </div>
          <p class="max-w-md leading-7 text-stone-600">
            覆盖高校心理中心、中学心理支持、教育集团、临床心理机构与正念课程项目。
          </p>
        </div>

        <div class="grid gap-px border border-stone-300 bg-stone-300 md:grid-cols-2">
          <div
            v-for="[name, date] in experience"
            :key="`${name}-${date}`"
            class="flex min-h-28 flex-col justify-between bg-white p-6"
          >
            <h3 class="text-lg text-stone-900">{{ name }}</h3>
            <p class="mt-5 text-sm text-stone-500">{{ date }}</p>
          </div>
        </div>
      </div>
    </section>

    <section id="contact" class="bg-stone-900 py-24 text-white md:py-28">
      <div class="mx-auto grid max-w-6xl gap-12 px-5 md:grid-cols-[1fr_0.9fr] md:px-6">
        <div>
          <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#d0a54a]">Contact</p>
          <h2 class="mt-5 max-w-2xl text-3xl font-light leading-tight md:text-5xl">
            如果你愿意，可以从一次简单的了解开始。
          </h2>
          <p class="mt-7 max-w-2xl leading-8 text-stone-300">
            咨询可根据来访者议题与现实情况进行初步沟通。建议首次联系时简要说明咨询期待、可预约时间与所在城市。
          </p>
        </div>

        <div class="border border-white/15 bg-white/[0.04] p-7 md:p-8">
          <dl class="space-y-6 text-sm">
            <div>
              <dt class="text-stone-400">咨询群体</dt>
              <dd class="mt-2 text-base leading-7">成人个体咨询 / 青少年个体咨询 / 家庭治疗</dd>
            </div>
            <div>
              <dt class="text-stone-400">咨询收费</dt>
              <dd class="mt-2 text-base leading-7">400 元 / 50 分钟；600 元 / 90 分钟</dd>
            </div>
            <div>
              <dt class="text-stone-400">咨询方式</dt>
              <dd class="mt-2 text-base leading-7">线上 / 成都</dd>
            </div>
            <div>
              <dt class="text-stone-400">邮箱</dt>
              <dd class="mt-2 text-base">
                <a href="mailto:383558947@qq.com" class="underline decoration-white/30 underline-offset-4 transition hover:text-[#d0a54a]">
                  383558947@qq.com
                </a>
              </dd>
            </div>
            <div>
              <dt class="text-stone-400">电话</dt>
              <dd class="mt-2 text-base">
                <a href="tel:15282820570" class="underline decoration-white/30 underline-offset-4 transition hover:text-[#d0a54a]">
                  15282820570
                </a>
              </dd>
            </div>
          </dl>
        </div>
      </div>
    </section>
  </main>
</template>
