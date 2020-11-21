<template>
    <div class="area">
         <div class="clock-area">
              <div class="timer">{{hour == 0 ? 12 : hour}}:{{ munite }}:{{second}} {{am_pm}} </div>
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
            am_pm: '',

            
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
            // get am or pm 
            if(this.hour >= 12){
                this.am_pm = 'pm';
            }else{
                this.am_pm = 'am';
            }

            // if munite is less then 10 then add zero in front 
            if(datesetup.getMinutes() < 10){
                this.munite = '0'+datesetup.getMinutes();
            }else{
                this.munite = datesetup.getMinutes();
            }

            // if second is less then 10 add zero in front
            if(datesetup.getSeconds()<10){
               this.second = '0'+datesetup.getSeconds();
            }else{
                this.second = datesetup.getSeconds();
            }
            

        },1000);
          
    },

}
</script>
