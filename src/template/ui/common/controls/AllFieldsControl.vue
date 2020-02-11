<template>
    <div class="controlItemWrapper" :class="control.className" :data-control-name="control.name">
        <div class="tools" @click="removeItem(control.name)"><span class="clickable fa fa-times"></span></div>
        <div class="controlItem row" :id="control.name">

            <label :class="{'bold': control.labelBold, 'italic': control.labelItalic, 'underline': control.labelUnderline}" v-html="control.label"></label>
        </div>
    </div>
</template>

<script>

    export default {
        name: "AllFieldsControl",
        props: ['control', 'labelPosition'],
        methods: {
            removeItem: function(name) {
                this.$emit('removeItem', name);
            }
        }
    }
</script>

<style scoped>

</style>
