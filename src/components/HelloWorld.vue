<template>
  <div class="page">
    <div class="box">
      <el-avatar icon="el-icon-user-solid" style="margin-bottom: 50px;font-size: 30px;"></el-avatar>
      <el-form :model="loginform" ref="loginform" :rules="rules">
        <el-form-item label="用户名" prop="name" class="labelrow">
          <el-input v-model="loginform.name" placeholder="请输入用户名"></el-input>
        </el-form-item>
        <el-form-item label="密 码" prop="pwd" class="labelrow">
          <el-input v-model="loginform.pwd" placeholder="请输入密码"></el-input>
        </el-form-item>
        <el-form-item class="btarea">
          <el-button type="primary" @click="login('loginform')">登录</el-button>
          <el-button @click="reset('loginform')">重置</el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data() {
      return {
        loginform: {
          name: '',
          pwd: ''
        },
        rules: {
          name: [{ required: true, message: '请输入用户名', trigger: 'blur' }],
          pwd: [{ required: true, message: '请输入密码', trigger: 'blur' }]
        }
      }
    },
    methods: {
      login(fornName) {
        this.$refs[fornName].validate((valid) => {
          if (valid) {
            this.$router.push({ name: 'MyPage', params: { usr: this.loginform.name } })
            console.log('登录成功')
          } else {
            console.log('error')
            return false
          }
        })

      },
      reset(formName) {
        this.$refs[formName].resetFields();
        console.log('重置成功')
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .page {
    width: 100%;
    height: 100%;
    background-image: url('../assets/bg.jpg');
  }

  .box {
    width: 400px;
    height: 400px;
    border-radius: 5px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    position: relative;
    left: 35%;
    top: 20%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: rgba(255, 255, 255, 0.05);
  }

  .labelrow {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    padding: 0;
    font-size: 20;
    margin-bottom: 40px;
    color: #fff;
  }

  .labelrow .el-form-item__label {
    font-size: 16px;
    color: #DCDFE6;
    margin-right: 10px;
  }

  .el-input__inner {
    background-color: rgba(255, 255, 255, 0.05);
    color: #DCDFE6;
  }

  .btarea {
    margin-top: 20px;
    margin-bottom: 0px;
  }

  .el-button {
    margin-right: 10px;
  }
</style>