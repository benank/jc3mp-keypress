Simple module that adds clientside events for keypress, keyup, and keydown.

Events: KeyUp (when a key is released), KeyPress (when a key is held), KeyDown (when a key is first pressed)

Sample usage:

jcmp.ui.AddEvent('KeyUp', key => {
    let myKey = "U".charCodeAt(0);
    if (key == myKey)
    {
        // do something
    }
})

The above script would check if the player pressed the "U" key.


If you want to not check for keys when chat is active, use the following.

let can_use = true;

jcmp.ui.AddEvent('chat_input_state', s => {
  can_use = !s;
});

And then add an if statement to see if can_use is true.