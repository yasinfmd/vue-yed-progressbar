# vue-yed-progressbar

> vue-yed-progressbar


[![NPM](https://img.shields.io/npm/v/vue-yed-progressbar.svg)](https://www.npmjs.com/package/vue-yed-progressbar) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Demo

[Demo](https://github.com/YASIINN/vue-yed-progressbar.git)


## Install
```bash
npm install --save  vue-yed-progressbar
```

## Usage

```vue
<template>
    <div id="app">
        <vue-yed-progressbar :percent="70"/>
    </div>
</template>
<script>
    import VueYedProgressbar from "vue-yed-progressbar"
    export default {
        name: 'App',
        components: {
            VueYedProgressbar
        },
    }
</script>
```

# Props
 Props Name | Description | Default Value | Required | Type | Values
 :---:  |  :----: | :---:| :---: | :---:| :---:
  percent | Percentage slice on progress | 100 | true | Number | 0-100
  progressColor | Progressbar background color | colorBlue(#2f54eb) | false |String | colorRed ,colorOrange , colorYellow ,colorGreen , colorPurple,colorPink,colorBlue
  progressTextColor|Text color showing the progressbar percentage value | #fff | false | String| rgb,hex,color
  progressStripeMode|Turns on progressbar stripe mod| null | false | Boolean |true,false
  progressStripe|Determines the stripe value if the progressbar stripe mode feature is on | stripeBlue | false | String | 'stripeGray', stripeGreen, stripeYellow,stripePurple,stripePink,stripeOrange,stripeRed,stripeBlue

## License

MIT © [yasiinn](https://github.com/YASIINN)
