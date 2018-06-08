<template>
    <div>
        <input type="text" v-model="newTodoItem" placeholder="Type what you have to do" v-on:keyup.enter="addTodo"/>
        <!--button v-on:click="addTodo">추가</button-->
        <span class="addContainer" v-on:click="addTodo">
            <!--i class="addBtn fa fa-plus" aria-hidden="true"></i-->
            <i class="fas fa-plus-square" aria-hidden="true"></i>
        </span>
        <modal v-if="showModal" @close="showModal = false">
            <h3 slot="header">경고</h3>
            <span slot="footer" @click="showModal = false">
                할 일을 입력하세요.
                <i class="closeModalBtn fas fa-times" aria-hidden="true"></i>
            </span>
        </modal> 
    </div>
</template>

<script>
    import Modal from './common/Modal.vue'

    export default{
        props: ['propsdate'],
        data() {
            return {
                newTodoItem: '',
                showModal: false
            }
        },
        

        methods: {
            addTodo() {
                //console.log(this.newTodoItem); 텍스트를 저장하기 위한 버튼 이벤트 추가하기
                if(this.newTodoItem !=="" ) {
                    var value = this.newTodoItem && this.newTodoItem.trim();
                    //localStorage.setItem(this.newTodoItem, this.newTodoItem);
                    //this.$emit('addTodo', value);
                    localStorage.setItem(value, value);
                    this.propsdate.push(value);
                    this.clearInput();
                }else{
                    this.showModal =! this.showModal;
                }
                
            },
            clearInput() {
                this.newTodoItem = '';
            }
        },
        components: {
            Modal: Modal
        }
    }
</script>

<style>
    input:focus {
        ontline: none;
    }
    .inputBox {
        background: white;
        height: 50px;
        line-height: 50px;
        border-radius: 5px;
    }
    .inputBox input{
        border-style: none;
        font-size: 0.9rem;
    }
    .addContainer{
        float: right;
        background: liner-gradinet(to right, #6478FB, #8763FB);
        display: inline-block;
        width: 3rem;
        border-radius: 0 5px 5px 0;
    }
    .fas {
        color: white;
        vertical-align: middle;
    }
</style>