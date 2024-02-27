# Typescript 規範
## 檔案結構
請參考Google標準之 [3. Source file structures](https://google.github.io/styleguide/tsguide.html#source-file-structure)
## 物件
1. 請使用 物件.成員 而非 物件[\"成員"]
2. 非必要請勿使用any，若未知請使用unknown或generics
## 命名規則
### Casing
1. Type名稱請使用PascalCase
2. 物件和函式名稱請使用camelCase
### Schema
1. ts型態請使用 {操作}+{名稱}+{請求|回覆}。例如：GetPaymentDataReq
2. zod type 請使用{z}+{ts型態}。例如：zGetPaymentDataReq
3. 宣告 zod type 時，請使用 `z.ZodSchema<\ts型態>` 型態。例如：
```ts
const zGetStuffReq: z.ZodSchema<GetStuffReq> = {
    id: string,
    stuff: string
}
```
