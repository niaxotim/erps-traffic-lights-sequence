### @activities true
### @explicitHints true

# ERPS STEM WEEK :: Traffic Lights - Sequence Tutorial

## Introduction
### Introduction Step @unplugged
Hopefully you've got your lights working! But traffic lights have a particular sequence...
On a piece of paper, can you write down the steps that a traffic light goes through, and
in which order the lights come on? Once you are done, come back and click OK to get to the next step.
![Have a think](https://raw.githubusercontent.com/niaxotim/erps-traffic-lights-sequence/master/assets/think.png)

### Sequence Step @unplugged
Did you figure out the sequence? There are four 'stages': "Stop", "Get ready", "Go" and "Prepare to stop".
![Have a think](https://raw.githubusercontent.com/niaxotim/erps-traffic-lights-sequence/master/assets/sequence.png)

## Traffic Lights Sequence
### Step 1
To get the traffic light sequence to continuously repeat, our code will be using the ``||basic:forever||`` block.  

#### ~ tutorialhint
```blocks
basic.forever(function () {
})
```

### Step 2
Hopefully from your written down traffic light sequence, there should be four stages: "Stop", "Get ready", "Go" and "Prepare to stop". Let's code the first of these.  
Add three ``||Kitronik_STOPbit.Turn Traffic Light On||`` blocks, making sure each block has a different colour selected. In this stage, only the "Red" light is turned on, the others are turned "off"

#### ~ tutorialhint
```blocks
basic.forever(function () {
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Red, Kitronik_STOPbit.DisplayLights.On)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Yellow, Kitronik_STOPbit.DisplayLights.Off)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Green, Kitronik_STOPbit.DisplayLights.Off)
})
```

### Step 3
Between each stage of the traffic light sequence there should be a pause. Add a ``||basic:pause||`` to the end of the code. Set the time for 1 second (1000 milliseconds).

#### ~ tutorialhint
```blocks
basic.forever(function () {
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Red, Kitronik_STOPbit.DisplayLights.On)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Yellow, Kitronik_STOPbit.DisplayLights.Off)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Green, Kitronik_STOPbit.DisplayLights.Off)
    basic.pause(1000)
})
```

### Step 4
The next stage of the sequence is "Get ready", which has "Red" and "Yellow" turned on and "Green" off. Add three ``||Kitronik_STOPbit.Turn Traffic Light On||`` blocks below the current code. Don't forget the pause at the end.

#### ~ tutorialhint
```blocks
basic.forever(function () {
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Red, Kitronik_STOPbit.DisplayLights.On)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Yellow, Kitronik_STOPbit.DisplayLights.Off)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Green, Kitronik_STOPbit.DisplayLights.Off)
    basic.pause(1000)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Red, Kitronik_STOPbit.DisplayLights.On)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Yellow, Kitronik_STOPbit.DisplayLights.On)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Green, Kitronik_STOPbit.DisplayLights.Off)
    basic.pause(1000)
})
```

### Step 5
Time to Go! Add another three ``||Kitronik_STOPbit.Turn Traffic Light On||`` blocks and set only the "Green" LED on. Remember the ``||basic:pause||`` block.

#### ~ tutorialhint
```blocks
basic.forever(function () {
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Red, Kitronik_STOPbit.DisplayLights.On)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Yellow, Kitronik_STOPbit.DisplayLights.Off)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Green, Kitronik_STOPbit.DisplayLights.Off)
    basic.pause(1000)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Red, Kitronik_STOPbit.DisplayLights.On)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Yellow, Kitronik_STOPbit.DisplayLights.On)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Green, Kitronik_STOPbit.DisplayLights.Off)
    basic.pause(1000)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Red, Kitronik_STOPbit.DisplayLights.Off)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Yellow, Kitronik_STOPbit.DisplayLights.Off)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Green, Kitronik_STOPbit.DisplayLights.On)
    basic.pause(1000)
})
```

### Step 6
Now we need to place the final traffic light sequence in to prepare the traffic to stop. Add another three ``||Kitronik_STOPbit.Turn Traffic Light On||`` blocks and a ``||basic.pause||``. Set only the "Yellow" LED on.
#### ~ tutorialhint
```blocks
basic.forever(function () {
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Red, Kitronik_STOPbit.DisplayLights.On)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Yellow, Kitronik_STOPbit.DisplayLights.Off)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Green, Kitronik_STOPbit.DisplayLights.Off)
    basic.pause(1000)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Red, Kitronik_STOPbit.DisplayLights.On)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Yellow, Kitronik_STOPbit.DisplayLights.On)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Green, Kitronik_STOPbit.DisplayLights.Off)
    basic.pause(1000)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Red, Kitronik_STOPbit.DisplayLights.Off)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Yellow, Kitronik_STOPbit.DisplayLights.Off)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Green, Kitronik_STOPbit.DisplayLights.On)
    basic.pause(1000)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Red, Kitronik_STOPbit.DisplayLights.Off)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Yellow, Kitronik_STOPbit.DisplayLights.On)
    Kitronik_STOPbit.trafficLightLED(Kitronik_STOPbit.LightColours.Green, Kitronik_STOPbit.DisplayLights.Off)
    basic.pause(1000)
})
```

### Step 7
Connect your BBC micro:bit and click ``|Download|``. Once programmed, power the BBC micro:bit and check if the traffic light sequence is correct.