<template>
    <div class="mainBlock">
        <div class="nameBlock">Оповещения о новых подборках</div>
        <div class="bodyBlock">
            <div>
                <p>
                    Выберите, куда будут приходить уведомления при появлении автомобилей, которые подходят под критерии
                    вашей подборки.
                </p>
            </div>
            <div>
                <div>
                    Уведомления
                </div>
                <div class="flexBlock">
                    <div>
                        <div>
                            <input id="is-notification-none" value="-1"
                                   type="radio" checked="checked"
                                   name="notification"
                            >
                            <label
                                    for="is-notification-none">
                                Выкл
                            </label>
                        </div>
                    </div>
                </div>
                <div class="flexBlock">
                    <div>
                        <input id="is-notification-push" value="0"
                               type="radio" disabled="disabled"
                               name="notification"
                        >
                        <label
                                for="is-notification-push">Push</label>
                    </div>
                    <div>
                            <span>
                            <img src="../assets/info-svgrepo-com.svg" class="infoImg" alt="infoImg">
                        </span>
                    </div>
                </div>
                <div class="flexBlock">
                    <div>
                        <input id="is-notification-email" value="2"
                               type="radio" checked="checked"
                               name="notification"
                        >
                        <label for="is-notification-email">Email </label>
                    </div>
                    <div>
                        <input v-model="email"
                               :rules="emailRules"
                               required class="input">
                    </div>

                    <div>
                            <span>
                            <svg width="17" height="17"
                                 viewBox="0 0 17 17" fill="none"
                                 xmlns="http://www.w3.org/2000/svg"
                            >
                                <path fill-rule="evenodd" clip-rule="evenodd"
                                      d="M9.22081 3.77446C9.63603 3.35924 10.1992 3.12598 10.7864 3.12598C12.0092 3.12598 13.0005 4.11725 13.0005 5.34004C13.0005 5.92725 12.7672 6.49041 12.352 6.90563L9.74075 9.51684C8.54147 10.7161 7.0388 11.5669 5.39341 11.9783L4.88871 12.1044C4.36527 12.2353 3.89113 11.7612 4.02199 11.2377L4.14816 10.733C4.55951 9.08763 5.41031 7.58496 6.60959 6.38568L9.22081 3.77446ZM10.7864 4.12598C10.4644 4.12598 10.1556 4.25389 9.92791 4.48157L9.52581 4.88367C9.46599 5.22738 9.63626 5.69076 10.036 6.09047C10.4357 6.49017 10.8991 6.66044 11.2428 6.60062L11.6449 6.19852C11.8725 5.97084 12.0005 5.66203 12.0005 5.34004C12.0005 4.66953 11.4569 4.12598 10.7864 4.12598ZM10.3671 7.47631C9.97046 7.32906 9.60994 7.07865 9.32886 6.79757C9.04778 6.51649 8.79738 6.15598 8.65012 5.75936L7.3167 7.09279C6.24558 8.16391 5.4857 9.506 5.11831 10.9756L5.10745 11.019L5.15087 11.0081C6.62044 10.6407 7.96253 9.88086 9.03365 8.80974L10.3671 7.47631Z"
                                      fill="#2DC574">

                                </path>
                                <path fill-rule="evenodd" clip-rule="evenodd"
                                      d="M3.33203 14.293C3.33203 14.0168 3.55589 13.793 3.83203 13.793H13.1654C13.4415 13.793 13.6654 14.0168 13.6654 14.293C13.6654 14.5691 13.4415 14.793 13.1654 14.793H3.83203C3.55589 14.793 3.33203 14.5691 3.33203 14.293Z"
                                      fill="#2DC574">

                                </path>
                            </svg>
                            </span>
                    </div>
                </div>
                <div class="flexBlock">
                    <div>
                        <input id="is-notification-telegram"
                               type="radio" name="notification"
                               value="1">
                        <label for="is-notification-telegram">
                            Telegram ID
                        </label>
                    </div>
                    <div>
                        <input type="text" name="text-field"
                               required class="input" :placeholder='telegramChat'>
                    </div>

                    <div>
                             <span>
                                <svg width="17" height="17"
                                     viewBox="0 0 17 17" fill="none"
                                     xmlns="http://www.w3.org/2000/svg"
                                >
                                    <path fill-rule="evenodd" clip-rule="evenodd"
                                          d="M9.22081 3.77446C9.63603 3.35924 10.1992 3.12598 10.7864 3.12598C12.0092 3.12598 13.0005 4.11725 13.0005 5.34004C13.0005 5.92725 12.7672 6.49041 12.352 6.90563L9.74075 9.51684C8.54147 10.7161 7.0388 11.5669 5.39341 11.9783L4.88871 12.1044C4.36527 12.2353 3.89113 11.7612 4.02199 11.2377L4.14816 10.733C4.55951 9.08763 5.41031 7.58496 6.60959 6.38568L9.22081 3.77446ZM10.7864 4.12598C10.4644 4.12598 10.1556 4.25389 9.92791 4.48157L9.52581 4.88367C9.46599 5.22738 9.63626 5.69076 10.036 6.09047C10.4357 6.49017 10.8991 6.66044 11.2428 6.60062L11.6449 6.19852C11.8725 5.97084 12.0005 5.66203 12.0005 5.34004C12.0005 4.66953 11.4569 4.12598 10.7864 4.12598ZM10.3671 7.47631C9.97046 7.32906 9.60994 7.07865 9.32886 6.79757C9.04778 6.51649 8.79738 6.15598 8.65012 5.75936L7.3167 7.09279C6.24558 8.16391 5.4857 9.506 5.11831 10.9756L5.10745 11.019L5.15087 11.0081C6.62044 10.6407 7.96253 9.88086 9.03365 8.80974L10.3671 7.47631Z"
                                          fill="#2DC574">
                                    </path>
                                    <path fill-rule="evenodd" clip-rule="evenodd"
                                          d="M3.33203 14.293C3.33203 14.0168 3.55589 13.793 3.83203 13.793H13.1654C13.4415 13.793 13.6654 14.0168 13.6654 14.293C13.6654 14.5691 13.4415 14.793 13.1654 14.793H3.83203C3.55589 14.793 3.33203 14.5691 3.33203 14.293Z"
                                          fill="#2DC574">

                                </path>
                                </svg>
                             </span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'NewCollectionAlerts',
    props: ['telegramChat',],
    data: () => ({
        valid: false,
        email: '',
        emailRules: [
            value => {
                if (value) return true

                return 'E-mail is requred.'
            },
            value => {
                if (/.+@.+\..+/.test(value)) return true

                return 'E-mail must be valid.'
            },
        ],
    }),

}

</script>

<style>
.flexBlock {
    display: flex;
    justify-content: space-between;
    width: 400px;
}

.input {
    border: 1px solid beige;
    border-radius: 3px;
    width: 190px;
    height: 20px;
    font-size: 12px;
    margin: 5px;
}
</style>