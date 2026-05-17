<template>
    <UHeader title="Mon journal de trading">
        <template #right>
            <UButton label="Importer des trades" class="mr-2.5"/>
            <NuxtLink to="/profile">
                <UAvatar src="https://github.com/benjamincanac.png" />
            </NuxtLink>
        
            <UColorModeButton />
            <UButton
                color="neutral"
                variant="ghost"
                to="login"
                target="_blank"
                icon="mdi-logout"
                aria-label="GitHub"
            />
        </template>
    </UHeader>
</template>