<script setup>
const credentials = [
  { value: '1000h+', label: '累计咨询时长' },
  { value: '250h+', label: '持续个体与团体督导' },
  { value: '100h+', label: '个人体验' },
]

const profileNotes = [
  ['咨询取向', '系统家庭治疗 / 正念减压 / 认知行为疗法'],
  ['工作对象', '成人个体 / 青少年 / 家庭关系'],
  ['咨询方式', '线上咨询 / 成都面询'],
]

const services = [
  {
    title: '成人个体咨询',
    scope: '情绪 · 关系 · 自我探索',
    desc: '适用于情绪压力、关系困扰、自我探索、边界议题与长期反复出现的内在模式，结合系统视角、认知行为与正念训练开展支持。',
  },
  {
    title: '青少年心理支持',
    scope: '学习压力 · 人际适应 · 亲子互动',
    desc: '基于学校心理中心与高中工作经验，关注学习压力、人际适应、情绪波动、亲子沟通与青春期自我认同。',
  },
  {
    title: '家庭治疗与亲子沟通',
    scope: '家庭系统 · 依恋 · 边界',
    desc: '受训于系统家庭治疗、依恋理论与中德模式家庭治疗，帮助家庭理解互动循环，看见关系中的需要与边界。',
  },
  {
    title: '正念课程与团体辅导',
    scope: 'MBCT · 减压课程 · 团体支持',
    desc: '结合 MBCT 师资培训、八周正念课程与 28 天正念减压课程经验，面向学校、机构与社群开展团体支持。',
  },
]

