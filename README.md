# asyncio-hello-world
an asyncio hello-world demo using an event loop

``` python
import asyncio


async def hello(name, sleepfor):
    print(f'hi {name} I"m giving you {sleepfor} seconds to answer me.')
    await asyncio.sleep(sleepfor)
    print(f'hello world, {name} here, I took all the time you gave me.. so, what do you want?')


loop = asyncio.get_event_loop()
loop.create_task(hello("Billy Bob", 3))
loop.create_task(hello("Billy Alice", 1))

loop.run_forever()
loop.close()

```

- created and tested on python 3.7
