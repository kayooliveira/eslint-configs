# ALL MY ESLINT AND PRETTIER DEPENDENCIES AND CONFIGURATIONS


## FOR REACT:
```json
{
    "@typescript-eslint/eslint-plugin":"",
    "@typescript-eslint/parser":"",
    "eslint":"",
    "eslint-config-prettier":"",
    "eslint-config-standard":"",
    "eslint-import-resolver-typescript":"",
    "eslint-plugin-import":"",
    "eslint-plugin-import-helpers":"",
    "eslint-plugin-jsx-a11y":"",
    "eslint-plugin-n":"",
    "eslint-plugin-prettier":"",
    "eslint-plugin-promise":"",
    "eslint-plugin-react":"",
    "eslint-plugin-vitest-globals":"",
    "prettier":"",
    "prettier-plugin-tailwindcss":""
}
```

## INSTALLATION

with npm: 

```bash
npm install --save-dev @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint eslint-config-prettier eslint-config-standard eslint-import-resolver-typescript eslint-plugin-import eslint-plugin-import-helpers eslint-plugin-jsx-a11y eslint-plugin-n eslint-plugin-prettier eslint-plugin-promise eslint-plugin-react eslint-plugin-vitest-globals prettier prettier-plugin-tailwindcss
```

with yarn: 

```bash
yarn add --dev @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint eslint-config-prettier eslint-config-standard eslint-import-resolver-typescript eslint-plugin-import eslint-plugin-import-helpers eslint-plugin-jsx-a11y eslint-plugin-n eslint-plugin-prettier eslint-plugin-promise eslint-plugin-react eslint-plugin-vitest-globals prettier prettier-plugin-tailwindcss
```

with pnpm: 

```bash
pnpm add --save-dev @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint eslint-config-prettier eslint-config-standard eslint-import-resolver-typescript eslint-plugin-import eslint-plugin-import-helpers eslint-plugin-jsx-a11y eslint-plugin-n eslint-plugin-prettier eslint-plugin-promise eslint-plugin-react eslint-plugin-vitest-globals prettier prettier-plugin-tailwindcss
```

## FOR NODE 
```json
{
    "@typescript-eslint/eslint-plugin":"",
    "@typescript-eslint/parser":"",
    "eslint":"",
    "eslint-config-prettier":"",
    "eslint-config-standard":"",
    "eslint-import-resolver-typescript":"",
    "eslint-plugin-import":"",
    "eslint-plugin-import-helpers":"",
    "eslint-plugin-n":"",
    "eslint-plugin-prettier":"",
    "eslint-plugin-promise":"",
    "prettier":"",
    "prettier-eslint":""
}
```

## INSTALLATION

with npm: 

```bash
npm install --save-dev @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint eslint-config-prettier eslint-config-standard eslint-import-resolver-typescript eslint-plugin-import eslint-plugin-import-helpers eslint-plugin-n eslint-plugin-prettier eslint-plugin-promise prettier prettier-eslint
```

with yarn: 

```bash
yarn add --dev @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint eslint-config-prettier eslint-config-standard eslint-import-resolver-typescript eslint-plugin-import eslint-plugin-import-helpers eslint-plugin-n eslint-plugin-prettier eslint-plugin-promise prettier prettier-eslint
```

with pnpm: 

```bash
pnpm add --save-dev @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint eslint-config-prettier eslint-config-standard eslint-import-resolver-typescript eslint-plugin-import eslint-plugin-import-helpers eslint-plugin-n eslint-plugin-prettier eslint-plugin-promise prettier prettier-eslint
```


## CONFIGURATION

### FOR REACT

