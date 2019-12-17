---
title: "Record a Call"
weight : 55
---

Now that we have successfully implemented the basic IVR we still have the matter of the press office to attend to. No one is currently present from the press office to handle our call so we are going to need to allow for a mechanism for folks calling into our IVR to leave a message for the press office.

We're going to do that by allowing them to leave a message with the press office.

Remember from the onInput callback from the previous section - the switch for input 3. 

```js
        case "3":
            ncco =
            [
                {
                    action: 'talk',
                    text: 'You have asked to speak with the press office. Unfortunately no one from the press office is currently available and the recording service has yet to be implemented, please try back later'
                }
            ]
            response.json(ncco)
            break;
```

We are going to edit this snippet of code to actually instruct Nexmo to preform the voice recording for us. To do this, we are going to add another action. Let's modify the snippet of code above to hold this record action. 