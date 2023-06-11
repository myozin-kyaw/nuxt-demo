<template>
  <DefaultWidth>
    <div class="space-y-5 w-[987px] mx-auto">
      <div class="flex flex-col justify-center space-y-5">
        <FolderStructure name=".nuxt"> 
          <HiddenText>
            ( Nuxt uses the .nuxt/ directory in development to generate your Vue application. )
          </HiddenText>
        </FolderStructure>
        <FolderStructure name=".output">
          <HiddenText>
            Nuxt creates the .output/ directory when building your application for production.
          </HiddenText>
        </FolderStructure>
        <FolderStructure name="assets">
          <HiddenText>
            The assets/ directory is used to add all the website's assets that the build tool (webpack or Vite) will process.
          </HiddenText>
        </FolderStructure>
        <FolderStructure name="component"></FolderStructure>
        <FolderStructure class="text-red-500" name="content"></FolderStructure>
        <FolderStructure name="layouts"></FolderStructure>
        <FolderStructure name="middleware"></FolderStructure>
        <FolderStructure class="text-red-500" name="modules"></FolderStructure>
        <FolderStructure name="node_modules"></FolderStructure>
        <FolderStructure name="pages"></FolderStructure>
        <FolderStructure class="text-red-500" name="plugins"></FolderStructure>
        <FolderStructure name="public"></FolderStructure>
        <FolderStructure name="server"></FolderStructure>
        <FolderStructure name="utils"></FolderStructure>
        <FolderStructure :isFolder="false" name=".env"></FolderStructure>
        <FolderStructure :isFolder="false" name=".gitignore"></FolderStructure>
        <FolderStructure :isFolder="false" name="app.config.ts"></FolderStructure>
        <FolderStructure :isFolder="false" name="app.vue"></FolderStructure>
        <FolderStructure :isFolder="false" name="nuxt.config.ts"></FolderStructure>
        <FolderStructure :isFolder="false" name="package.json"></FolderStructure>
        <FolderStructure :isFolder="false" name="tsconfig.json"></FolderStructure>
      </div>
      <div>
          <H1>Directory Structure</H1>
          <Paragraph>
              Link : <OtherLink href="https://nuxt.com/docs/guide/directory-structure/content" name="Directory Structure"/>
          </Paragraph>
      </div>
    </div>
  </DefaultWidth>
</template>