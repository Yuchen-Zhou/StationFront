<template>
  <div>

    <el-form :model="form"
             label-width="auto"
             label-position="top"
             style="max-width: 600px">
      <el-form-item label="用户名: ">
        <el-input v-model="form.username" style="width: 300px;" placeholder="请输入你的用户名..."></el-input>
      </el-form-item>
      <el-form-item label="邮箱: ">
        <el-input v-model="form.email" placeholder="请输入你的邮箱..."></el-input>
      </el-form-item>
      <el-form-item label="密码: ">
        <el-input v-model="form.password"
                  type="password" show-password="true"
                  placeholder="请输入你的密码"></el-input>
      </el-form-item>
      <el-form-item label="确认密码: ">
        <el-input v-model="form.confirmPassword"
                  type="password" show-password="true"
                  placeholder="请再次输入你的密码"></el-input>
      </el-form-item>

      <el-form-item>
        <el-button type="primary" @click="onSubmit" :plain="true">注册</el-button>
        <el-button @click="resetForm(form)">重置</el-button>
      </el-form-item>
    </el-form>

  </div>
</template>

<script setup>
import {ref} from 'vue';
import {ElForm, ElFormItem, ElInput, ElButton, ElSelect, ElOption, ElMessage} from 'element-plus';

const form = ref({
  username: '',
  password: '',
  confirmPassword: '',
  email: '',
});

const onSubmit = () => {
  for (const key in form.value) {
    if (!form.value[key]) {
      ElMessage.error('请完整填写表单信息');
      return;
    }
  }

  if (form.value.password !== form.value.confirmPassword) {
    ElMessage.error('两次密码不一致，请重新输入');
    return;
  }

  console.log('获取到的数据:', form.value);
}

const resetForm = (form) => {
  form.username = '';
  form.password = '';
  form.confirmPassword = '';
  form.email = '';
}


</script>

<style scoped>
</style>