<script setup lang="ts">
type IArray = {
    tag: String;
    title: String;
    text: String;
    likes: String,
}
defineProps({
    title: String,
    tag: String,
    img_figma: Boolean,
    img_card: Boolean,
    data: String || undefined,
    tagShow: Boolean,
    horizontal: Boolean,
    vertical: Boolean,
    text: String,
    likes: String,
    data_icon: Boolean,
    ux: Boolean,
}
)
</script>
<template>
    <div :class="{'container-vertical': vertical}">
        <div :class="{ 'container-horizontal': horizontal, 'container': !horizontal }">
        
            <div v-if="img_card"><img class="card" src="./img/card_img.svg">
                </div>
                <div v-if="img_figma"><img class="figma" src="./img/figma.svg"></div>

            <div :class="{ 'body-content': horizontal }">
                <div class="tag">
                    <span v-show="tagShow" class="tag">{{ tag }}</span>
                    <div class="title-desc">
                        <div>{{ title }}</div>
                        <span>{{ text }}.</span>
                    </div>
                </div>

                <div class="footer">
                    <div>
                        <svg xmlns="http://www.w3.org/2000/svg" width="266" height="2" viewBox="0 0 266 2" fill="none">
                            <path opacity="0.2" d="M1 1H265" stroke="#333333" stroke-linecap="round" />
                        </svg>
                    </div>


                    <div class="footer-content">

                        <div v-if="data">
                            <div v-if="ux"><img src="./img/ux.png"> </div>
                            <div v-if="data_icon">
                                <svg width="24" height="24" viewBox="0 0 24 24" fill="none"
                                    xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                                    <circle cx="12" cy="12" r="12" fill="url(#pattern0)" />
                                    <defs>
                                        <pattern id="pattern0" patternContentUnits="objectBoundingBox" width="1" height="1">
                                            <use xlink:href="#image0_125_43"
                                                transform="translate(-0.016129) scale(0.0322581)" />
                                        </pattern>
                                        <image id="image0_125_43" width="32" height="31"
                                            xlink:href="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAfCAIAAAAJNFjbAAAD1klEQVR42uyWb2hb5RfHzznPc29yc5e2adKuLU3741dXa21VGFU3ihTBvRIcA0WUgeAbpfgXBd8IgiDIUHw19sa9UDYY+kKQVlGxoDjccJujVNMNNl3bNFvXrPl7k9w/R25ukqVtrG21LwQfEvKE53nO557znPM9VzIz7OQg2OHx7wfIjZeZ2QY22U47xRBpEgkBEPEfADDzopU5njofM5OEgoAYSSBFZfNjet+gEvaT3AwA12dR+amdj1YuTOWvALmmiQQyARIRIRAgtgn95ab72kj7S2/WAlYs44vMrxPZGJBwbRGtB5A7EczQLYOjvs6HfF3055jbAGa+YWXeTEzm2HSDgQI2BCC7PwC4V21/SutTUTT0pgJIlFIfJ8+cK8wTSvcYUg0QJv1+rTsqmxbt3Iy5HLfz9QB3Du6nTzY9E9ijk7IW4DjOLSv/+sInBltIgkF4AChf7LC/85XW/RKr2czwUzFxKn85BxbUA8r3H0b/S/qghhLqPMHvUrGjN74lIctGyQMIlIdb9u7TenWhMvN63wuONWn8PlWKI2IN4E1GlPAhX2+NIYxn7yQUZetYznAKkO+1yNgDgR7FDRQ2jKxAGlRao2LXnJU1wHYx6J3HRafQL5qaSa3UAVaLmQFCFHhj94GoEvL4G6Qglr/DanhYCV+2UsfzlyyoJIvDPLp09mrHmJdahGx7Rzpl07tdB6NqCLZQp8DAe5TmV/Wh/1HQs/5j0Yg7pbxjVz1AtJ3SC+0P7w/2b0O5PS/bpDa+666T+bnxlVmTWQLNO8aACFbETiAdTXw1kTzH4GxP0Wzmi6X0+Mols4xk4BCqq9UU4eTy6eevfjibj2+jBY0tnd23dMbN3PLfCKltogqomUPEnFN8a+HTY4mvs7YBW6FkHIvqpOxFvYeqN4nnM1eOLH5OSPVih4BDge6DoZEBrQs2Ic6fGdefTF5U0H3cUbXly8gIQ6V6xLF3PiDAWGFh1b0hXDdTU+mZrF3o8Ud8KL3drl6Zacux/dUIeGNA6tNmdtbKPeqPnAjdq9Dt6nGlAhFvmblTy6e/z8TW5L4XQJVkv68rKP1zxZvXSstvdz9xh9axOlndnb+Y2SEl6Lpf33A8iyFFf67jkbAMTqYulNiq7fFWTbanjWvg3mHjeHltbkgNeuFt3NGY+fHIg4daR2JG/L3ERImtVb3btYw1nzYui8ZNHyuVTXfr0SM9T/ep7bSlmt58y/QEABlNtk7c/OGb9PSatfd7D7erzX8LUD9m8vM/535bMJMOc4sIHGi+5//a7oYavk3Af6+OOw34IwAA//+XMJN6j2WOeAAAAABJRU5ErkJggg==" />
                                    </defs>
                                </svg>
                            </div>

                            <span class="footer-text">{{ data }}</span>
                        </div>
                        <div>
                            <div>
                                <svg width="14" height="14" viewBox="0 0 14 14" fill="none"
                                    xmlns="http://www.w3.org/2000/svg">
                                    <g opacity="0.6">
                                        <path fill-rule="evenodd" clip-rule="evenodd"
                                            d="M4.7236 6.99999C4.7236 8.24444 5.7423 9.25696 7.00002 9.25696C8.25205 9.25696 9.27075 8.24444 9.27075 6.99999C9.27075 5.74989 8.25205 4.73737 7.00002 4.73737C5.7423 4.73737 4.7236 5.74989 4.7236 6.99999ZM10.3464 3.52686C11.3423 4.29616 12.1903 5.42181 12.7992 6.8303C12.8447 6.93777 12.8447 7.06222 12.7992 7.16403C11.5813 9.981 9.41303 11.6667 7.00002 11.6667H6.99433C4.58701 11.6667 2.41872 9.981 1.20083 7.16403C1.1553 7.06222 1.1553 6.93777 1.20083 6.8303C2.41872 4.01333 4.58701 2.33333 6.99433 2.33333H7.00002C8.20652 2.33333 9.35043 2.75191 10.3464 3.52686ZM7.0007 8.40723C7.78038 8.40723 8.41778 7.7737 8.41778 6.99875C8.41778 6.21814 7.78038 5.58461 7.0007 5.58461C6.93241 5.58461 6.86412 5.59027 6.80152 5.60158C6.77875 6.2238 6.26656 6.72158 5.63485 6.72158H5.60639C5.58932 6.81208 5.57794 6.90259 5.57794 6.99875C5.57794 7.7737 6.21534 8.40723 7.0007 8.40723Z"
                                            fill="#333333" />
                                    </g>
                                </svg>
                            </div>
                            <span class="footer-text">{{ likes }}</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script lang="ts">
