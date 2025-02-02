# Main Message
Umm, I have been using your extenstion pxt-clicks for months. However, I found out a problem and I had tried to fix it. Unfortunately, my bad coding skills crashed the microbit. Can you help me to fix it?

# Email (For you to contact me)
puppy.ies.dog@gmail.com

# Problem
When I use Button A+B (Normal without any extenstion), and your pxt-clicks `onButtonSingleClicked`, it just became all add together likely because your extenstion is not capiblity with the normal one. (Not my suggest solution, solution below)

## Code (Not the code when I figured the problem, just for you to test, remember to open debug mode)
```
buttonClicks.onButtonSingleClicked(buttonClicks.AorB.A, function () {
    list.push(0)
})

buttonClicks.onButtonSingleClicked(buttonClicks.AorB.B, function () {
    list.push(1)
})

input.onButtonPressed(Button.AB, function () {
    list.push(2)
})

let list: number[] = []
list = []
```

### Notes
I used `motor` in the code when I figured out the problem.
1. `Button.A` for moving forwards (pxt-clicks)
2. `Button.B` for moving backwards (pxt-clicks)
3. `Button.AB` for stop (Normal input one)

And it will stop for a second and go randomly forwards or backwards.
I think it is mainly because the microbit is using both normal one and pxt-clicks. And the normal one (`Button.AB`) stops the motor but the pxt-clicks (`Button.A`) and pxt-clicks (`Button.B`) just do the single click one amd runs forward or backward.

### Suggest Solution
In my above text, I may haven't show a clearly question. So here I hope you will fix this bug like this (I've been fork and tried to fix the problem but as above, my bad coding skills just crushed the microbit coding page):
1. Add `Button.AB` to every code you have like held, single click, double click those ones.
2. Just add on A+B is pressed that program.
