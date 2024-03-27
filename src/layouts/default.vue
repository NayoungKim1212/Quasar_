<template>
    <q-layout view="hHh lpR fFf">

        <q-header elevated class="bg-primary text-white">
            <q-toolbar>
                <q-toolbar-title>

                    <q-avatar>
                        <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg">
                    </q-avatar>
                    Title
                </q-toolbar-title>
                <q-btn stretch flat label="Link" />
                <q-separator dark vertical />
                <q-btn stretch flat label="Link" />
                <q-btn stretch flat label="Link" />
                <q-separator dark vertical />
                <q-btn stretch flat label="Link" />
            </q-toolbar>
        </q-header>

        <q-page-container>
            <router-view />
        </q-page-container>
    </q-layout>
</template>