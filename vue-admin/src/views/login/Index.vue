<template>
    <div id="login">
        <div class="login-wrap" >
            <el-form :model="form"  label-width="80px">
                <el-form-item class="item_wrap">
                    <el-input prefix-icon="el-icon-user" v-model="form.name" clearable></el-input>
                </el-form-item>
                <el-form-item class="item_wrap">
                    <el-input prefix-icon="el-icon-unlock" v-model="form.pwd" show-password style="border-radius:30px"></el-input>
                </el-form-item>
                <el-form-item class="item_wrap">
                      <el-checkbox v-model="form.checked">记住我</el-checkbox>  注册
                </el-form-item>
                <el-form-item class="item_wrap">
                    <el-button id="submitBtn" type="primary" @click="onSubmit">登入</el-button>
                </el-form-item>
            </el-form>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return {
            form: {
                name:'周坤',
                pwd:'123456',
                checked:false
            }
        }
    },
    methods:{
        //提交
        onSubmit(){

        }
    }
}
</script>
// scoped 加上之后之后样式文件只对当前有效
<style lang="scss" scoped>

#login{
    height: 100vh;
    background-color:#F08080;

    .login-wrap{
    
       position: relative;
       top: 25%;
       padding: 50px;
       width: 30%;
       background-color: white;
       margin: 0 auto;
       border-radius: 10px;
    }

}
#submitBtn{
    width: 100%;
}

.el-form-item__content{
    margin-left: 0px;
}
</style>