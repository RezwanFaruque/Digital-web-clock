<template>
    <div class="area">
         <div class="clock-area">
              <div class="timer">{{hour == 0 ? 12 : hour}}:{{ munite }}:{{second}}</div>
         </div>
       
    </div>
</template>

<script>
import "../assets/css/clockstyle.css";
export default {
    
    name: "ClockComponent",
    data:()=>{
        return{
            date: '',
            hour: '',
            munite: '',
            second: '',

            
        }
    },
    props:{

    },

    mounted(){

        // update data variable in every one second;
        setInterval(() => {
            
            let datesetup = new Date();
            this.date = datesetup.getDate();
            this.hour = datesetup.getHours();
            this.munite = datesetup.getMinutes();
            this.second = datesetup.getSeconds();

        },1000);
          
    },

}
</script>
