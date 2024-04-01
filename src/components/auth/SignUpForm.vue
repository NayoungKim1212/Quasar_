<template>
    <div>
        <div class="test-h5 text-center text-weight-bold q-mb-xl">회원가입</div>
        <q-form class="q-gutter-y-md"> <!--gutter : column간의 간격-->
            <q-input placeholder="닉네임" outlined dense />
            <q-input placeholder="이메일" outlined dense />
            <q-input placeholder="비밀번호:문자, 숫자조합 8자 이상" outlined dense />
            <div>
                <q-btn label="가입하기" class="full-width" unelvaled color="primary" />
            </div>
            <q-separator /> <!---라인이 생성-->
            <q-btn label="로그인하기" class="full-width" unelvaled flat @click="$emit('changeView', 'SignInForm')" />
        </q-form>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped></style>