<template>
    <div class="mainBlock">
        <div class="nameBlock">Прочие настройки</div>
        <div class="bodyBlock">
            <div class="labelBlock">
                <label class="multiselectCaption">Часовой пояс</label>
                <v-select class="inputSity"
                          clearable
                          :items="['Калининград', 'Москва', 'Самара', 'Екатеринбург', 'Омск', 'Красноярск','Иркутск', 'Якутск', 'Владивасток', 'Магадан', 'Камчатка' ]"
                ></v-select>
            </div>

            <div class="labelBlock">
                <v-container fluid>
                    <v-checkbox
                            v-model="checkbox1"
                            :label="`Автоматически переходить к новым объявлениям`"
                    ></v-checkbox>
                    <v-checkbox
                            v-model="checkbox2"
                            :label="`Включить цвета в ленте`"
                    ></v-checkbox>
                </v-container>

                <img src="../assets/info-svgrepo-com.svg" class="infoImg">
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