<template>
    <q-layout view="hHh lpR fFf" class="bg-grey-2">
        <!--H: 아래로 스크롤 하면 Header 고정, h: Header 비고정 --->
        <q-header bordered class="bg-white text-grey-9">
            <q-toolbar>
                <q-btn flat dense to="/"> <!--그림자를 제거하기 위해 flat, 버튼을 조금 더 얇게 만들기 위해 dense-->
                    <q-toolbar-title>
                        <q-avatar>
                            <img src="/logo.png"> <!--이미지 경로 : public 아래에 위치-->
                        </q-avatar>
                        Happy Market
                    </q-toolbar-title>
                </q-btn>
                <q-space />
                <q-btn stretch flat label="Home" to="/home" /> <!--router를 통해 이동할 때는 to-->
                <q-space /> <!--버튼에 의해 컴포넌트가 한 쪽으로 쏠렸을 경우 사용-->
                <q-btn stretch flat label="리빙윈도" href="https://shopping.naver.com/living/homeliving/home" target="_blank" />
                <q-btn stretch flat label="푸드윈도" href="https://shopping.naver.com/fresh/directfarm/home" target="_blank" />
                <q-btn stretch flat label="장보기" href="https://shopping.naver.com/market/emart/home" target="_blank" />
                <!---외부 링크로 연결 시 새 창을 띄워 보내기 위해 target="_blank" 사용-->
                <q-separator class="q-my-md q-mr-md" vertical />
                <q-btn unelvaled rounded color="primary" label="로그인 / 회원가입" @click="openAuthDialog" />
                <!---그림자 제거를 위해 unelvaled, 둥글게 표현하기 위해 rounded-->
            </q-toolbar>
        </q-header>

        <q-page-container :style="pageContainerStyles">
            <router-view />
        </q-page-container>
        <AuthDialog v-model="authDialog" />
    </q-layout>
</template>

<script setup>
import { computed, ref } from 'vue';
import { useRoute } from 'vue-router';
import AuthDialog from 'src/components/auth/AuthDialog.vue'

const route = useRoute();

const pageContainerStyles = computed(() => ({
    maxWidth: route.meta?.width || '1080px', // route에 meta에 width가 있으면 해당 width 적용 없으면 1080px 적용
    margin: '0 auto'
}));

const authDialog = ref(true); // true일 경우 자동으로 팝업을 띄움(새로고침할 때마다 띄움)
const openAuthDialog = () => (authDialog.value = true);

</script>