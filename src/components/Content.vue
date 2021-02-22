<template>
  <div class="pf_content">
    <div class="pf_content_left">
      <el-form label-position="right" label-width="80px">
        <el-form-item label="传送方式">
          <el-radio-group v-model="form.radio">
            <el-radio :label="1">发送端</el-radio>
            <el-radio :label="2">接收端</el-radio>
          </el-radio-group>
        </el-form-item>
        <el-form-item label="缓冲大小">
          <el-input type="text" onkeyup="value=value.replace(/[^\d]/g,'')" style="width: 160px; margin-top: 4px;" v-model="form.buzSize" size="small">
            <el-select v-model="form.buzUnit" slot="append" placeholder="请选择">
              <el-option label="字节" value="1"></el-option>
              <el-option label="KB" value="2"></el-option>
              <el-option label="MB" value="3"></el-option>
            </el-select>
          </el-input>
        </el-form-item>
        <el-form-item label="传输ip">
          <el-input v-model="form.ip" style="width: 160px;" placeholder="请输入接收端 ip 地址" size="small">
          </el-input>
        </el-form-item>
      </el-form>

    </div>
    <div class="pf_content_right">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        radio: 1,
        buzSize: 1024,
        buzUnit: '2',
        ip: ''
      }

    }
  }
}
</script>

<style lang="scss">
 @import '../assets/css/content.scss';
</style>