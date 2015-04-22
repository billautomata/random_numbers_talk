

###[`demonstration of the project`](http://billautomata.github.io/random_numbers_talk/)


This is a continuation of my [PI Day project](https://github.com/billautomata/piday_2015).

# scope mode

In this mode I take a stream of random numbers

`[32, 4, 1, 3, 4, 127, 244, 0, 134, ...]`

...and treat them as a series of X/Y coordinates.

`[ x, y, x, y, x, y, x, y, ...]`

I can source the stream of random numbers from anywhere.

`[ Math.random(), Math.random(), Math.random(), ...]`

Or the pixel values of an image.

`[ r, g, b, r, g, b, r, g, b, ...]`

Or the raw bytes from a file, encoded in the format (zip file, binary files)

I normalize the values from the input stream to `[-1 to 1]`.




# particle mode

In this mode I take that normalized stream and make the source of randomness for a particle system.

```
function tick(){

  for each particle {

    particle.velocity.x += random_number[index]
    particle.velocity.y += random_number[index+1]
    index+=2

    particle.position += particle.velocity

  }
}
```



# why do this?
