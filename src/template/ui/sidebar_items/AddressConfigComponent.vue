<template>
    <div>
        <div class="form-group">
            <label>Label 1</label>
            <input type="text" class="form-control" v-model="control.label1" placeholder="Address line">
        </div>
        <div class="form-group">
            <label>Label 2</label>
            <input type="text" class="form-control" v-model="control.label2" placeholder="Address line2">
        </div>
        <div class="form-group">
            <label>Label 3</label>
            <input type="text" class="form-control" v-model="control.label3" placeholder="Postcode">
        </div>
        <div class="form-group">
            <label>Label 4</label>
            <input type="text" class="form-control" v-model="control.label4" placeholder="Country">
        </div>
    </div>
</template>

<script>
    export default {
        name: "AddressConfigComponent",
        props: {
            control: {
                type: Object
            },
        },
    }
</script>

<style scoped>

</style>
