<template>
  <div class="connect-device-login" id="connect-device-login">
  
    <div class="img-container">
        <img src="~/img/logo1.png" />
        <div style="color:white; font-size:11px">
            <i>Quản lý những gì bạn muốn</i>
        </div>
    </div>
    <div class="input-container">
        <i class="fa fa-user icon"></i>
        <input class="input-field" type="text" placeholder="Tên gian hàng" v-model="brandName">
    </div>

    <div class="input-container">
        <i class="fa fa-user icon"></i>
        <input class="input-field" type="text" placeholder="Tên đăng nhập" v-model="userLogin">
    </div>

    <div class="input-container">
        <i class="fa fa-key icon"></i>
        <input class="input-field" type="password" placeholder="Mật khẩu" v-model="password">
    </div>
    <div class="input-container">
        <label style="font-size:12px">
            <input type="checkbox" v-model="remember" v-on:change="ClickRemember" />
            Ghi nhớ mật khẩu
        </label>

    </div>
    <div class="text" style="color:red; height:20px" v-if="error!==''">
        <i>
            {{error}}
        </i>
    </div>
    <div class="input-container">
        <button type="submit" class="btn" v-on:click="Login">Đăng nhập</button>
    </div>
    <div class="text">
        <i>
            Tổng đài hỗ trợ 0247 303 9333
        </i>
    </div>


</div>

</template>

<script>
export default {
  name: 'Login',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
 * {
        box-sizing: border-box;
    }

    /* Style the input container */
    .input-container {
        display: flex;
        width: 100%;
        margin-bottom: 15px;
        padding-left: 20px;
        padding-right: 20px;
    }

    /* Style the form icons */
    .icon {
        padding: 10px;
        background: #0097c4;
        color: white;
        min-width: 50px;
        text-align: center;
    }

    /* Style the input fields */
    .input-field {
        width: 100%;
        padding: 10px;
        outline: none;
    }

        .input-field:focus {
            border: 2px solid dodgerblue;
        }

    /* Set a style for the submit button */
    .btn {
        background-color: #0097c4;
        color: white;
        padding: 10px 20px;
        border: none;
        cursor: pointer;
        width: 100%;
        opacity: 0.9;
        margin-left: 35%;
        margin-right: 35%;
    }

        .btn:hover {
            opacity: 1;
        }

    .connect-device-login {
        width: 25%;
        margin: 0 auto;
        font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
        border: 1px solid #d3d3d3;
    }

    .img-container {
        width: auto;
        text-align: center;
    }

        .img-container div {
            color: white;
            font-size: 11px;
        }

    .text {
        text-align: center;
        font-size: 12px;
    }
</style>
