<template>
    <div class="alarm-setter">
        <div class="al-st-title">Set Your Alarm Bellow</div>
        <div class="alarm-setter-form">
            <form @submit.prevent="handlealarmsubmit">
                <input type="text" v-model="alarmhour">
                <input type="text" v-model="alarmmunite">
                <input type="text" v-model="alarmsecond">

                <button>Set Alarm</button>
            </form>
        </div>
    </div>
</template>
<script>
import '../assets/css/alarmsetterstyle.css';
export default {
    name: "AlarmSetterComponent",
    data:()=>{
        return{
            alarmhour: '',
            alarmmunite: '',
            alarmsecond: '',
        }
       
    },
    props:{

    },

    mounted(){

        
    },

    methods:{
        handlealarmsubmit:()=>{
          
        }
    }

    
}
</script>