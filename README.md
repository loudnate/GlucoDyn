# GlucoDyn
GlucoDyn was created to educate T1D's and their caregivers about blood sugar dynamics.

For more information, please visit the original repo at [Perceptus/GlucoDyn](https://github.com/Perceptus/GlucoDyn)

## Reporter fork
This is an automated, display-only version of GlucoDyn, preserving its algorithm and chart display implementations but removing the manual input logic.

The remaining Javascript interface is currently as follows:

```javascript
// Set settings
localStorage["userdata"] = JSON.stringify({
	cratio: userdata.cratio,  // g/U
	sensf: userdata.sensf,  // (mg/dL)/U
	idur: userdata.idur,  // hours
	bginitial: userdata.bginitial,  // mg/dL
	stats: userdata.stats,  // 1 or 0
	simlength: userdata.simlength,  // hours
	inputeffect: userdata.inputeffect  // 1 or 0
})

// Add temp basal
uevent[uevent.length] = {
	etype: "tempbasal",
	id: uevent_counter++,
	time: 0
	t1: 0,
	t2: 90,
	dbdt: 1,
}
addEventHistory()

// Add bolus
uevent[uevent.length] = {
	id: uevent_counter++,
	etype: "bolus",
	time: 0,
	units: 3.2
}
addEventHistory()

// Add carb
uevent[uevent.length] = {
	id: uevent_counter++,
	etype: "carb",
	time: 0,
	grams: 17
}
addEventHistory()

// Reload graph data
reloadGraphData()
```

# License
### The MIT License (MIT)

		The MIT License (MIT)

		Copyright (c) 2015 Perceptus.org

		Permission is hereby granted, free of charge, to any person obtaining a copy
		of this software and associated documentation files (the "Software"), to deal
		in the Software without restriction, including without limitation the rights
		to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
		copies of the Software, and to permit persons to whom the Software is
		furnished to do so, subject to the following conditions:

		The above copyright notice and this permission notice shall be included in all
		copies or substantial portions of the Software.

		THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
		IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
		FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
		AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
		LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
		OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
		SOFTWARE.
