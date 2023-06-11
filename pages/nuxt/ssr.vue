<template>
  <DefaultWidth>
    <div class="space-y-5">
      <div>
        <H1>SSR (Servier Side Rendering)</H1>
        <Paragraph> 1. Faster initial page load time </Paragraph>
        <Paragraph> 2. Improved SEO </Paragraph>
        <Paragraph> 3. Better performance on low-powered devices </Paragraph>
        <Paragraph>
          4. Better accessibility: the content is immediately available on the
          initial page load
        </Paragraph>
        <Paragraph>
          5. Easier caching: pages can be cached on the server-side, which can
          further improve performance by reducing the amount of time it takes to
          generate and send the content to the client.
        </Paragraph>
        <Paragraph>
          * Overall, server-side rendering can provide a faster and more
          efficient user experience, as well as improve search engine
          optimization and accessibility.
        </Paragraph>
        <Paragraph>
          * As Nuxt is a versatile framework, it gives you the possibility to
          statically render your whole application to a static hosting with nuxt
          generate, disable SSR globally with the
          <span class="font-semibold text-red-500">ssr: false</span> option or
          leverage hybrid rendering by setting up the routeRules option.
        </Paragraph>
      </div>
    </div>
  </DefaultWidth>
</template>