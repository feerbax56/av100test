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
                    <input type="checkbox" id="auto" value="auto" v-model="checkedNames">
                    <label for="auto">Автоматически переходить к новым объявлениям</label>
                    <!--                    <v-checkbox label="Автоматически переходить к новым объявлениям" color="success"></v-checkbox>-->
                    <img src="../assets/info-svgrepo-com.svg" class="infoImg" alt="infoImg">
                </div>
                <div class="labelBlock">
                    <input type="checkbox" id="color" value="color" v-model="checkedNames">
                    <label for="color">Включить цвета в ленте</label>
                    <!--                    <v-checkbox label="Включить цвета в ленте" color="success"></v-checkbox>-->
                    <img src="../assets/info-svgrepo-com.svg" class="infoImg" alt="infoImg">
                </div>

            </div>


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


</style>