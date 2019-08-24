<template>
    <div>
        <div>
            <h2>线形进度条 -- 百分比外显</h2>
            <v-progress :percentage="0" :show-text="false"/>
            <v-progress :percentage="80" color="yellow"/>
            <v-progress :percentage="100" status="success"/>
            <v-progress :percentage="30" status="exception"/>
            <br/>

            <h2>线形进度条 -- 百分比内显</h2>
            <v-progress :stroke-width="18" :percentage="0" :text-inside='true'/>
            <v-progress :stroke-width="18" :percentage="80" :text-inside='true'/>
            <v-progress :stroke-width="18" :percentage="100" status="success" :text-inside='true'/>
            <v-progress :stroke-width="18" :percentage="60" status="exception" :text-inside='true'/>
            <br/>

            <h2>环形进度条</h2>
            <v-progress :percentage="0" type="circle"/>
            <v-progress :percentage="80" type="circle"/>
            <v-progress :percentage="100" type="circle" status="success"/>
            <v-progress :percentage="60" type="circle" status="exception"/>

        </div>
    </div>
</template>

<script>
import VProgress from './Progress';
export default {
    components: {
        VProgress
    },
    data(){
        return{
            msg: 'hello world'
        }
    }
}
</script>

<style>
    
</style>