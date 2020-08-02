<script>
export default {
  name: 'VueYedProgressbar', // vue component name
  props:{
    progressColor:{
      type:String,
      required: false,
      default:"colorBlue",
      validator:function(value){
        return ['colorRed', 'colorOrange', 'colorYellow','colorGreen','colorPurple','colorPink','colorBlue'].indexOf(value) !== -1
      }
    },
    progressStripeMode:{
      type:Boolean,
      required:false
    },
    progressStripe:{
      type:String,
      required:false,
      default:"stripeBlue",
      validator:function(value){
        return ['stripeGray', 'stripeGreen', 'stripeYellow','stripePurple','stripePink','stripeOrange','stripeRed','stripeBlue'].indexOf(value) !== -1
      }
    },
    progressTextColor:{
      type:String,
      required:false,
      default: "#fff"
    },
    percent:{
      type:Number,
      required:true,
      default:100
    }
  }
};
</script>

<template>
  <div class="yedprogress" >
    <div class="yedprogressbar" :class="progressStripeMode===false?progressColor:progressStripe" :style="{width:percent+'%'}">
    </div>
    <div class="yedprogresstext" :style="{color:progressTextColor}"><em> %{{percent}}</em></div>

  </div>
</template>

<style scoped>
  .yedprogress {
    font-size: 14px;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
    background: #e9ecef;
    box-sizing: border-box;
    border: 1px solid #ccc;
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
    border-top-left-radius: 8px;
    border-top-right-radius: 8px;
    height: 20px;
    display: flex;
    position: relative;
    align-items: center;
  }

  .yedprogressbar {
    border-bottom-left-radius: 8px;
    border-bottom-right-radius: 8px;
    border-top-left-radius: 8px;
    border-top-right-radius: 8px;
    display: flex;
    align-items: center;
    height: 20px;
    transition: width .6s ease;
  }

  .yedprogresstext {
    color: white;
    position: absolute;
    left: 50%;
    bottom: 0.5px;
  }

  .colorRed {
    background: #f5222d;
  }

  .colorOrange {
    background: #fa541c;
  }

  .colorYellow {
    background: #faad14;
  }
  .colorGreen{
    background: #52c41a;
  }
  .colorPurple{
    background: #722ed1;
  }
  .colorPink{
    background: #eb2f96;
  }
  .colorBlue{
    background: #2f54eb;
  }
  .stripeBlue{
    background: repeating-linear-gradient(
            45deg,
            #69c0ff,
            #69c0ff 10px,
            #1890ff 10px,
            #1890ff 20px
    );
  }
  .stripeRed{
    background: repeating-linear-gradient(
            45deg,
            #ff7875,
            #ff7875 10px,
            #cf1322 10px,
            #cf1322 20px
    );
  }
  .stripeOrange{
    background: repeating-linear-gradient(
            45deg,
            #ff9c6e,
            #ff9c6e 10px,
            #fa541c 10px,
            #fa541c 20px
    );
  }
  .stripePink{
    background: repeating-linear-gradient(
            45deg,
            #ff85c0,
            #ff85c0 10px,
            #eb2f96 10px,
            #eb2f96 20px
    );
  }
  .stripePurple{
    background: repeating-linear-gradient(
            45deg,
            #b37feb,
            #b37feb 10px,
            #722ed1 10px,
            #722ed1 20px
    );
  }
  .stripeYellow{
    background: repeating-linear-gradient(
            45deg,
            #ffd666,
            #ffd666 10px,
            #faad14 10px,
            #faad14 20px
    );
  }
  .stripeGreen{
    background: repeating-linear-gradient(
            45deg,
            #95de64,
            #95de64 10px,
            #52c41a 10px,
            #52c41a 20px
    );
  }
  .stripeGray{
    background: repeating-linear-gradient(
            45deg,
            #d9d9d9,
            #d9d9d9 10px,
            #8c8c8c 10px,
            #8c8c8c 20px
    );
  }

</style>
