<template>
    <DefaultWidth>
        <div class="space-y-5">
            <div>
                <H1>Nuxt Configs</H1>
            </div>
            <div  class="grid grid-cols-1 gap-4 sm:grid-cols-2">
                <Lesson name="runtimeConfig" to="config/runtimeConfig"/>
                <Lesson name="appConfig" to="config/appConfig"/>
                <Lesson name="externalConfig" to="/"/>
            </div>
        </div>
    </DefaultWidth>
</template>