<template>
    <q-layout view="hHh lpR fFf">

        <q-header bordered class="bg-white text-grey-9">
            <q-toolbar>
                <q-btn flat dense> <!--그림자를 제거하기 위해 flat, 버튼을 조금 더 얇게 만들기 위해 dense-->
                    <q-toolbar-title>
                        <q-avatar>
                            <img src="/logo.png"> <!--이미지 경로 : public 아래에 위치-->
                        </q-avatar>
                        Happy Market
                    </q-toolbar-title>
                </q-btn>
                <q-space /> <!--버튼에 의해 컴포넌트가 한 쪽으로 쏠렸을 경우 사용-->
                <q-btn stretch flat label="장보기" href="https://shopping.naver.com/market/emart/home" target="_blank" />
                <!---외부 링크로 연결 시 새 창을 띄워 보내기 위해 target="_blank" 사용--> 
                <q-separator class="q-my-md q-mr-md" vertical />
                <q-btn unelvaled rounded color="primary" label="로그인 / 회원가입" />
                <!---그림자 제거를 위해 unelvaled, 둥글게 표현하기 위해 rounded-->
            </q-toolbar>
        </q-header>

        <q-page-container>
            <router-view />
        </q-page-container>
    </q-layout>
</template>