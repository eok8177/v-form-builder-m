<template>
    <div>
        <!-- <div class="row" v-if="labelPosition === 'left'">
        </div> -->
        <div class="form-group">
            <label :class="{'bold': control.labelBold, 'italic': control.labelItalic, 'underline': control.labelUnderline}" v-html="control.label1"></label>

            <input type="text"
                   class="form-control"
                   :name="control.fieldName + '1'"
                   v-model="control.value1" />
        </div>
        <div class="form-group">
            <label :class="{'bold': control.labelBold, 'italic': control.labelItalic, 'underline': control.labelUnderline}" v-html="control.label2"></label>

            <input type="text"
                   class="form-control"
                   :name="control.fieldName + '2'"
                   v-model="control.value2" />
        </div>
        <div class="form-group">
            <label :class="{'bold': control.labelBold, 'italic': control.labelItalic, 'underline': control.labelUnderline}" v-html="control.label3"></label>

            <input type="text"
                   class="form-control"
                   :name="control.fieldName + '3'"
                   v-model="control.value3" />
        </div>
        <div class="form-group">
            <label :class="{'bold': control.labelBold, 'italic': control.labelItalic, 'underline': control.labelUnderline}" v-html="control.label4"></label>

            <input type="text"
                   class="form-control"
                   :name="control.fieldName + '4'"
                   v-model="control.value4" />
        </div>
    </div>
</template>

<script>
    export default {
        name: "AddressControl",
        props: ['control', 'labelPosition'],
        mounted() {
        }
    }
</script>

<style scoped>

</style>
