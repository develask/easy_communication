## Easy Communication

It is a simmple module to create communication between diferent processes.

#### A Server sample:

```python
import easy_communication
s = easy_communication.Server()

def echo(x):
	print(x)
	return "New message"

s.handler = echo
s.start()
```

#### How to send data from other proccess:

```python
import easy_communication

data = "my data"
returned_data = easy_communication.send_data(data)

assert returned_data == "New message"
```