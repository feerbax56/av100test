<template>
    <div class="mainBlock">
        <div class="nameBlock">Учётная запись</div>
        <div class="bodyBlock">
            <div>
                <div>
                    <div class="inputBlock">
                        <label class="inputName">Компания</label>
                        <div>
                            <input type="text" name="text-field" :placeholder='companyname' readonly="readonly"
                                   class="input">
                        </div>
                    </div>
                    <div class="inputBlock">
                        <label class="inputName">Логин</label>
                        <div>
                            <input type="text" name="text-field" :placeholder='login'
                                   class="input">
                        </div>
                    </div>
                    <div class="inputBlock">
                        <label class="inputName">Номер телефона</label>
                        <div>
                            <input type="text" name="text-field" :placeholder='phone' class="input">
                        </div>
                    </div>
                    <div class="inputBlock">
                        <label class="inputName">Имя</label>
                        <div>
                            <input type="text" name="text-field" :placeholder='fname' class="input">
                        </div>
                    </div>
                </div>
                <div class="inputBlock">
                    <label class="inputName">Фамилия</label>
                    <div>
                        <input type="text" name="text-field" :placeholder='lname' class="input">
                        <small>* Не обязательно</small>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MeAccount',
    props: ['companyname', 'login', 'phone', 'fname', 'lname'],
    methods: {
        check() {
            console.log(this.phone)
        }
    },
}
</script>

<style>
.input {
    border: 1px solid beige;
    border-radius: 3px;
    width: 190px;
    font-size: 12px;
    margin: 5px;
}

.inputName {
    width: 96px;
    font-size: 12px;
}

.inputBlock {
    display: flex;

}
</style>