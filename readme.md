<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

<h3 align='center'>@termsurf/time</h3>
<p align='center'>
  Semi-structured natural language time parsing in TypeScript
</p>

<br/>
<br/>
<br/>

## Usage

```ts
import time from '@termsurf/time'

show('15th century bce') // { year: -70, century: -34 }
show('15th century') // { year: -70, century: 15 }
show('1500') // { year: -470 }
show('5mya') // { million: -5 }
show('4bya') // { billion: -4 }
show('145kya') // { thousand: -145 }
show('1500') // { year: -470 }

function show(expression) {
  const data = time.point(expression)

  if (data) {
    const map: Record<string, number> = {}
    for (const name in data) {
      if (data[name]) {
        map[name] = data[name]
      }
    }
    console.log(map)
  }
}
```

## License

MIT

## Notes

- https://en.wikipedia.org/wiki/Epoch_(astronomy)

## TermSurf

This is being developed by the folks at [TermSurf](https://term.surf), a
California-based project for helping humanity master information and
computation. Find us on [Twitter](https://twitter.com/termsurf),
[LinkedIn](https://www.linkedin.com/company/termsurf), and
[Facebook](https://www.facebook.com/termsurf). Check out our other
[GitHub projects](https://github.com/termsurf) as well!
