<template>
  <div class="q-pa-md">
    <div class="row">
      <div class="col">
        Person 1
        
      <q-card class="my-card">
        <q-img src="https://cdn.quasar.dev/img/mountains.jpg" />
      </q-card>

      </div>
      <div class="col">
        Person2
        <q-card class="my-card">
          <q-img src="https://cdn.quasar.dev/img/parallax2.jpg" />
        </q-card>
      </div>
    </div>

    <div class="row">
      <div class="col">
        <q-card class="my-card">
          <!-- <q-img 
           src="../assets/i-show-speed-speed.gif" 
           style="height: 400px"/> -->
           <q-video
            src="https://www.youtube.com/embed/I_7_sHllnyU"
            style="height: 400px"/>
        </q-card>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent, ref } from 'vue'
import EssentialLink from 'components/EssentialLink.vue'

const linksList = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev'
  },
  {
    title: 'Github',
    caption: 'github.com/quasarframework',
    icon: 'code',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Discord Chat Channel',
    caption: 'chat.quasar.dev',
    icon: 'chat',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'Forum',
    caption: 'forum.quasar.dev',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev'
  },
  {
    title: 'Twitter',
    caption: '@quasarframework',
    icon: 'rss_feed',
    link: 'https://twitter.quasar.dev'
  },
  {
    title: 'Facebook',
    caption: '@QuasarFramework',
    icon: 'public',
    link: 'https://facebook.quasar.dev'
  },
  {
    title: 'Quasar Awesome',
    caption: 'Community Quasar projects',
    icon: 'favorite',
    link: 'https://awesome.quasar.dev'
  }
]

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink
  },

  setup () {
    const leftDrawerOpen = ref(false)

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
