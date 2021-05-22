# SheetSQL

## This is just forked version of original package [sheetsql](https://github.com/joway/sheetsql/) but supports reading info from env variable instead of json file. In most of the case the original one is more than enough.



## Usage

```ts
import Database from 'sheetsql-v2';

export const db = new Database({
  db: process.env.SPREADSHEET_ID, // sheet id
  table: process.env.SPREADSHEET_NAME, // sheet name, default = Sheet1
  cacheTimeoutMs: 5000, // optional, default = 5000
  clientEmail: process.env.GOOGLE_SHEETS_CLIENT_EMAIL,
  privateKey: (process.env.GOOGLE_SHEETS_PRIVATE_KEY || '').replace(
    /\\n/g,
    '\n'
  ),
});
```


Docs [same as original package](https://github.com/joway/sheetsql#sheetsql)