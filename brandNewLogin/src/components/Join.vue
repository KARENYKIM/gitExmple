<template>
     <article class="container">
    
        <div class="col-md-12">
        <div class="page-header">
    	    <h1>회원가입 <small>zoin form</small></h1>
        </div>
        <form class="form-horizontal">
        <div class="form-group">
          <label class="col-sm-3 control-label" for="UserId">아이디</label>
        <div class="col-sm-6">
          <input class="form-control" v-model="UserId" id="UserId" type="UserId" placeholder="아이디">
        </div>
        </div>
        <div class="form-group">
          <label class="col-sm-3 control-label" for="UserPassword">비밀번호</label>
        <div class="col-sm-6">
          <input class="form-control" v-model="UserPassword" id="UserPassword" type="password" placeholder="비밀번호">
        <!--<p class="help-block">숫자, 특수문자 포함 8자 이상</p>-->
        </div>
        </div>
          <div class="form-group">
              <label class="col-sm-3 control-label" for="UserPasswordCheck">비밀번호 확인</label>
             <div class="col-sm-6">
              <input class="form-control" v-model="UserPasswordCheck" id="UserPasswordCheck" type="password" placeholder="비밀번호 확인">
                <p class="help-block">비밀번호를 한번 더 입력해주세요.</p>
             </div>
          </div>
        <div class="form-group">
            <label class="col-sm-3 control-label" for="inputName">이름</label>
          <div class="col-sm-6">
            <input class="form-control" v-model="inputName" id="inputName" type="text" placeholder="이름">
          </div>
        </div>
        
        <div class="form-group">
          <div class="col-sm-12 text-center">
            <button class="btn btn-primary" type="submit">회원가입<i class="fa fa-check spaceLeft"></i></button>
            <button class="btn btn-danger" type="submit">가입취소<i class="fa fa-times spaceLeft"></i></button>
          </div>
        </div>
        </form>
          <hr>
        </div>
      </article>
</template>


<script>
export default {
    data() {
        return {
             UserId: '',
            UserPassword: '',
            UserPasswordCheck : '',
            inputName: ''            

        }
    }
}
</script>
