![WebAssembly from the Ground Up — a hands-on book](https://wasmgroundup.com/img/og-image-large.png?1)

## WebAssembly from the Ground Up

## Learn Wasm by building a simple compiler in JavaScript.

Find out how WebAssembly works and why it's a big deal. You'll go from hand crafting bytecodes to writing a compiler for a toy programming language.

**No compiler expertise necessary.** All the code is in the book; we'll take you through it step by step.

Forget the hype — get your hands dirty and see for yourself what WebAssembly is all about.

The book includes:

-   15 chapters of technical content.
-   Git repo with complete source code.
-   Membership in our private Discord.
-   30-day money-back guarantee.


## Our approach

![Representation of WebAssembly concepts as the atomic model with binary format, validation and execution at the center and Web API, JS API, WASI and others orbiting around](https://wasmgroundup.com/assets/images/atomic-model-transparent-1d3a521a9ce42e9319741e03f919aa4a.png)

To really understand what WebAssembly is and what makes it special, you need to dive into the low-level details.

We use a hands-on approach to teach you the core of WebAssembly: the instruction set and the module format.

Since WebAssembly is primarily a compilation target, we think the best way to learn the details is by writing a compiler. (Really.)

You’ll build a compiler that compiles a simple programming language down to WebAssembly.

The focus is on WebAssembly, _not_ the finer details of parsing. The compiler is built in JavaScript, using [Ohm](https://ohmjs.org), a user-friendly parsing toolkit.

No compiler expertise is necessary; all the code you need is provided in the book. Everything proceeds step by step — in small, logical increments.


## What’s Inside?

Here’s a peek inside the book — 15 chapters of technical content, and two bonus chapters.

![](https://wasmgroundup.com/assets/images/chapter-preview-lg-3d0d7c7d0f9ac3d0b3d1409b25f71d5e.webp)

Full source code (including tests) is available for each milestone in every chapter. The code is MIT-licensed, so you’re free to use it in your own projects.

![](https://wasmgroundup.com/assets/images/code-preview-lg-3f0cd4ea851997e0a8dded99174e6ad7.webp)

## You’ll build…

The compiler for a programming language called Wafer:

```swift
extern func setPixel(x, y, r, g, b, a);

func sayHello() {
  print("Hello from Wafer!!")
}

func draw(width, height, t) {
  let y = 0;
  while y < height {
    let x = 0;
    while x < width {
      let r = t;
      let g = x;
      let b = y;
      let a = 255;
      setPixel(x, y, r, g, b, a);
      x := x + 1;
    }
    y := y + 1;
  }
  0
}
```

A wafer program that draws to a canvas:

![](https://beta.wasmgroundup.com/assets/images/animated-gradient-61a58ba510febb5560fb8120e559b8c2.webp)

A library to emit WebAssembly 1.0 modules:

```js
//...
export function section(id, contents) {
  const sizeInBytes = contents.flat(Infinity).length;
  return [id, u32(sizeInBytes), contents];
}

export function vec(elements) {
  return [u32(elements.length), elements];
}

export const SECTION_ID_TYPE = 1;

export function functype(paramTypes, resultTypes) {
  return [0x60, vec(paramTypes), vec(resultTypes)];
}
//...
```

## You’ll learn…

-   What exactly WebAssembly _is_, and what makes it unique.
-   How to instantiate a WebAssembly module in JavaScript and run its functions.
-   The binary module format, and how to hand craft a module from scratch.
-   How to create a simple compiler with [Ohm](https://ohmjs.org).
-   The instruction set: numeric instructions, memory access, control flow, etc.
-   How to interact with the outside world.
-   The WebAssembly security model: what makes it safe?

## Who should read this book?

The book is mainly targeted at experienced programmers. You don’t need to be an expert, but ideally you’ve been programming for a few years and are fluent in more than one language. For important topics that some readers might not be familiar with, we’ve included optional _deep dive_ sections to get you up to speed.

In order to understand the code, you’ll need at least intermediate knowledge of JavaScript, or a willingness to learn. We try to stick to “the good parts” and to avoid any advanced or obscure features.

You do not need any previous experience with writing a compiler! Our compiler is based on Ohm, a framework that handles the lower-level details of parsing. This lets us keep the focus on WebAssembly.

For some reason, many people believe that writing a compiler is a complex, esoteric task. But we hope to convince you that it’s really not.


## About the authors

**Mariano Guerra** [🐦](https://twitter.com/warianoguerra) [🐘](https://hachyderm.io/@marianoguerra) [🦋](https://bsky.app/profile/marianoguerra.org) [🏠](https://marianoguerra.org/)

is the co-founder of [Gloodata](https://gloodata.com/) and [Instadeq](https://instadeq.com/) data analysis and visualization products. He has a long history of language- and compiler-related side projects, including the programming languages [Efene](http://efene.org/) and [Interfix](https://github.com/marianoguerra/interfix). In the past, he worked with IBM Research and on high-performance computing at Intel. Originally from Córdoba, Argentina, he now lives in Stuttgart, Germany.

**Patrick Dubroy** [🐦](https://twitter.com/dubroy) [🐘](https://hachyderm.io/@dubroy) [🦋](https://bsky.app/profile/dubroy.com) [🏠](https://dubroy.com/blog/)

is a programmer and independent researcher based in Munich, Germany. He’s a co-creator and the primary maintainer of [Ohm](https://ohmjs.org), a user-friendly parsing toolkit for JavaScript. At the beginning of his career, he spent four years working on the J9 Java VM at IBM. Since then, he’s worked at companies like Google (on Chrome and Android), Lyft, and Sourcegraph.
