nft art generator project made with javascript and canvas api and nodejs

Before you use the nft art generator project, make sure you have node.js and yarn installed.

## Installation 🛠️

If you are cloning the project then run this first, otherwise you can download the source code on the release page and skip this step.

```sh
git clonehttps://github.com/tarunwalia12345/nft-art-generator-project
```

Go to the root of your folder and run this command if you have yarn installed.

```sh
yarn install
```

Alternatively you can run this command if you have node installed.

```sh
npm install // I prefer NPM over Yarn
```

## Usage ℹ️

Create your different layers as folders in the 'layers' directory, and add all the layer assets in these directories. You can name the assets anything as long as it has a rarity weight attached in the file name like so: `example element#70.png`. You can optionally change the delimiter `#` to anything you would like to use in the variable `rarityDelimiter` in the `src/config.js` file.

Once you have all your layers, go into `src/config.js` and update the `layerConfigurations` objects `layersOrder` array to be your layer folders name in order of the back layer to the front layer.

_Example:_ If you were creating a portrait design, you might have a background,antena,body,ear,chess,ear base, hand shadow,etc so your `layersOrder` would look something like this:
```js
const layerConfigurations = [
 {
    growEditionSizeTo: 10, 
    layersOrder: [
      { name: "background" },
      { name: "upper stomach" },
      { name: "stomach" },
      { name: "hips" },
      { name: "obliques" },
      { name: "arm joint" },
      { name: "head" },
      { name: "upper neck" },
      { name: "neck" },
      { name: "body" },
      { name: "left fore arm" },
      { name: "right arm" },
      { name: "left arm" },
      { name: "hand shadow" },
      { name: "hands" },
      { name: "right fore arm" },
      { name: "ear base" },
      { name: "ear" },
      { name: "mouth" },
      { name: "eye base" },
      { name: "oculus" },
      
     
      { name: "antena" },
      { name: "shoulders" },
      { name: "shoulders cover" },
      { name: "elbows" },
      { name: "elbows cover" },
     
      { name: "chest" },
      { name: "outline" },
      


      


    ],
  },
]; 
```

The `name` of each layer object represents the name of the folder (in `/layers/`) that the images reside in.

Optionally you can now add multiple different `layerConfigurations` to your collection. Each configuration can be unique and have different layer orders, use the same layers or introduce new ones. This gives the artist flexibility when it comes to fine tuning their collections to their needs.







Here is a list of the different blending modes that you can optionally use.

```js
const MODE = {
  sourceOver: "source-over",
  sourceIn: "source-in",
  sourceOut: "source-out",
  sourceAtop: "source-out",
  destinationOver: "destination-over",
  destinationIn: "destination-in",
  destinationOut: "destination-out",
  destinationAtop: "destination-atop",
  lighter: "lighter",
  copy: "copy",
  xor: "xor",
  multiply: "multiply",
  screen: "screen",
  overlay: "overlay",
  darken: "darken",
  lighten: "lighten",
  colorDodge: "color-dodge",
  colorBurn: "color-burn",
  hardLight: "hard-light",
  softLight: "soft-light",
  difference: "difference",
  exclusion: "exclusion",
  hue: "hue",
  saturation: "saturation",
  color: "color",
  luminosity: "luminosity",
};
```

When you are all ready, run the following command and your outputted art will be in the `build/images` directory and the json in the `build/json` directory:

```sh
npm run build
```

or

```sh
node index.js
```

The program will output all the images in the `build/images` directory along with the metadata files in the `build/json` directory. Each collection will have a `_metadata.json` file that consists of all the metadata in the collection inside the `build/json` directory. The `build/json` folder also will contain all the single json files that represent each image file. The single json file of a image will look something like this:

```json
{
  "dna": "92ed7f14e73f7dbb87d555de7544b1f6b6dcb779",
  "name": "#1",
  "description": "nft art generator project is a project build for buidl it hackathon where you can create nft collection by coding",
  "image": "undefined/1.png",
  "edition": 1,
  "date": 1639405013942,
  "attributes": [
    {
      "trait_type": "background",
      "value": "background5"
    },
    {
      "trait_type": "upper stomach",
      "value": "upperStomach2"
    },
    {
      "trait_type": "stomach",
      "value": "STOMACH2"
    },
    {
      "trait_type": "hips",
      "value": "hips2"
    },
    {
      "trait_type": "obliques",
      "value": "obliques2"
    },
    {
      "trait_type": "arm joint",
      "value": "armjoint"
    },
    {
      "trait_type": "head",
      "value": "head2"
    },
    {
      "trait_type": "upper neck",
      "value": "upperneck1"
    },
    {
      "trait_type": "neck",
      "value": "neck2"
    },
    {
      "trait_type": "body",
      "value": "body1"
    },
    {
      "trait_type": "left fore arm",
      "value": "left-fore-arm2"
    },
    {
      "trait_type": "right arm",
      "value": "right-Arm2"
    },
    {
      "trait_type": "left arm",
      "value": "leftArm1"
    },
    {
      "trait_type": "hand shadow",
      "value": "hand-shadow1"
    },
    {
      "trait_type": "hands",
      "value": "hands2"
    },
    {
      "trait_type": "right fore arm",
      "value": "right-fore-arm1"
    },
    {
      "trait_type": "ear base",
      "value": "ear-base2"
    },
    {
      "trait_type": "ear",
      "value": "ear2"
    },
    {
      "trait_type": "mouth",
      "value": "mouth1"
    },
    {
      "trait_type": "eye base",
      "value": "eyeBase2"
    },
    {
      "trait_type": "oculus",
      "value": "oculus1"
    },
    {
      "trait_type": "antena",
      "value": "antena"
    },
    {
      "trait_type": "shoulders",
      "value": "shoulders1"
    },
    {
      "trait_type": "shoulders cover",
      "value": "shoulderscover1"
    },
    {
      "trait_type": "elbows",
      "value": "elbows1"
    },
    {
      "trait_type": "elbows cover",
      "value": "elbowscover2"
    },
    {
      "trait_type": "chest",
      "value": "chest2"
    },
    {
      "trait_type": "outline",
      "value": "outline1"
    }
  ],
  "compiler": "NFT art generator project"
}
```

