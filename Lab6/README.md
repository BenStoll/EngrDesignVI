# Lab 6
## Node.js

![image](https://user-images.githubusercontent.com/98097869/236324096-39bddfac-e2f9-46ae-8027-79e4d7122752.png)

![image](https://user-images.githubusercontent.com/98097869/236324558-170a741a-c5a7-44b1-a703-0f0f896ee627.png)

![image](https://user-images.githubusercontent.com/98097869/236325226-9fba81b8-a7d5-4a55-98ef-8f9036fdb62f.png)

```
PS C:\Users\stoll\iot\lesson6> node http.js
0

1
2
3
4
5
6
7
```

## Pystache
```
PS C:\Users\stoll\iot\lesson6> cat say_hello.mustache
Hello, {{to}}!


PS C:\Users\stoll\iot\lesson6> cat say_hello.py
# https://github.com/defunkt/pystache
import pystache
print(pystache.render('Hi {{person}}!', {'person': 'Alexa'}))

# Create dedicated view classes to hold view logic
class SayHello(object):
    def to(self):
        return "World"
hello = SayHello()

# Use template in say_hello.mustache
renderer = pystache.Renderer()
print(renderer.render(hello))

# Pre-parse a template
parsed = pystache.parse('Hey {{#who}}{{.}}!{{/who}}')
print(parsed)
print(renderer.render(parsed, {'who': 'Google'}))
print(renderer.render(parsed, {'who': 'Siri'}))


PS C:\Users\stoll\iot\lesson6> python say_hello.py
Hi Alexa!
Hello, World!

['Hey ', _SectionNode(key='who', index_begin=12, index_end=18, parsed=[_EscapeNode(key='.'), '!'])]
Hey Google!
Hey Siri!
```
#### I had an issue woth calling python3 directly, however it worked when I simply called python.
