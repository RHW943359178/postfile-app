<template>
  <div class="pf_header">
    <!-- <el-form inline>
      <el-form-item label="传送方式">
        <el-radio-group v-model="form.radio">
          <el-radio :label="1">发送端</el-radio>
          <el-radio :label="2">接收端</el-radio>
        </el-radio-group>
      </el-form-item>
      <el-form-item label="缓冲区大小" >
        <el-input type="number" style="width: 200px; margin-top: 4px;" v-model="form.buzSize" size="small">
          <el-select v-model="form.buzUnit" slot="append" placeholder="请选择">
            <el-option label="字节" value="1"></el-option>
            <el-option label="KB" value="2"></el-option>
            <el-option label="MB" value="3"></el-option>
          </el-select>
        </el-input>
      </el-form-item>
    </el-form> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        radio: 1,
        buzSize: 1024,
        buzUnit: '2'
      }

    }
  }
}
</script>

<style lang="scss">
 @import '../assets/css/header.scss';
</style>