That's it, you're done.

### Updating baseUri for IPFS

You might possibly want to update the baseUri after you have ran your collection. To update the baseUri simply run:

```sh
node utils/updateBaseUri.js
```

### Printing rarity data (Experimental feature)

To see the percentages of each attribute across your collection, run:

```sh
node utils/rarityData.js
```

The output will look something like this:

```sh
Trait type: background
{ trait: 'background1', chance: '20', occurrence: '50' }
{ trait: 'background2', chance: '10', occurrence: '0' }
{ trait: 'background4', chance: '10', occurrence: '10' }
{ trait: 'background5', chance: '10', occurrence: '40' }

Trait type: upper stomach
{ trait: 'upperStomach1', chance: '10', occurrence: '70' }
{ trait: 'upperStomach2', chance: '5', occurrence: '30' }

Trait type: stomach
{ trait: 'STOMACH1', chance: '10', occurrence: '80' }
{ trait: 'STOMACH2', chance: '10', occurrence: '20' }

Trait type: hips
{ trait: 'hips1', chance: '10', occurrence: '50' }
{ trait: 'hips2', chance: '10', occurrence: '50' }

Trait type: obliques
{ trait: 'obliques1', chance: '10', occurrence: '50' }
{ trait: 'obliques2', chance: '10', occurrence: '50' }

Trait type: arm joint
{ trait: 'armjoint', chance: '10', occurrence: '70' }
{ trait: 'armjoint2', chance: '10', occurrence: '30' }

Trait type: head
{ trait: 'head1', chance: '10', occurrence: '50' }
{ trait: 'head2', chance: '10', occurrence: '50' }

Trait type: upper neck
{ trait: 'upperneck1', chance: '10', occurrence: '50' }
{ trait: 'upperneck2', chance: '10', occurrence: '50' }

Trait type: neck
{ trait: 'neck1', chance: '10', occurrence: '40' }
{ trait: 'neck2', chance: '10', occurrence: '60' }

Trait type: body
{ trait: 'body1', chance: '10', occurrence: '40' }
{ trait: 'body2', chance: '10', occurrence: '60' }

Trait type: left fore arm
{ trait: 'Left-fore-arm1', chance: '10', occurrence: '40' }
{ trait: 'left-fore-arm2', chance: '10', occurrence: '60' }

Trait type: right arm
{ trait: 'right-Arm1', chance: '10', occurrence: '50' }
{ trait: 'right-Arm2', chance: '10', occurrence: '50' }

Trait type: left arm
{ trait: 'leftArm1', chance: '10', occurrence: '30' }
{ trait: 'leftArm2', chance: '10', occurrence: '70' }

Trait type: hand shadow
{ trait: 'hand-shadow1', chance: '10', occurrence: '100' }

Trait type: hands
{ trait: 'hands1', chance: '10', occurrence: '70' }
{ trait: 'hands2', chance: '10', occurrence: '30' }

Trait type: right fore arm
{ trait: 'right-fore-arm1', chance: '10', occurrence: '50' }
{ trait: 'right-fore-arm2', chance: '10', occurrence: '50' }

Trait type: ear base
{ trait: 'ear-base1', chance: '10', occurrence: '70' }
{ trait: 'ear-base2', chance: '10', occurrence: '30' }

Trait type: ear
{ trait: 'ear1', chance: '10', occurrence: '60' }
{ trait: 'ear2', chance: '10', occurrence: '40' }

Trait type: mouth
{ trait: 'mouth1', chance: '10', occurrence: '70' }
{ trait: 'mouth2', chance: '10', occurrence: '30' }

Trait type: eye base
{ trait: 'eyeBase1', chance: '10', occurrence: '30' }
{ trait: 'eyeBase2', chance: '10', occurrence: '70' }

Trait type: oculus
{ trait: 'oculus1', chance: '10', occurrence: '50' }
{ trait: 'oculus2', chance: '10', occurrence: '50' }

Trait type: antena
{ trait: 'antena', chance: '1', occurrence: '100' }
{ trait: 'antena', chance: '2', occurrence: '100' }

Trait type: shoulders
{ trait: 'shoulders1', chance: '10', occurrence: '50' }
{ trait: 'shoulders2', chance: '10', occurrence: '50' }

Trait type: shoulders cover
{ trait: 'shoulderscover1', chance: '10', occurrence: '70' }
{ trait: 'shoulderscover2', chance: '5', occurrence: '30' }

Trait type: elbows
{ trait: 'elbows1', chance: '10', occurrence: '60' }
{ trait: 'elbows2', chance: '10', occurrence: '40' }

Trait type: elbows cover
{ trait: 'elbowscover1', chance: '10', occurrence: '60' }
{ trait: 'elbowscover2', chance: '10', occurrence: '40' }

Trait type: chest
{ trait: 'chest1', chance: '10', occurrence: '50' }
{ trait: 'chest2', chance: '10', occurrence: '50' }

Trait type: outline
{ trait: 'outline1', chance: '5', occurrence: '100' }
```

Hope you create some awesome artworks with this code 👄 

When you're all finished with your NFT's here, and we update your metadata .json files to the correct CID that we're going to go over in the video...


<p/>
