<script setup lang="ts">
import { Form as AForm } from '@arco-design/web-vue'
import { reactive } from 'vue'

const formData = reactive({})
</script>

<template>
    <!-- running type-check gets the following error -->
    <!-- error TS2742: The inferred type of '__VLS_template' cannot be named without a reference to '.pnpm/scroll-into-view-if-needed@2.2.31/node_modules/scroll-into-view-if-needed'. This is likely not portable. A type annotation is necessary. -->
    <slot></slot>
    <a-form
        ref="formRef"
        :model="formData" />

    <!-- following also gets error -->
    <!-- <a-form
        ref="formRef"
        :model="formData">
        <slot></slot>
    </a-form> -->
</template>
