<template>
    <button @click="$emit('click')">
        <slot>提交</slot>
    </button>
    
</template>
<script>
export default {
    data() {
        return {
            innerLabelWidth: 0
        }
    },
    created() {
        this.innerLabelWidth = this.$parent.$props && this.$parent.$props.labelWidth || 0;
    }
}
</script>
<style scoped>
    button {
        width: 150px;
        height: 40px;
        border-radius: 5px;
        font-size: 18px;
        background: #38A2FF;
        color: white;
        border: #38A2FF solid 1px;
    }
    button:hover {
        cursor: pointer;
    }
</style>