```json

{
  "env": {
    "browser": true,
    "es2021": true,
    "vitest-globals/env":true
  },
  "extends": [
    "standard",
    "prettier",
    "plugin:@typescript-eslint/recommended",
    "plugin:import/warnings",
    "plugin:import/errors",
    "plugin:import/typescript",
    "eslint:recommended",
    "plugin:@next/next/recommended",
    "plugin:vitest-globals/recommended"
  ],
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaFeatures": {
      "jsx": true
    },
    "ecmaVersion": "latest",
    "sourceType": "module"
  },
  "plugins": [
    "@typescript-eslint",
    "eslint-plugin-import-helpers",
    "prettier",
    "jsx-a11y",
    "@next/eslint-plugin-next"
  ],
  "rules": {
    "prettier/prettier": "error",
    "space-before-function-paren": "off",
    "camelcase": "warn",
    "react/prop-types": "off",
    "react/react-in-jsx-scope": "off",
    "no-use-before-define": "off",
    "@typescript-eslint/no-explicit-any": "off",
    "@typescript-eslint/no-unused-vars": [
      "error",
      {
        "argsIgnorePattern": "_"
      }
    ],
    "import-helpers/order-imports": [
      "warn",
      {
        // example configuration
        "newlinesBetween": "always",
        "groups": ["module", "/^@shared/", ["parent", "sibling", "index"]],
        "alphabetize": { "order": "asc", "ignoreCase": true }
      }
    ],
    "import/prefer-default-export": "off",
    "jsx-a11y/alt-text": [
        "warn",
        {
            "elements": ["img"],
            "img": ["Image"]
        }
    ],
    "jsx-a11y/aria-props": "warn",
    "jsx-a11y/aria-proptypes": "warn",
    "jsx-a11y/aria-unsupported-elements": "warn",
    "jsx-a11y/role-has-required-aria-props": "warn",
    "jsx-a11y/role-supports-aria-props": "warn"
    
  },
  "settings": {
    "react": {
      "version": "detect"
    },
    "import/resolver": {
      "node": {
        "extensions": [".js", ".jsx", ".ts", ".tsx"]
      },
      "typescript": {
        "project": "./tsconfig.json"
      }
    }
}

```

### FOR NODE 

```json
{
    "env": {
        "es2021": true,
        "jest": true,
        "node": true
    },
    "extends": [
        "standard",
        "plugin:@typescript-eslint/recommended"
    ],
    "globals": {
        "Atomics": "readonly",
        "SharedArrayBuffer": "readonly"
    },
    "parser": "@typescript-eslint/parser",
    "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module"
    },
    "plugins": [
        "@typescript-eslint",
        "eslint-plugin-import-helpers",
        "prettier"
    ],
    "rules": {
        "camelcase": "off",
        "@typescript-eslint/camelcase": "off",
        "@typescript-eslint/explicit-function-return-type": [
            "off"
        ],
        "@typescript-eslint/explicit-module-boundary-types": [
            "warn",
            {
                "allowArgumentsExplicitlyTypedAsAny": true
            }
        ],
        "@typescript-eslint/naming-convention": [
            "error",
            {
                "custom": {
                    "match": true,
                    "regex": "^I[A-Z]"
                },
                "format": [
                    "PascalCase"
                ],
                "selector": "interface"
            }
        ],
        "@typescript-eslint/no-explicit-any": "off",
        "@typescript-eslint/no-unused-vars": [
            "error",
            {
                "argsIgnorePattern": "_"
            }
        ],
        "class-methods-use-this": "off",
        "import-helpers/order-imports": [
            "warn",
            {
                "alphabetize": {
                    "ignoreCase": true,
                    "order": "asc"
                },
                "groups": [
                    "/^@/",
                    "module",
                    [
                        "index",
                        "parent",
                        "sibling"
                    ]
                ],
                "newlinesBetween": "always"
            }
        ],
        "import/extensions": [
            "error",
            "ignorePackages",
            {
                "ts": "never"
            }
        ],
        "import/prefer-default-export": "off",
        "max-classes-per-file": 1,
        "no-console": "off",
        "no-new": "off",
        "no-prototype-builtins": "off",
        "no-restricted-syntax": "off",
        "no-underscore-dangle": "off",
        "no-useless-constructor": "off",
        "space-before-function-paren": ["error", "always"]
    },
    "settings": {
        "import/resolver": {
            "typescript": {
                "project": "./tsconfig.json"
            }
        }
    }
}

```
