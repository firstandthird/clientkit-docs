# Transitions

Transitions use all custom cubic bezier functions. All transition variables are namespaced under `stylesheets.easing` which means they can be accessed within a yaml or configuration file as such: `'{{ stylesheets.easing.<name of equation> }}'`, where `<name of equation>` is one of the equations listed below.

## Variables

* `var(--easing-out)`: **cubic-bezier(0.35, 0.97, 0.57, 0.99)**
* `var(--easing-in-out)`: **ease-in-out**

### Default Equations

* `var(--easing-linear)`: **cubic-bezier(0.250, 0.250, 0.750, 0.750)**
* `var(--easing-ease)`: **cubic-bezier(0.250, 0.100, 0.250, 1.000)**
* `var(--easing-ease-in)`: **cubic-bezier(0.420, 0.000, 1.000, 1.000)**
* `var(--easing-ease-out)`: **cubic-bezier(0.000, 0.000, 0.580, 1.000)**
* `var(--easing-ease-in-out)`: **cubic-bezier(0.420, 0.000, 0.580, 1.000)**

### EaseIn Equations

* `var(--easing-ease-in-quad)`: **cubic-bezier(0.550, 0.085, 0.680, 0.530)**
* `var(--easing-ease-in-cubic)`: **cubic-bezier(0.550, 0.055, 0.675, 0.190)**
* `var(--easing-ease-in-quart)`: **cubic-bezier(0.895, 0.030, 0.685, 0.220)**
* `var(--easing-ease-in-quint)`: **cubic-bezier(0.755, 0.050, 0.855, 0.060)**
* `var(--easing-ease-in-sine)`: **cubic-bezier(0.470, 0.000, 0.745, 0.715)**
* `var(--easing-ease-in-expo)`: **cubic-bezier(0.950, 0.050, 0.795, 0.035)**
* `var(--easing-ease-in-circ)`: **cubic-bezier(0.600, 0.040, 0.980, 0.335)**
* `var(--easing-ease-in-back)`: **cubic-bezier(0.600, -0.280, 0.735, 0.045)**

### EaseOut Equations

* `var(--easing-ease-out-quad)`: **cubic-bezier(0.250, 0.460, 0.450, 0.940)**
* `var(--easing-ease-out-cubic)`: **cubic-bezier(0.215, 0.610, 0.355, 1.000)**
* `var(--easing-ease-out-quart)`: **cubic-bezier(0.165, 0.840, 0.440, 1.000)**
* `var(--easing-ease-out-quint)`: **cubic-bezier(0.230, 1.000, 0.320, 1.000)**
* `var(--easing-ease-out-sine)`: **cubic-bezier(0.390, 0.575, 0.565, 1.000)**
* `var(--easing-ease-out-expo)`: **cubic-bezier(0.190, 1.000, 0.220, 1.000)**
* `var(--easing-ease-out-circ)`: **cubic-bezier(0.075, 0.820, 0.165, 1.000)**
* `var(--easing-ease-out-back)`: **cubic-bezier(0.175, 0.885, 0.320, 1.275)**

### EaseInOut Equations

* `var(--easing-ease-in-out-quad)`: **cubic-bezier(0.455, 0.030, 0.515, 0.955)**
* `var(--easing-ease-in-out-cubic)`: **cubic-bezier(0.645, 0.045, 0.355, 1.000)**
* `var(--easing-ease-in-out-quart)`: **cubic-bezier(0.770, 0.000, 0.175, 1.000)**
* `var(--easing-ease-in-out-quint)`: **cubic-bezier(0.860, 0.000, 0.070, 1.000)**
* `var(--easing-ease-in-out-sine)`: **cubic-bezier(0.445, 0.050, 0.550, 0.950)**
* `var(--easing-ease-in-out-expo)`: **cubic-bezier(1.000, 0.000, 0.000, 1.000)**

## Mixins

None

## Helpers

None
