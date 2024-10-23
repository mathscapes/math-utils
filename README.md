# @mathscapes/math-utils

[![Node.js Package](https://github.com/gv-sh/math-utils/actions/workflows/npm-publish.yml/badge.svg)](https://github.com/gv-sh/math-utils/actions/workflows/npm-publish.yml)

A TypeScript library for mathematical operations on scalars and vectors with JSON-LD support.

## Features

- Basic arithmetic operations for scalars and vectors
- JSON-LD support for scalar and vector representations
- TypeScript support with full type definitions
- Configurable error handling
- Modular structure for flexible imports

## Installation

To install @mathscapes/math-utils, use npm:

```bash
npm install @mathscapes/math-utils
```

## Usage

### Scalar Operations

```typescript
import { add, subtract, multiply, divide } from '@mathscapes/math-utils';
console.log(add(5, 3)); // 8
console.log(subtract(10, 4)); // 6
console.log(multiply(2, 6)); // 12
console.log(divide(15, 3)); // 5
console.log(divide(10, 0)); // null (or throws an error if strictErrorHandling is enabled)
```

### Vector Operations

```typescript
import { addVectors, subtractVectors, multiplyVectors, divideVectors } from '@mathscapes/math-utils';
const a = [1, 2, 3];
const b = [4, 5, 6];
console.log(addVectors(a, b)); // [5, 7, 9]
console.log(subtractVectors(a, b)); // [-3, -3, -3]
console.log(multiplyVectors(a, b)); // [4, 10, 18]
console.log(divideVectors(a, b)); // [0.25, 0.4, 0.5]
```

### JSON-LD Support

```typescript
import { parseScalar, toScalarJson, parseVector, toVectorJson } from '@mathscapes/math-utils';
const scalarJson = toScalarJson(42);
console.log(scalarJson); // { "@type": "Scalar", value: 42 }
console.log(parseScalar(scalarJson)); // 42
const vectorJson = toVectorJson([1, 2, 3]);
console.log(vectorJson); // { "@type": "Vector", values: [1, 2, 3] }
console.log(parseVector(vectorJson)); // [1, 2, 3]
```

## Development

To set up the project for development:

1. Clone the repository
2. Install dependencies: `npm install`
3. Build the project: `npm run build`

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the ISC License.