<template lang="html">
<div v-if="isActive">

    <div class="row">
        <h2 class="text-center">News Items From Life Hacker</h2>
    </div>

    <div class="row">
        <div class="item">
            <h4>Simple Sidebar</h4>
            <p>This template has a responsive menu toggling system. The menu will appear collapsed on smaller screens, and will appear
                non-collapsed on larger screens.</p>
        </div>

        <div class="item">
            <h4>Simple Sidebar</h4>
            <div class="item-content">
                <p>This template has a responsive menu toggling system. The menu will appear collapsed on smaller screens, and will
                    appear non-collapsed on larger screens..</p>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default{
    props: {
        name: {required: true},
        selected: {default: false}
    },
    data(){
        return {
            isActive: false,
        }
    },
    created(){
        this.isActive = this.selected;
    },

    watch: {
        isActive (){
            console.log("Tab Changed to " + this.name);
        }
    },

}
</script>

<style lang="css">
	
</style>