<template>
    <div>
        <div class="test-h5 text-center text-weight-bold q-mb-xl">비밀번호 찾기</div>
        <q-form class="q-gutter-y-md"> <!--gutter : column간의 간격-->
            <q-input placeholder="가입한 이메일" outlined dense />
            <div>
                <q-btn label="확인" class="full-width" unelvaled color="primary" />
            </div>
            <q-separator /> <!---라인이 생성-->
            <q-btn label="로그인하기" 
            class="full-width" 
            unelvaled 
            flat 
            @click="$emit('changeView', 'SignInForm')"/>
        </q-form>
    </div>
</template>

<script setup>
defineEmits(['changeView']);
</script>

<style lang="scss" scoped></style>