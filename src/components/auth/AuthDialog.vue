<template>
    <q-dialog :model-value="modelValue" @update:model-value="val => $emit('update:modelValue', val)"
        transition-show="none" transition-hide="none"> <!--transition 효과 제거-->
        <!--해당 value를 emit을 통해 update modelValue를 동시에 전달-->
        <q-card :style="{ width: '400px' }">
            <q-card-section class="flex">
                <q-space />
                <q-btn icon="close" flat rounded dense v-close-popup />
            </q-card-section>
            <q-card-section class="q-px-xl q-pb-xl">
                <SignInForm v-if="viewMode == 'SignInForm'" @change-view="changeViewMode" />
                <SignUpForm v-else-if="viewMode == 'SignUpForm'" @change-view="changeViewMode" />
                <FindPasswordForm v-else @change-view="changeViewMode" />
            </q-card-section>
        </q-card>
    </q-dialog>
</template>

<script setup>
import { ref, defineProps, defineEmits } from 'vue';
import SignInForm from './SignInForm.vue';
import SignUpForm from './SignUpForm.vue';
import FindPasswordForm from './FindPasswordForm.vue';

// 외부에서 v-model을 사용하기 위해 Props, Emits 사용
defineProps({ // 정의할 때
    modelValue: {
        type: Boolean,
        defalut: false
    }
});

defineEmits(['update:modelValue']);

const viewMode = ref('SignInForm'); // SignInForm, SignUpForm, FindPasswordForm
const changeViewMode = (mode) => (viewMode.value = mode); // parameter로 mode를 받음
</script>

<style lang="scss" scoped></style>