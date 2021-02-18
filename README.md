# React Native Bepaid

[React Native](http://facebook.github.io/react-native) library for accepting payments with [Bepaid](https://bepaid.by) SDK

# Install
Download package:
```shell
npm install --save @Goldyukol/react-native-bepaid
```

or

```shell
yarn add @Goldyukol/react-native-bepaid
```

# Methods

### createEncryptedFields()
Create encrypted card fields.
Returns a `Promise` that resolve encrypted fields (`Object`).

__Arguments__
- `cardNumber` - `String` Number of payment card.
- `cardExp` - `String` Expire date of payment card.
- `cardCvv` - `String` CVV code of payment card.
- `cardHolder` - `String` Card holder name

__Examples__
```js
import RNBepaid from 'react-native-bepaid';

const exampleCard = {
  number: '4200000000000000',
  extDate: '12/21',
  cvvCode: '123',
  cardHolder: 'IVANOV IVAN'
};

RNBepaid.createEncryptedFields(exampleCard.number, exampleCard.extDate, exampleCard.cvvCode, exampleCard.cardHolder)
  .then(encryptedFields => {
    console.log(encryptedFields);
  });
```

# License
Licensed under the MIT License.
