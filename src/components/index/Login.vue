<template>
<div>
  <el-form :model="form"
                  label-width="auto"
                  label-position="top"
                  style="max-width: 600px">
            <el-form-item label="邮箱: ">
              <el-input v-model="form.username" style="width: 300px;" placeholder="请输入你的注册邮箱"></el-input>
            </el-form-item>

            <el-form-item label="密码: ">
              <el-input v-model="form.password"
                        type="password" show-password="true"
                        placeholder="请输入你的密码"></el-input>
            </el-form-item>

            <el-form-item>
              <el-button type="primary"
                        @click="onSubmit"
                        round="true">登录</el-button>
              <el-button type="primary" @click="redirect" :link="true">
                忘记密码</el-button>
            </el-form-item>
          </el-form>
</div>
</template>

<script setup>
import { ref } from 'vue';
  import { ElForm, ElFormItem, ElInput, ElButton, ElSelect, ElOption, ElMessage } from 'element-plus';

  const form = ref({
    username: '',
    password: '',
    confirmPassword: '',
    email: '',
    position: ''
  });

  const onSubmit = () => {
    for (const key in form.value) {
      if (!form.value[key]) {
        ElMessage.error('请输入员工ID或密码');
        return;
      }
    }

    console.log('获取到的数据:', form.value);
  }

const redirect = () => {
  window.location.href='/reset';
}

</script>

<style scoped>

</style>