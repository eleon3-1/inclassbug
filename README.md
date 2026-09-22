My app uses StatefulWidget and setState() whenever something on the screen needs to change. _TactileDeckAppState keeps track of dark mode because the theme affects the whole app. It sends the current theme and a function to ControlDeckScreen so that screen can switch the theme.

_ControlDeckScreenState keeps track of the total taps, power level, and system status. When I tap a button, _triggerAction() updates the tap count and status. When I move the slider, setState() updates the power level, so the slider and energy percentage match.

Each tactile button keeps track of whether it is pressed. That way, pressing one button does not make the others look pressed. The superhero panel also keeps track of its own energy and forcefield. I put values used by multiple widgets in their parent and let each widget handle the values that only affect itself.
