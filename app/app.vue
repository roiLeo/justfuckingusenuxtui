<script setup>
useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/favicon.ico' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

const title = 'Just Fucking Use Nuxt UI - Stop Wasting Time Building Components'
const description = 'Stop reinventing the wheel. Nuxt UI is a fully customizable, accessible component library built on Headless UI and Tailwind CSS. Tree-shakeable, dark mode ready, and 30+ components that actually work. Just fucking use it.'

useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: '/ogImage.png',
  twitterImage: '/ogImage.png',
  twitterCard: 'summary_large_image'
})
</script>

<template>
  <UApp>
    <UHeader :toggle="false">
      <template #left>
        <NuxtLink to="/">
          <AppLogo class="w-auto h-6 shrink-0" />
        </NuxtLink>

        <TemplateMenu />
      </template>

      <template #right>
        <UColorModeButton />
      </template>
    </UHeader>

    <UMain>
      <UContainer>
        <NuxtPage class="prose dark:prose-invert prose-lg max-w-3xl mx-auto py-12 px-4 sm:px-6 lg:px-8 selection:bg-primary selection:text-white" />
      </UContainer>
    </UMain>

    <USeparator icon="i-simple-icons-nuxtdotjs" />

    <UFooter>
      <template #left>
        <div class="flex-row">
          <div class="text-sm text-muted">
            Learn more at <ULink to="https://ui.nuxt.com">ui.nuxt.com</ULink>
          </div>
          <div class="text-sm text-muted italic">
            Made with ❤️ and frustration for developers who waste time reinventing wheels
          </div>
        </div>
      </template>

      <template #right>
        <UButton
          to="https://github.com/roiLeo/justfuckingusenuxtui"
          target="_blank"
          icon="i-simple-icons-github"
          aria-label="GitHub"
          color="neutral"
          variant="ghost"
        />
      </template>
    </UFooter>
  </UApp>
</template>