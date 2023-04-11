<template>
    <div class="mainBlock">
        <div class="nameBlock">Учётная запись</div>
        <div class="bodyBlock">
            <div class="wide-section__body">
                <div class="settings-section__fields">
                    <div class="input-field settings-section__field" readonly="readonly" value="Частное лицо">
                        <label class="input-field__label caption">Компания</label>
                        <div class="input-field__main"><!---->
                            <input type="text" name="text-field" placeholder="" readonly="readonly"
                                   class="input-field__input input">
                            <div class="extra-field__currency">

                            </div>  <!----></div>
                    </div>
                    <div class="input-field settings-section__field" readonly="readonly" value="9878420298"><label
                            class="input-field__label caption">Логин</label>
                        <div class="input-field__main"><!----> <input type="text" name="text-field" placeholder=""
                                                                      readonly="readonly"
                                                                      class="input-field__input input">
                            <div class="extra-field__currency">

                            </div>  <!----></div>
                    </div>
                    <div class="input-field settings-section__field" value="79878420298"><label
                            class="input-field__label caption">Номер телефона</label>
                        <div class="input-field__main"><!----> <input type="text" name="text-field" placeholder=""
                                                                      class="input-field__input input">
                            <div class="extra-field__currency">

                            </div>  <!----></div>
                    </div>
                    <div class="input-field settings-section__field" value="Анонимус-2"><label
                            class="input-field__label caption">Имя</label>
                        <div class="input-field__main"><!----> <input type="text" name="text-field" placeholder=""
                                                                      class="input-field__input input">
                            <div class="extra-field__currency">

                            </div>  <!----></div>
                    </div>
                    <div class="input-field settings-section__field" value=""><label class="input-field__label caption">Фамилия</label>
                        <div class="input-field__main"><!----> <input type="text" name="text-field" placeholder=""
                                                                      class="input-field__input input">
                            <div class="extra-field__currency">

                            </div>
                            <small class="settings-section__info">* Не обязательно</small> <!----></div>
                    </div>
                </div>
            </div>
        </div>


    </div>


</template>

<script>
export default {
    name: 'MeAccount',
}

</script>

<style>

</style>