const approachPoints = [
  {
    title: '从系统中理解个人',
    desc: '把困扰放回关系、家庭、学校或工作情境中理解，而不是孤立地看待一个人的情绪。',
  },
  {
    title: '在稳定觉察中处理情绪',
    desc: '结合正念训练与咨询对话，帮助来访者更清楚地辨认情绪、身体感受和内在需要。',
  },
  {
    title: '重视持续训练与督导',
    desc: '以长期受训、个人体验和督导维持专业敏感度，让咨询保持温和而有边界。',
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
  {
    place: '四川大学心理中心',
    date: '2024.9 至今',
    role: '高校心理咨询与支持',
    desc: '持续参与高校心理支持工作，面对青年学生在学业、人际、自我发展和情绪调节中的复杂处境。',
  },
  {
    place: '嘉祥教育集团',
    date: '2024.10 至今',
    role: '学校与家庭教育项目',
    desc: '面向学校与家庭场景开展心理支持、家庭教育与青少年成长相关工作，连接学生、家长与教育系统。',
  },
  {
    place: '鸿鹤高中',
    date: '2023.7-2024.10',
    role: '中学心理工作',
    desc: '在高中场域中支持青少年应对学习压力、同伴关系、亲子沟通和成长阶段中的自我认同议题。',
  },
  {
    place: '四川和光临床心理研究院',
    date: '2022-2024',
    role: '临床心理机构经验',
    desc: '在临床心理机构中积累个体咨询、课程与项目经验，深化对系统家庭治疗和认知行为取向的应用。',
  },
  {
    place: '西南大学心理中心',
    date: '2021.4-2023.6',
    role: '高校心理中心训练',
    desc: '在硕士阶段进入高校心理中心工作与学习，建立咨询基本功、个案理解与持续督导的专业习惯。',
  },
  {
    place: '今心空间 / 中加正念协会',
    date: '2023.9',
    role: '28 天正念减压课程',
    desc: '参与正念减压课程项目，将正念练习与团体支持结合，服务于压力管理和自我觉察训练。',
  },
]

const contactNotes = [
  '简要说明想咨询的议题或目前困扰',
  '说明方便预约的时间段与咨询方式',
  '首次沟通后再确认是否进入正式咨询',
]

const contactSteps = [
  ['01', '初步联系', '简要说明咨询期待与方便沟通的时间。'],
  ['02', '确认匹配', '根据议题、咨询方式和时间安排进行初步确认。'],
  ['03', '开始咨询', '确定咨询设置后，进入稳定、持续的工作。'],
]

const contactIssues = ['情绪压力', '关系困扰', '亲子沟通', '青少年成长', '正念减压', '自我探索']
</script>

<template>
  <main class="min-h-screen bg-[#f7f3ec] text-stone-800 antialiased">
    <header class="fixed left-0 right-0 top-0 z-50 border-b border-stone-200/70 bg-[#f7f3ec]/90 backdrop-blur-md">
      <div class="mx-auto flex max-w-6xl items-center justify-between px-4 py-3 md:px-6 md:py-4">
        <a href="#" class="text-base font-medium tracking-wide text-stone-900">
          石婷 Sting
        </a>

        <nav class="hidden items-center gap-7 text-sm text-stone-500 md:flex">
          <a href="#about" class="transition hover:text-stone-900">专业背景</a>
          <a href="#services" class="transition hover:text-stone-900">咨询方向</a>
          <a href="#training" class="transition hover:text-stone-900">受训经历</a>
          <a href="#experience" class="transition hover:text-stone-900">职业路径</a>
          <NuxtLink to="/activities" class="transition hover:text-stone-900">活动成果</NuxtLink>
          <a href="#contact" class="transition hover:text-stone-900">预约咨询</a>
        </nav>
      </div>

      <nav class="scrollbar-none flex gap-5 overflow-x-auto border-t border-stone-200/60 px-4 py-2 text-sm text-stone-500 md:hidden">
        <a href="#about" class="shrink-0">专业背景</a>
        <a href="#services" class="shrink-0">咨询方向</a>
        <a href="#training" class="shrink-0">受训经历</a>
        <a href="#experience" class="shrink-0">职业路径</a>
        <NuxtLink to="/activities" class="shrink-0">活动成果</NuxtLink>
        <a href="#contact" class="shrink-0">预约咨询</a>
      </nav>
    </header>

    <section class="relative overflow-hidden pt-24 md:pt-20">
      <div class="pointer-events-none absolute inset-x-0 top-0 h-32 border-b border-stone-200 bg-[#edf0e9] md:h-40"></div>

      <div class="reveal relative mx-auto grid max-w-6xl items-start gap-9 px-4 py-7 md:grid-cols-[1.05fr_0.95fr] md:px-6 md:py-12">
        <div>
          <p class="mb-4 text-xs font-medium uppercase tracking-[0.22em] text-[#a47c2b] md:mb-5 md:tracking-[0.28em]">
            Psychological Counseling
          </p>

          <h1 class="max-w-3xl text-[2.35rem] font-light leading-[1.18] text-stone-900 md:text-6xl">
            在关系、情绪与自我之间，陪你慢慢看见内心的需要
          </h1>

          <p class="mt-6 max-w-2xl text-base leading-8 text-stone-600 md:mt-7 md:text-lg">
            注册系统心理咨询师，多伦多正念研究中心 MBCT 受训背景。面向成人、青少年与家庭关系议题，提供个体咨询、正念减压与团体心理支持。
          </p>

          <div class="mt-7 grid max-w-2xl grid-cols-3 border-y border-stone-300/80 md:mt-9">
            <div
              v-for="item in credentials"
              :key="item.label"
              class="border-r border-stone-300/80 px-2 py-4 last:border-r-0 md:px-0 md:py-5"
            >
              <p class="text-xl font-light text-stone-900 md:text-3xl">{{ item.value }}</p>
              <p class="mt-1 text-xs leading-5 text-stone-500 md:text-sm">{{ item.label }}</p>
            </div>
          </div>

          <div class="mt-7 grid gap-3 sm:flex sm:flex-wrap md:mt-9">
            <a
              href="#contact"
              class="rounded-full bg-[#26332f] px-6 py-3 text-center text-sm font-medium text-white shadow-sm transition hover:bg-stone-900"
            >
              预约咨询
            </a>
            <a
              href="#about"
              class="rounded-full border border-stone-300 px-6 py-3 text-center text-sm font-medium text-stone-700 transition hover:border-stone-500 hover:bg-white"
            >
              查看专业背景
            </a>
            <NuxtLink
              to="/activities"
              class="rounded-full border border-[#5f766f]/40 px-6 py-3 text-center text-sm font-medium text-[#26332f] transition hover:border-[#5f766f] hover:bg-[#edf0e9]"
            >
              活动与成果
            </NuxtLink>
          </div>
        </div>

        <div class="mx-auto w-full max-w-md md:max-w-none">
          <div class="aspect-[4/5] max-h-[560px] overflow-hidden rounded-lg border-[8px] border-white bg-stone-200 shadow-[0_28px_80px_rgba(68,64,60,0.18)] md:border-[10px]">
            <img
              src="/images/profile.jpg"
              alt="石婷个人照片"
              class="h-full w-full object-cover"
            />
          </div>

          <div class="mt-5 border border-stone-200 bg-white/75 shadow-sm backdrop-blur">
            <div
              v-for="[label, value] in profileNotes"
              :key="label"
              class="grid gap-1 border-b border-stone-200 px-4 py-3 text-sm last:border-b-0 sm:grid-cols-[5rem_1fr] sm:gap-4 md:px-5 md:py-4"
            >
              <p class="text-stone-400">{{ label }}</p>
              <p class="leading-6 text-stone-700">{{ value }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="about" class="reveal border-t border-stone-200 py-16 md:py-28">
      <div class="mx-auto grid max-w-6xl gap-9 px-4 md:grid-cols-[0.75fr_1.25fr] md:gap-12 md:px-6">
        <div>
          <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#a47c2b]">About</p>
          <h2 class="mt-5 text-3xl font-light leading-tight text-stone-900 md:text-5xl">
            以系统视角理解关系，以正念训练陪伴情绪。
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
              石婷是应用心理学硕士、注册系统心理咨询师，长期接受系统家庭治疗、依恋理论、认知行为疗法、正念减压、人本主义与焦点解决短期疗法等方向训练，并持续接受个体与团体督导。
            </p>
            <p>
              工作经验覆盖四川大学心理中心、西南大学心理中心、中学心理支持、教育集团家庭教育项目、临床心理机构与正念课程。咨询中，她更关注个体所处的关系系统、情绪背后的需要，以及一个人如何在更稳定的觉察中重新理解自己。
            </p>
          </div>

          <div class="grid gap-px overflow-hidden border border-stone-300 bg-stone-300 md:grid-cols-3">
            <article
              v-for="point in approachPoints"
              :key="point.title"
              class="bg-[#f7f3ec] p-5"
            >
              <h3 class="text-base font-medium text-stone-900">{{ point.title }}</h3>
              <p class="mt-3 text-sm leading-7 text-stone-600">{{ point.desc }}</p>
            </article>
          </div>
        </div>
      </div>
    </section>

    <section id="services" class="reveal bg-[#e9e4db] py-16 md:py-28">
      <div class="mx-auto max-w-6xl px-4 md:px-6">
        <div class="mb-12 max-w-3xl">
          <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#a47c2b]">Services</p>
          <h2 class="mt-5 text-3xl font-light text-stone-900 md:text-5xl">咨询与支持方向</h2>
        </div>

        <div class="grid gap-px overflow-hidden border border-stone-300/80 bg-stone-300/80 md:grid-cols-2">
          <article
            v-for="(service, index) in services"
            :key="service.title"
            class="group bg-[#f7f3ec] p-7 transition duration-300 hover:bg-white md:p-9"
          >
            <div class="flex items-start justify-between gap-6">
              <div>
                <p class="text-xs font-medium uppercase tracking-[0.22em] text-[#a47c2b]">
                  0{{ index + 1 }}
                </p>
                <h3 class="mt-4 text-xl font-medium text-stone-900">{{ service.title }}</h3>
              </div>
              <span class="mt-1 h-2 w-2 shrink-0 rounded-full bg-[#5f766f] transition group-hover:scale-125"></span>
            </div>
            <p class="mt-4 text-sm text-stone-500">{{ service.scope }}</p>
            <p class="mt-4 leading-7 text-stone-600">{{ service.desc }}</p>
          </article>
        </div>
      </div>
    </section>

    <section id="training" class="reveal py-16 md:py-28">
      <div class="mx-auto max-w-6xl px-4 md:px-6">
        <div class="mb-12 grid gap-6 md:grid-cols-[0.9fr_1.1fr] md:items-end">
          <div>
            <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#a47c2b]">Training</p>
            <h2 class="mt-5 text-3xl font-light leading-tight text-stone-900 md:text-5xl">
              持续受训，持续督导。
            </h2>
          </div>

          <p class="max-w-2xl leading-8 text-stone-600 md:justify-self-end">
            咨询师的专业性不只来自证书，也来自长期训练、个人体验、督导与真实工作场景中的反思。
          </p>
        </div>

        <div class="grid gap-x-10 border-t border-stone-300 md:grid-cols-2">
          <div
            v-for="[name, date] in trainings"
            :key="`${name}-${date}`"
            class="grid gap-2 border-b border-stone-200 py-4 text-sm md:grid-cols-[1fr_6.5rem] md:gap-6"
          >
            <p class="leading-7 text-stone-800">{{ name }}</p>
            <p class="text-stone-500 md:text-right">{{ date }}</p>
          </div>
        </div>
      </div>
    </section>

    <section id="experience" class="reveal bg-white py-16 md:py-28">
      <div class="mx-auto max-w-6xl px-4 md:px-6">
        <div class="mb-12 grid gap-6 md:grid-cols-[0.95fr_1.05fr] md:items-end">
          <div>
            <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#a47c2b]">Experience</p>
            <h2 class="mt-5 text-3xl font-light leading-tight text-stone-900 md:text-5xl">
              从高校、学校到家庭系统的职业路径。
            </h2>
          </div>
          <p class="max-w-2xl leading-8 text-stone-600 md:justify-self-end">
            她的经历不是单一咨询室经验，而是穿行在高校、中学、教育集团、临床心理机构与正念课程之间，逐渐形成面向个体与系统的工作方式。
          </p>
        </div>

        <div class="relative border-l border-stone-300">
          <article
            v-for="(item, index) in experience"
            :key="`${item.place}-${item.date}`"
            class="relative grid gap-4 border-b border-stone-200 pb-7 pl-5 pt-7 first:pt-0 last:border-b-0 md:grid-cols-[10rem_1fr] md:gap-10 md:pl-8 md:pt-8"
          >
            <span class="absolute -left-[5px] top-9 h-2.5 w-2.5 rounded-full border-2 border-white bg-[#5f766f] shadow-sm"></span>
            <div>
              <p class="text-xs font-medium uppercase tracking-[0.22em] text-[#a47c2b]">
                Path 0{{ index + 1 }}
              </p>
              <p class="mt-3 text-sm leading-6 text-stone-500">{{ item.date }}</p>
            </div>
            <div class="border border-stone-200 bg-[#fbfaf7] p-5 transition duration-300 hover:border-stone-300 hover:bg-white md:p-6">
              <h3 class="text-xl font-medium text-stone-900">{{ item.place }}</h3>
              <p class="mt-2 text-sm text-[#5f766f]">{{ item.role }}</p>
              <p class="mt-5 leading-7 text-stone-600">{{ item.desc }}</p>
            </div>
          </article>
        </div>
      </div>
    </section>

    <section id="contact" class="reveal bg-[#202a27] py-16 text-white md:py-28">
      <div class="mx-auto grid max-w-6xl gap-10 px-4 md:grid-cols-[1fr_0.9fr] md:gap-12 md:px-6">
        <div>
          <p class="text-xs font-medium uppercase tracking-[0.28em] text-[#d0a54a]">Contact</p>
          <h2 class="mt-5 max-w-2xl text-3xl font-light leading-tight md:text-5xl">
            如果你愿意，可以从一次简单的了解开始。
          </h2>
          <p class="mt-7 max-w-2xl leading-8 text-stone-300">
            咨询可根据来访者议题与现实情况进行初步沟通。建议首次联系时简要说明咨询期待、可预约时间与所在城市。
          </p>

          <div class="mt-10 grid gap-px overflow-hidden border border-white/15 bg-white/15">
            <div
              v-for="[number, title, desc] in contactSteps"
              :key="title"
              class="grid gap-4 bg-[#202a27] p-5 md:grid-cols-[4.5rem_1fr]"
            >
              <p class="text-sm font-medium tracking-[0.2em] text-[#d0a54a]">{{ number }}</p>
              <div>
                <h3 class="text-base font-medium text-white">{{ title }}</h3>
                <p class="mt-2 text-sm leading-6 text-stone-300">{{ desc }}</p>
              </div>
            </div>
          </div>

          <div class="mt-8">
            <p class="text-sm text-stone-400">常见咨询议题</p>
            <div class="mt-4 flex flex-wrap gap-2">
              <span
                v-for="issue in contactIssues"
                :key="issue"
                class="border border-white/15 px-3 py-1.5 text-sm text-stone-200"
              >
                {{ issue }}
              </span>
            </div>
          </div>

          <div class="mt-8 flex flex-wrap gap-3">
            <a
              href="mailto:383558947@qq.com"
              class="rounded-full bg-white px-5 py-3 text-sm font-medium text-[#202a27] transition hover:bg-stone-100"
            >
              邮件预约
            </a>
            <a
              href="tel:15282820570"
              class="rounded-full border border-white/20 px-5 py-3 text-sm font-medium text-white transition hover:border-white/40 hover:bg-white/5"
            >
              电话联系
            </a>
          </div>
        </div>

        <div class="border border-white/15 bg-white/[0.05] p-7 shadow-2xl shadow-black/10 md:p-8">
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

          <div class="mt-8 border-t border-white/15 pt-7">
            <p class="text-sm text-stone-400">预约前可以准备</p>
            <ul class="mt-4 space-y-3">
              <li
                v-for="note in contactNotes"
                :key="note"
                class="flex gap-3 text-sm leading-6 text-stone-200"
              >
                <span class="mt-2 h-1.5 w-1.5 shrink-0 rounded-full bg-[#d0a54a]"></span>
                <span>{{ note }}</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>
