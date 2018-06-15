<template>
    <article class="container">
        <div class="page-header">
          <h1>로그인 </h1>
        </div>
        <div class="col-md-6 col-md-offset-3">
          <form role="form">
            <div class="form-group">
              <label for="UserId">아이디</label>
              <input type="text" v-model="UserId" class="form-control" id="UserId" placeholder="아이디">
            </div>
            <div class="form-group">
              <label for="userPwd">비밀번호</label>
              <input type="password" v-model="userPwd" class="form-control" id="userPwd" placeholder="비밀번호">
            </div>
            
           
            <div class="form-group text-center">
              <button type="submit" class="btn btn-info" >로그인<i class="fa fa-check spaceLeft"></i></button>
              <router-link to="/Join" class="btn btn-danger">회원가입<i class="fa fa-check spaceLeft"></i></router-link>
              <a href="/Join.vue" class="btn btn-danger">회원가입<i class="fa fa-check spaceLeft"></i></a>
            </div>
          </form>
        </div>

      </article>
      
</template>

<script>
export default {
    data() {
        return{
            UserId: '',
            userPwd: ''
            
        }
    }
}
//   var router = [
//     {
//      path : '/Join'
//     }
//  ];

//  var router = new VueRouter({
//    routes
//  });


</script>

