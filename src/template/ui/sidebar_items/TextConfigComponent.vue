<template>
    <div>
        <label>
            <input type="checkbox" name="isMultiLine" v-model="control.isMultiLine"> Multi-line?
        </label>
        <label>
            <input type="checkbox" name="isEmail" v-model="control.isEmail"> Email?
        </label>
    </div>
</template>

<script>
    export default {
        name: "TextConfigComponent",
        props: {
            control: {
                type: Object
            },
        },
    }
</script>

<style scoped>

</style>