export default {
    // props:{
    //     tag: String,
    //     title: String,
    // }
}
</script>
<style scoped lang="css">
.body-content {
    display: flex;
    padding: 16px 20px;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 28px;
    flex: 1 0 0;
    align-self: stretch;
}

img.figma {
    margin-left: -24px;
    object-fit: cover;
    margin-top: -25px;
    border-radius: 8px;
}

img.card {
    border-radius: 8px;
    padding: 0px;
}

.footer-text {
    color: #333;
    font-family: Lato;
    font-size: 12px;
    font-style: normal;
    font-weight: 400;
    line-height: 140%;
    /* 16.8px */
    letter-spacing: 0.06px;
}

.footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    align-self: stretch;

    >div {
        display: flex;
        align-items: center;
        gap: 8px;
    }
}

.tag {
    color: #29C6CF;
    font-size: 12px;
    font-style: normal;
    font-weight: 550;
    line-height: 140%;
    /* 16.8px */
    letter-spacing: 0.06px;
}

.title-desc {
    text-align: left;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;
    align-self: stretch;

    >div {
        color: #333;
        font-family: Poppins;
        font-size: 20px;
        font-style: normal;
        font-weight: 700;
        line-height: 140%;
        /* 28px */
    }

    >span {
        color: #333;
        font-family: Lato;
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: 140%;
        /* 19.6px */
        letter-spacing: 0.21px;

    }

}

.container {
    display: flex;
    margin-bottom: 20px;
    padding: 24px;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 32px;
    align-self: stretch;
    background: #FFF;
    width: 264px;
    border-radius: 8px;
    background: #FFF;
    box-shadow: 0px 6px 20px 0px rgba(0, 0, 0, 0.08);
}

.container-vertical {
    display: flex;
    width: 312px;
    height: 538px;
    margin-top: -766px;
    margin-left: 340px;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    flex-shrink: 0;
    border-radius: 8px;
    background: #FFF;
    box-shadow: 0px 6px 20px 0px rgba(0, 0, 0, 0.08);
}

.container-horizontal {
    display: flex;
    width: 648px;
    height: 226px;
    justify-content: center;
    align-items: flex-start;
    border-radius: 8px;
    background: #FFF;
    box-shadow: 0px 6px 20px 0px rgba(0, 0, 0, 0.08);
}

.tag-title {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;
    align-self: stretch;
}

.footer {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 16px;
    align-self: stretch;
}</style>