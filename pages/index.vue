<template>
  <div class="mb-40">
    <div class="bg-gray-900">
      <nav class="flex justify-center py-4">
        <div class="flex justify-between w-3/5">
          <h2 class="text-white text-xl font-bold">Charles Poullain</h2>
          <!-- <ul class="flex space-x-6">
            <li
              class="uppercase text-primary-600 border-primary-600 border-b-4 font-bold"
            >
              Compétences
            </li>
            <li class="uppercase text-white font-semibold">Tech</li>
            <li class="uppercase text-white font-semibold">Projets</li>
            <li class="uppercase text-white font-semibold">Blog</li>
          </ul> -->
        </div>
      </nav>
      <div class="flex justify-center pt-20 pb-40">
        <div class="flex justify-around w-3/5">
          <div class="w-1/2">
            <h1 class="text-white text-4xl font-bold">Charles Poullain</h1>
            <h3 class="text-primary-600 text-xl font-medium">
              APIs & Applications
            </h3>
            <p class="text-gray-300 mt-4">
              Après un Master en alternance, je suis devenu développeur Full
              Stack spécialisé dans l’écosystème javascript.
            </p>
            <p class="text-gray-300 mt-2">
              Je travaille au sein de l’Agence Cube, à la Roche sur Yon en tant
              que Lead Dev.
            </p>
            <button class="text-white bg-red-600 py-1 px-6 rounded-lg mt-8">
              Contactez moi
            </button>
          </div>
          <div class="flex justify-center w-1/2">
            <head-illustration></head-illustration>
          </div>
        </div>
      </div>
    </div>
    <div class="flex justify-center -mt-20">
      <div class="w-3/5 bg-white rounded-3xl">
        <div class="flex justify-around">
          <div class="flex items-center flex-col">
            <h2 class="text-center font-bold text-3xl py-6 text-gray-900">
              Quelle sont mes compétences
            </h2>
            <h3 class="text-center w-2/3 text-gray-500">
              Développement from scratch, mise à niveau, reprise de projet,
              technologies modernes…
            </h3>
          </div>
        </div>
        <div class="flex flex-row items-center flex-wrap">
          <div
            v-for="skill in skills"
            :key="skill.tite"
            class="w-1/3 px-10 py-6"
          >
            <img class="w-1/3 mb-3" :src="skill.img" />
            <h3 class="text-gray-900 text-xl font-semibold mb-2">
              {{ skill.title }}
            </h3>
            <p class="text-sm text-gray-600">{{ skill.body }}</p>
          </div>
        </div>
      </div>
    </div>
    <div class="flex justify-center -mt-20 pb-10 bg-gray-100">
      <div class="w-3/5 mt-40">
        <h3 class="text-center text-gray-900 text-2xl font-semibold mb-10">
          Les technologies que j’utilise
        </h3>
        <h4 class="text-center text-primary-600 text-3xl font-semibold mb-2">
          Chaque projet est unique avec des besoins spécifiques.
        </h4>
        <h5 class="text-center text-gray-600 text-sm">
          Pour répondre à ces besoins, je suis devenu polyvalent en utilisant
          des technologies modernes.
        </h5>
        <div class="flex flex-row items-center justify-start flex-wrap mt-8">
          <div v-for="tool in mainTools" :key="tool.title" class="w-1/4 px-6">
            <img class="w-1/3 mb-3" :src="tool.img" />
            <h3 class="text-gray-900 text-xl font-semibold mb-2">
              {{ tool.title }}
            </h3>
            <p class="text-sm text-gray-600">{{ tool.body }}</p>
          </div>
        </div>
        <div class="flex flex-col justify-center mt-10">
          <div class="flex justify-center space-x-10">
            <h4
              v-for="tool in tools1"
              :key="tool"
              class="font-bold text-gray-500 text-md"
            >
              {{ tool }}
            </h4>
          </div>
          <div class="flex justify-center space-x-8 mt-6">
            <h4
              v-for="tool in tools2"
              :key="tool"
              class="font-semibold text-gray-400 text-sm"
            >
              {{ tool }}
            </h4>
          </div>
        </div>
      </div>
    </div>
    <!-- <svg
      xmlns="http://www.w3.org/2000/svg"
      width="1920"
      height="192"
      viewBox="0 0 1920 192"
    >
      <path
        id="waves"
        d="M514.224,98.363c92.8-18.8,182.656-52.51,275.2-72.954,131.824-29.14,269.1-30.9,400.72-.68,127.9,29.3,260.528,100.751,386.912,137.054,112.08,32.207,234.448,45.47,342.944,5.228V0H0V47.666c163.945,67.715,341.781,85.248,514.224,50.7Z"
        fill="#f3f4f6"
      />
    </svg> -->
  </div>
</template>
<script>
export default {
  data: () => ({
    skills: [
      {
        title: 'Web et Mobile',
        body:
          'Le développement d’application Web et Mobiles sur mesure accompagné d’un design propre et responsive.',
        img: require('assets/skills/WebEtMobile.svg'),
      },
      {
        title: 'Web Services',
        body:
          'Le développement d’APIs de communication pour des SPA ou des applications mobiles.',
        img: require('assets/skills/WebService.svg'),
      },
      {
        title: 'Gestion de contenu',
        body:
          'L’utilisation d’outils CMS pour éditer et publier facilement du contenu.',
        img: require('assets/skills/GestionContenu.svg'),
      },
      {
        title: 'Web Design',
        body:
          'La conception et la réalisation de maquettes d’applications Web et mobiles simples.',
        img: require('assets/skills/WebDesign.svg'),
      },
      {
        title: 'Projet de A à Z',
        body:
          'La maitrise de tout les phases clés d’un projet, de sa conception jusqu’a son déploiement et son évolution.',
        img: require('assets/skills/ProjetAZ.svg'),
      },
      {
        title: 'Outils de développement',
        body:
          'L’utilisation d’outils pour faciliter le développement (syntaxe, builds, tests, …)',
        img: require('assets/skills/OutilsDev.svg'),
      },
    ],
    mainTools: [
      {
        title: 'Laravel',
        body:
          'Framework pour la création d’applications monolithiques et d’APIs',
        img: require('assets/tools/Laravel.png'),
      },
      {
        title: 'NuxtJS',
        body: 'Framework pour la création d’interfaces Web (SPA, SSG,SSR)',
        img: require('assets/tools/NuxtJS.svg'),
      },
      {
        title: 'Tailwind',
        body: 'Framework CSS orienté utility-first',
        img: require('assets/tools/Tailwind.png'),
      },
      {
        title: 'React Native',
        body: 'Framework pour la création d’applications mobile',
        img: require('assets/tools/ReactNative.png'),
      },
    ],
    tools1: ['VueJS', 'AdonisJS', 'MariaDB', 'Netlify', 'NetlifyCMS', 'Docker'],
    tools2: [
      'Slim',
      'AngularJS',
      'Cordova',
      'Ionic',
      'Gatsby',
      'Gridsome',
      'NodeJS',
    ],
  }),
}
</script>
