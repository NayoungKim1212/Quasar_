<template>
    <q-layout view="hHh lpR fFf">

        <q-header bordered class="bg-white text-grey-9">
            <q-toolbar>
                <q-btn flat dense>
                    <q-toolbar-title>

                        <q-avatar>
                            <img src="/logo.png">
                        </q-avatar>
                        Happy Market
                    </q-toolbar-title>
                </q-btn>
                <q-space />
                <q-btn stretch flat label="장보기" href="https://shopping.naver.com/market/emart/home" target="_blank" />
                <q-separator class="q-my-md q-mr-md" vertical />
                <q-btn unelvaled rounded color="primary" label="로그인 / 회원가입" />
            </q-toolbar>
        </q-header>

        <q-page-container>
            <router-view />
        </q-page-container>
    </q-layout>
</template>