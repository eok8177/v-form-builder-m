<template>
    <div class="row" style="margin: 0 20px;">
        <div class="col-md-8">
            <section-component :form="form" ref="SectionComponent"></section-component>
        </div>
        <div class="col-md-4">
            <sidebar-component></sidebar-component>
        </div>
    </div>
</template>

<script>
    import SectionComponent from "./ui/SectionComponent";
    import { dom } from '@fortawesome/fontawesome-svg-core'
    import SidebarComponent from "./ui/SidebarComponent";
    dom.watch();

    var default_form_value = () => ({
        sections: [],
        layout: "",
        _uniqueId: Math.random()
    });

    export default {
        name: "form-builder-template",
        components: {
            SidebarComponent,
            SectionComponent
        },
        props: {
            form: {
                type: Object
            }
        },
        methods: {
            getValue() {
                return this.form;
            },
            setValue(val) {
                this.form = val;
            }
        }
    }
</script>

<style scoped>

</style>
