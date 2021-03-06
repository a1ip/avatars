![DiceBear Avatars - Avataaars Sprite Collection](https://raw.githubusercontent.com/DiceBear/avatars/master/packages/avatars-avataaars-sprites/banner.svg?sanitize=true)

![license](https://img.shields.io/github/license/dicebear/avatars-avataaars-sprites.svg)
[![npm](https://img.shields.io/npm/v/@dicebear/avatars-avataaars-sprites.svg)](https://www.npmjs.com/package/@dicebear/avatars-avataaars-sprites)

Designed by [Pablo Stanley](https://twitter.com/pablostanley), the Sketch library can be found on
[avataaars.com](https://avataaars.com/).

<p>
    <img src="https://avatars.dicebear.com/v2/avataaars/1.svg" width="60" />
    <img src="https://avatars.dicebear.com/v2/avataaars/2.svg" width="60" />
    <img src="https://avatars.dicebear.com/v2/avataaars/3.svg" width="60" />
    <img src="https://avatars.dicebear.com/v2/avataaars/4.svg" width="60" />
    <img src="https://avatars.dicebear.com/v2/avataaars/5.svg" width="60" />
    <img src="https://avatars.dicebear.com/v2/avataaars/6.svg" width="60" />
    <img src="https://avatars.dicebear.com/v2/avataaars/7.svg" width="60" />
    <img src="https://avatars.dicebear.com/v2/avataaars/8.svg" width="60" />
    <img src="https://avatars.dicebear.com/v2/avataaars/9.svg" width="60" />
</p>

## Usage

### HTTP-API (recommended)

Our free HTTP-API is the easiest way to use this sprite collection. Just use the following URL as image source.

    https://avatars.dicebear.com/v2/avataaars/:seed.svg

The value of `:seed` can be anything you like - but **don't** use any sensitive or personal data here! The GET parameter
`option` can be used to pass [options](#options).

#### Examples

| preview                                                                                                                              | url                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------- |
| <img src="https://avatars.dicebear.com/v2/avataaars/example.svg" width="60" />                                                       | https://avatars.dicebear.com/v2/avataaars/example.svg                                                       |
| <img src="https://avatars.dicebear.com/v2/avataaars/example.svg?options[top][]=longHair&options[facialHairChance]=0" width="60" />   | https://avatars.dicebear.com/v2/avataaars/example.svg?options[top][]=longHair&options[facialHairChance]=0   |
| <img src="https://avatars.dicebear.com/v2/avataaars/example.svg?options[top][]=longHair&options[facialHairChance]=100" width="60" /> | https://avatars.dicebear.com/v2/avataaars/example.svg?options[top][]=longHair&options[facialHairChance]=100 |

### NPM

Install the Avatars and this sprite collection with the following command.

    npm install --save @dicebear/avatars @dicebear/avatars-avataaars-sprites react react-dom

Now you are ready to create your first Avatar.

```js
import Avatars from '@dicebear/avatars';
import sprites from '@dicebear/avatars-avataaars-sprites';

let options = {};
let avatars = new Avatars(sprites(options));
let svg = avatars.create('custom-seed');
```

## Options

| name              | type             | default       | description                                                                                                                                  |
| ----------------- | ---------------- | ------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| style             | string           | `transparent` | One of: `transparent`, `circle`                                                                                                              |
| mode              | string           | `include`     | `include` or `exclude` passed options.                                                                                                       |
| top               | array of strings | `null`        | Possible values: `longHair`, `shortHair`, `eyepatch`, `hat`, `hijab`, `turban`                                                               |
| topChance         | number           | `100`         | Probability in percent                                                                                                                       |
| hatColor          | array of strings | `null`        | Possible values: `black`, `blue`, `gray`, `heather`, `pastel`, `pink`, `red`, `white`                                                        |
| hairColor         | array of strings | `null`        | Possible values: `auburn`, `black`, `blonde`, `brown`, `pastel`, `platinum`, `red`, `gray`                                                   |
| accessories       | array of strings | `null`        | Possible values: `kurt`, `prescription01`, `prescription02`, `round`, `sunglasses`, `wayfarers`                                              |
| accessoriesChance | number           | `10`          | Probability in percent                                                                                                                       |
| facialHair        | array of strings | `null`        | Possible values: `medium`, `light`, `magestic`, `fancy`, `magnum`                                                                            |
| facialHairChance  | number           | `10`          | Probability in percent                                                                                                                       |
| facialHairColor   | array of strings | `null`        | Possible values: `auburn`, `black`, `blonde`, `brown`, `platinum`, `red`                                                                     |
| clothes           | array of strings | `null`        | Possible values: `blazer`, `sweater`, `shirt`, `hoodie`, `overall`                                                                           |
| clothesColor      | array of strings | `null`        | Possible values: `black`, `blue`, `gray`, `heather`, `pastel`, `pink`, `red`, `white`                                                        |
| eyes              | array of strings | `null`        | Possible values: `close`, `cry`, `default`, `dizzy`, `roll`, `happy`, `hearts`, `side`, `squint`, `surprised`, `wink`, `winkWacky`           |
| eyebrow           | array of strings | `null`        | Possible values: `angry`, `default`, `flat`, `raised`, `sad`, `unibrow`, `up`                                                                |
| mouth             | array of strings | `null`        | Possible values: `concerned`, `default`, `disbelief`, `eating`, `grimace`, `sad`, `scream`, `serious`, `smile`, `tongue`, `twinkle`, `vomit` |
| skin              | array of strings | `null`        | Possible values: `tanned`, `yellow`, `pale`, `light`, `brown`, `darkBrown`, `black`                                                          |

## Further informations

You can find the DiceBear Avatars documentation at [avatars.dicebear.com](https://avatars.dicebear.com)
