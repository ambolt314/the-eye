# The Eye
A platform that takes in a question and returns with a true/false answer to that question, along with the data it fetched to derive the answer. [Based on my play 'Crichton'](https://drive.google.com/file/d/1uGDA0linrNsyccggprEWJD8B9hmOMt2c/)

This combines my passions for Data Science and theatre. I welcome any contributors.

# Architecture

HLSD:
- User interface: input, output 
- Inference engine 
- Data parser 
- Data sockets


Sample output:
```
{ 
“query_id”: 01da3476 
“query_body”: { 
“inferred_question”: “Will it rain tomorrow?”, 
“inferred_answer”: true, 
“inference_data”: { 
“key_words”: [“rain”, “tomorrow”], 
“local_area”: “Mantua”, 
“radius”: 10, 
“forecast”: [[0600, sunny], [0700, cloudy], [0800, rain], 
“forecast_source”: “Italian Meteorological Office” 
} 
} 
} 
```

# Quotations
> You’re getting data from loads of places, aren’t you? May I take a look? 

> Oh, it works for unstructured things too?

> This is an inference that I have made from a series of black box tests. So it may not be accurate. And if I may start with the part that you all see. The central function is to indicate a Boolean value. That is the truth which the acolytes control. The Creators have made The Eye, hopefully how this diagram shows, to give the truth via the answer to a true/false question. But how does it get that answer? If my assumptions are correct, from a series of sockets with a common interface, a scalable architecture of course. These sockets pick up data from whatever source they’re programmed to, such as camera footage, ticketing systemsor weather information. Anything you can think of. It appears that we are dealing with a form of general intelligence, as it knows what data to fetch and parse without any user input. The existence of an “inferred” keyword in the JSON implies that there is some sort of machine-learned inference going on behind the scenes. The Creators of The Eye are very wise, so they would most likely have separated it out into separate modules. Which is what I’ve done here: the raw, unstructured data is parsed into a readable format and then, I speculate, converted into a simple HTTP request. I have the raw data here. You can gauge a surprising amount from it. I guess that this was for debugging
