<template>
    <div>
        <div class="test-h5 text-center text-weight-bold q-mb-xl">로그인</div>
        <q-form class="q-gutter-y-md"> <!--gutter : column간의 간격-->
            <q-input placeholder="이메일" outlined dense />
            <q-input placeholder="비밀번호" outlined dense />
            <div>
                <q-btn label="로그인하기" class="full-width" unelvaled color="primary" />
                <div class="flex justify-between">
                    <q-btn label="비밀번호 찾기" color="secondary" flat dense size="13px" @click="$emit('changeView', 'FindePasswordForm')"/>
                    <q-btn label="이메일 가입하기" color="secondary" flat dense size="13px" @click="$emit('changeView', 'SignUpForm')" />
                </div>
            </div>
            <q-separator /> <!---라인이 생성-->
            <q-btn label="구글 계정으로 로그인하기" class="full-width" unelvaled color="primary" outline />
        </q-form>
    </div>
</template>

<script setup>
defineEmits(['changeView']);
</script>

<style lang="scss" scoped></style>