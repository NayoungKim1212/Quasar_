<template>
    <q-page padding>
        <div class="text-h4">커뮤니티 목록</div>
        <section class="q-qutter-y-sm q-mt-lg">
            <!--<q-card v-for="id in 100" :key="id" @click="goPostDetails(id)"></q-card>-->
            <q-card v-for="id in 100" :key="id"> <!--1부터 100까지 순회, 각 id에 대해 <q-card> 컴포넌트를 생성-->
                <router-link :to="`/posts/${id}`">
                    <q-card-section>
                        {{ id }}게시글</q-card-section>
                </router-link>
            </q-card>
        </section>
    </q-page>
</template>

<script setup>
import { useRouter } from 'vue-router';

const router = useRouter();
//const goPostDetails = {id} => router.push(`/posts/${id}`);
</script>

<style lang="scss" scoped></style>