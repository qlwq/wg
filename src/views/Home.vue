<template>
  <div class="home">
    <div class="leftBox">
      <div class="gyBox">
        <div class="gyApp">工业APP</div>
        <div class="gyliBox">
         <div v-for="(item,index) in gyData" :key="item.name" class="ygDataBox"  >
           <div class="itemNameBox">
          自己找图标 {{item.name}}
          </div>
          <div class="indexBox" :class="backgroundC(index)">
            {{index+1}}
          </div>
        </div>
        </div>
      </div>
      <div class="yycjBox">
        <div class="gyApp">应用场景</div>
        <div class="gyliBox">
          <div v-for="(item) in yycjData" :key="item.name" 
          class="ygDataBox">
           <div class="itemNameBox">
            自己找图标 {{item.name}}
            </div>
          </div>
        </div>
      </div>
      </div>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'Home',
  data() {
    return {
      gyData:[{
        name: '智能运维'
      },
      {
        name: '设备画像'
      },
      {
        name: '云MES'
      },
      {
        name: '云备件'
      },
      {
        name: '能耗管理'
      }],
      yycjData:[{
        name: '状态监测'
      },
      {
        name: '生产制造优化'
      },
      {
        name: '远程运维'
      },
      {
        name: '预测性维护'
      },
      {
        name: '资源调度优化'
      },
      {
        name: '能耗优化'
      },
       {
        name: '质量优化'
      }
      ]
    }
  },
  methods:{
      backgroundC(index) {
       if(index+1 === 1){
        return 'color1'
       }
       if(index+1 ===2 || index+1 ===3){
         return 'color2'
       }
      return 
    }
  },
  computed: {
    
  
  }
}
</script>

<style lang="less">
.home{
  height: 100%;
  width: 100%;
  background-color: rgb(5, 35, 63);
  .leftBox{
    height: 100%;
    display: flex;
    flex-direction: column;
  }
  .gyBox{
    display: flex;
    flex-grow: 2; 
    flex-shrink:1;
    flex-direction: column;
    margin-top: 20px;
    margin-left: 30px;
    min-height: 330px;
    width: 19%;
    color: white;
    background-image: linear-gradient(rgb(24, 93, 141), rgb(13, 44, 82));;
    border:thick double rgb(84, 145, 188);
  }
  .yycjBox{
    display: flex;
    flex-grow: 3; 
    flex-shrink:1;
    flex-direction: column;
    margin-top: 20px;
    margin-left: 30px;
    min-height: 350px;
    width: 19%;
    color: white;
    background-image: linear-gradient(rgb(24, 93, 141), rgb(13, 44, 82));;
    border:thick double rgb(84, 145, 188);
  }
  .gyApp{
      text-align:left;
      padding: 20px 0px 20px 10%
    }
    .gyliBox{
      height: 100%;
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
  
      .ygDataBox{
        flex-shrink:1;
        flex-grow: 2;
        margin-bottom: 15px;
        height: 10%;
        width: 80%;
        background-color: rgb(17, 120, 178);
        display: flex;
        justify-content:space-between;
        align-items: stretch;
        text-align: center;       
    }
    }
  .itemNameBox{
    display: flex;
    align-items: center;
  }
  .indexBox{
    float: right;
    width: 20px;
    height: 20px;
    line-height: 20px;
    text-align: center;
    background-color: rgb(54, 184, 252);
  }
  .color1{
    background-color: red !important;
  }
  .color2{
   background-color: orange !important;
  }
}
</style>