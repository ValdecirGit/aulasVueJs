<template>
    <div :class="baseClass">
        <slot/>
    </div>
</template>

<script>
    export default {
        props: ['variant', 'test'],

        computed: {
            baseClass() {
                return [
                    'alert',
                    this.variant ? `alert-${this.variant}` : ''
                ]
            }
        }
    }
</script>


<style scoped>
.alert {
    padding: 10px;
    border-radius: 10px;
    color: gray;
    background: #ddd;
}

.alert-success {
    padding: 10px;
    border-radius: 10px;
    color:white;
    background:green;
}

.alert-danger {
    padding: 10px;
    border-radius: 10px;
    color:white;
    background:red;
}
.alert-warning {
    padding: 10px;
    border-radius: 10px;
    color:white;
    background:orange;
}
</style>