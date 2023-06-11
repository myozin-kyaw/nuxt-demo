<template>
    <DefaultWidth>
        <div class="space-y-5">
            <div>
                <H1>Nuxt Configs</H1>
                <Paragraph>1. runtimeConfig ( <OtherLink href="https://nuxt.com/docs/getting-started/configuration" name="link"/> ) </Paragraph>
                <Paragraph>2. App Configuration</Paragraph>
            </div>
            <div>
                <H1>Runtime Config</H1>
                <Paragraph>
                    * By default, Nuxt has config <span class="text-emerald-400">(nuxt.config.ts)</span> 
                    file can override or extend this default configuration by adding custom scripts, register modules or change rendering modes.
                </Paragraph>
            </div>
            <div>
                <H1>Nuxt Default Configuration reference</H1>
                <Paragraph>
                    Link : <OtherLink href="https://nuxt.com/docs/api/configuration/nuxt-config" name="Configuration reference"/>
                </Paragraph>
            </div>
            <div>
                <H1>Environment Variables and Private Tokens</H1>
                <Paragraph>
                    * By default, <span class="text-emerald-400">runtimeConfig</span> keys are only available <span class="text-emerald-400">server-side</span>. <br/> 
                    * The key with <span class="text-emerald-400">runtimeConfig.public</span> are also available <span class="text-emerald-400">client-side</span> <br/>
                    * Serialization : <span class="underline">Your runtime config will be serialized before being passed to Nitro</span>
                </Paragraph>
            </div>
            <div>
                <H1>Why should use runtimeConfig</H1>
                <Paragraph>
                    In Nuxt.js, the runtimeConfig option allows you to define runtime configuration variables 
                    that can be accessed both on the server and the client side. It provides a way to pass 
                    dynamic configuration values to your Nuxt.js application without hardcoding them into your codebase.
                </Paragraph>
            </div>
        </div>
    </DefaultWidth>
</template>