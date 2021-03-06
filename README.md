# html-substring
[![Build Status](https://travis-ci.org/Tarik02/html-substring-js.svg?branch=master)](https://travis-ci.org/Tarik02/html-substring-js)

Module making safe substring of HTML source

# Doc
```ts
interface Options {
  breakWords: boolean // defaults to true
  suffix: (() => string) | string | null // defaults to null
}

/**
 * @param source Source HTML
 * @param length Visible characters (everything but HTML tags) limit
 * @param options Options object
 *
 * @returns stripped source by length characters
 */
function html_substring(
  source: string,
  length: number,
  options?: Partial<Options>,
): string
```

# Examples
```ts
// JavaScript/TypeScript

import html_substring from 'html-substring'

console.log(html_substring('<span><div>Hello</div> <p>World</p></span>', 6))
// <span><div>Hello</div> </span>
```

You can look [tests](https://github.com/Tarik02/html-substring-js/blob/master/test/test.ts) for more examples
