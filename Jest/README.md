## Tips

### jestでESMを読み込めるようにする

#### Vanila
```
npm install -D jest cross-env

-- package.json --
  "scripts": {
    "test": "cross-env NODE_OPTIONS=--experimental-vm-modules jest"
  },
```

#### TypeScript

```
npm i -D jest @types/jest ts-jest

-- package.json --
  "jest": {
    "globals": {
      "ts-jest": {
        "useESM": true
      }
    },
    "preset": "ts-jest/presets/default-esm"
  },
```