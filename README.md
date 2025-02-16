[npm-version-shield]: https://img.shields.io/npm/v/rutility?style=flat&colorA=000000&colorB=000000
[npm-downloads-shield]: https://img.shields.io/npm/dt/rutility.svg?style=flat&colorA=000000&colorB=000000
[npm-url]: https://www.npmjs.com/package/rutility
[github-stars-shield]: https://img.shields.io/github/stars/wotanCode/rutility?style=flat&colorA=000000&colorB=000000
[github-url]: https://github.com/wotanCode/rutility

[![Version][npm-version-shield]][npm-url]
[![Downloads][npm-downloads-shield]][npm-url]
[![GitHub Stars][github-stars-shield]][github-url]


# RUTility
## Chilean RUT Validation and Formatting Library

A library for validating and formatting the Chilean RUT (Rol Único Tributario). This library provides functions to format the RUT with dots and dashes, as well as to validate its format and check digit.

## Installation

You can install the library using npm:

```sh
npm install rutility
```

## Usage

### Import in a Node.js Project
```javascript
const { format, calculateDv, isValidRut, isFormat } = require('rutility');
```

### Import in an ES6 Module
```sh
import { format, calculateDv, isValidRut, isFormat } from 'rutility';
```

### Formatting Functions
<table border="1">
  <thead>
    <tr>
      <th>Function</th>
      <th>Description</th>
      <th>Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>format.dot(rut: string): string</code></td>
      <td>Formats a RUT by adding dots.</td>
      <td><code>console.log(format.dot('12345678')); // '12.345.678'</code></td>
    </tr>
    <tr>
      <td><code>format.dash(rut: string): string</code></td>
      <td>Formats a RUT by adding a dash.</td>
      <td><code>console.log(format.dash('123456780')); // '12345678-0'</code></td>
    </tr>
    <tr>
      <td><code>format.dotDash(rut: string): string</code></td>
      <td>Formats a RUT by adding dots and a dash.</td>
      <td><code>console.log(format.dotDash('123456780')); // '12.345.678-0'</code></td>
    </tr>
    <tr>
      <td><code>format.notDot(rut: string): string</code></td>
      <td>Removes dots from a RUT.</td>
      <td><code>console.log(format.notDot('12.345.678-0')); // '12345678-0'</code></td>
    </tr>
    <tr>
      <td><code>format.notDash(rut: string): string</code></td>
      <td>Removes the dash and check digit from a RUT.</td>
      <td><code>console.log(format.notDash('12.345.678-0')); // '12.345.678'</code></td>
    </tr>
    <tr>
      <td><code>format.notDotDash(rut: string): string</code></td>
      <td>Removes dots and the dash from a RUT.</td>
      <td><code>console.log(format.notDotDash('12.345.678-9')); // '12345678'</code></td>
    </tr>
  </tbody>
</table>

### Validation Functions
<table border="1">
  <thead>
    <tr>
      <th>Function</th>
      <th>Description</th>
      <th>Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>calculateDv(rut: string | number): string</code></td>
      <td>Calculates the check digit of a Chilean RUT.</td>
      <td><code>console.log(calculateDv('12.345.678')); // '5'</code></td>
    </tr>
    <tr>
      <td><code>isValidRut(rut: string): boolean</code></td>
      <td>Validates if a Chilean RUT is valid.</td>
      <td><code>console.log(isValidRut('12.345.678-5')); // true</code></td>
    </tr>
  </tbody>
</table>

### Format Validations
<table border="1">
  <thead>
    <tr>
      <th>Function</th>
      <th>Description</th>
      <th>Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>isFormat.dot(rut: string): boolean</code></td>
      <td>Checks if a RUT has the correct format with dots.</td>
      <td><code>console.log(isFormat.dot('12.345.678')); // true</code></td>
    </tr>
    <tr>
      <td><code>isFormat.dash(rut: string): boolean</code></td>
      <td>Checks if a RUT has the correct format with a dash.</td>
      <td><code>console.log(isFormat.dash('12345678-9')); // true</code></td>
    </tr>
    <tr>
      <td><code>isFormat.dotDash(rut: string): boolean</code></td>
      <td>Checks if a RUT has the correct format with dots and a dash.</td>
      <td><code>console.log(isFormat.dotDash('12.345.678-9')); // true</code></td>
    </tr>
  </tbody>
</table>

## Contributing
If you wish to contribute to this project, please open an issue or submit a pull request.

## Star History

<a href="https://star-history.com/#wotanCode/RUTility&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=wotanCode/RUTility&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=wotanCode/RUTility&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=wotanCode/RUTility&type=Date" />
 </picture>
</a>

### Main Developer
[![Contribuidores](https://contrib.rocks/image?repo=wotanCode/RUTility&max=500&columns=20)](https://github.com/wotanCode/RUTility/graphs/contributors)

## License
This project is licensed under the MIT License.
