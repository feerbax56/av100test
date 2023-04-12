<template>
    <div class="mainBlock">
        <div class="nameBlock">Прочие настройки</div>
        <div class="bodyBlock">
            <div class="labelBlock">
                <label class="multiselectCaption">Часовой пояс</label>
                <v-select class="inputSity"
                          clearable
                          :placeholder="timezonestring"
                          :items="['Калининград', 'Москва', 'Самара', 'Екатеринбург', 'Омск', 'Красноярск','Иркутск', 'Якутск', 'Владивасток', 'Магадан', 'Камчатка' ]"
                ></v-select>
            </div>
            <div class="checkBoxBlock">
                <div class="labelBlock">
                    <v-checkbox label="Автоматически переходить к новым объявлениям" color="success"></v-checkbox>
                    <img src="../assets/info-svgrepo-com.svg" class="infoImg">
                </div>
                <div class="labelBlock">
                    <v-checkbox label="Включить цвета в ленте" color="success"></v-checkbox>
                    <img src="../assets/info-svgrepo-com.svg" class="infoImg">
                </div>

            </div>

            <button class="btnSave">
                Сохранить
            </button>
        </div>

    </div>


</template>

<script>
export default {
    name: 'OtherSettings',
    props: ['timezonestring'],


}

</script>

<style>
.multiselectCaption {
    margin: 4px 25px 0 0;
    font-size: 14px;
}

.inputSity {
    width: 214px;
    height: 28px;
    margin: 0;
}

.labelBlock {
    display: flex;
    align-content: center;
    align-items: center;
}

.checkBoxBlock {
    display: flex;
    margin: 25px;
    flex-direction: column;
}

.btnSave {
    background-color: rgb(45, 197, 116);
    display: block;
    width: 100%;
    height: 44px;
    padding: 13px 20px;
    font-size: 13px;
    color: white;
    border-radius: 5px;
}

.btnSave:active {
    background: #26a763;
}
</style>