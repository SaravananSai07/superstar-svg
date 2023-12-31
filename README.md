# Rajnikanth's Silhouette SVG


![Rajnikanth](/superstar.svg)


### Context
Recently, I was looking for a SVG icon which I couldn't find with some of the icon providers. I tried prompting ChatGPT to come up with the SVG code, I got the SVG code which was, well, close to 1% of what I asked for. And, a whileback I watched a [100 seconds](https://www.youtube.com/playlist?list=PL0vfts4VzfNiI1BsIK5u7LpPaIDKMJIDN) video from [Jeff Delaney](https://fireship.io/contributors/jeff-delaney/#:~:text=Jeff%20Delaney%20is%20a%20Google,the%20creator%20of%20fireship.io.) on [SVGs](https://youtu.be/emFMHH2Bfvo?si=DsM7Lo-clZS9W4Zq) and thought of giving it a try back then and it remained a thought till the time came.


> *404: Part where SVG is explained with its advantages over some other formats.*
*But if you have the time and will, then [go ahead](https://developer.mozilla.org/en-US/docs/Web/SVG).*


### Shapes
SVG provides some [basic shapes](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Basic_Shapes) like `circle`, `rectangle`, `eclipse` and `polygon`. While it comes to complex shapes we'll take [path](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Paths)'s help. It is possible to compose any possible shape with just `path`. 


### Designing Rajnikanth
While I was reading about SVG, I wanted to give it a try with something *not regular* to test it out and was thinking of designing a human standing and wanted it to be a silhouette to get away with not working on the details. Started thinking of making a silhouette of a recognizable figure and Rajnikanth's silhouette is one that is easily recognizable and strongly registered (for Tamilians at least).

> Disclaimer: Kindly bear with my (lack of) artistic skills.

#### Commands
I designed it with the use of `path` which has a few [line commands](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Paths#line_commands) like *Move to* `M x y` and *Line to* `L x y` and a few [curve commands](https://developer.mozilla.org/en-US/docs/Web/SVG/Tutorial/Paths#curve_commands) like *Bezier Curves* `C x1 y1, x2 y2, x y` and *Arcs* `A rx ry x-axis-rotation large-arc-flag sweep-flag x y`. 
In this case, I've used *Move to*, *Line to* and *Arcs* to complete the design.

#### [Code](/superstar.svg)

* In a ~75 x 100 space, I've started with bottom left with `M20 99.5` and ended up almost at that point with `L19.5 99.5` command.
* If there are multiple `path` or other shape elements which has a similar styling properties like `fill`, `stroke` and `stroke-width`,  `<g>` tag can be used to group them.
```
    <g fill="black" stroke="black" stroke-width="1">
        <path d="M20 90 ...">
        <circle cx="50" cy="50" r="10">
    </g>
```
