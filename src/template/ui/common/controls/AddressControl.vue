<template>
    <div class="controlItemWrapper" :class="control.className" :data-control-name="control.name">
        <div class="tools" @click="removeItem(control.name)"><span class="clickable fa fa-times"></span></div>

        <!-- <div class="controlItem row" :id="control.name" v-if="labelPosition === 'left'"> -->
        <!-- </div> -->
        <div class="controlItem" :id="control.name">
            <div class="row">
                <div class="form-group col-md-12">
                    <label :class="{'bold': control.labelBold, 'italic': control.labelItalic, 'underline': control.labelUnderline}" v-html="control.label1"></label>
                    <div class="input-group">
                        <input type="text" class="form-control"
                               :readonly="control.readonly"
                               :name="control.fieldName + '1'"
                               >
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="form-group col-md-12">
                    <label :class="{'bold': control.labelBold, 'italic': control.labelItalic, 'underline': control.labelUnderline}" v-html="control.label2"></label>
                    <div class="input-group">
                        <input type="text" class="form-control"
                               :readonly="control.readonly"
                               :name="control.fieldName + '2'"
                               >
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="form-group col-md-12">
                    <label :class="{'bold': control.labelBold, 'italic': control.labelItalic, 'underline': control.labelUnderline}" v-html="control.label3"></label>
                    <div class="input-group">
                        <input type="text" class="form-control"
                               :readonly="control.readonly"
                               :name="control.fieldName + '3'"
                               >
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="form-group col-md-12">
                    <label :class="{'bold': control.labelBold, 'italic': control.labelItalic, 'underline': control.labelUnderline}" v-html="control.label4"></label>
                    <div class="input-group">
                        <input type="text" class="form-control"
                               :readonly="control.readonly"
                               :name="control.fieldName + '4'"
                               >
                    </div>
                </div>
            </div>
        </div>


    </div>
</template>

<script>
    export default {
        name: "AddressControl",
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
