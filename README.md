# 21cmEMU
An emulator of 21cmFAST summaries

## Dowloading the emulator
First clone this repository, and install it using `python setup.py install`. 
Once installed, run:
```
from emu21cmfast.emulator import EMU21cmFAST
emulator_instance = EMU21cmFAST()
```

You can now use the emulator to make predictions. For example:
```
import py21cmfast as p21
params_dict = {'F_STAR10':-0.81, 'ALPHA_STAR': 0.91, 'F_ESC10': -0.35, 
               'ALPHA_ESC': -0.27, 'M_TURN': 9.45, 't_STAR': 0.87, 
               'L_X': 38.92, 'NU_X_THRESH': 1039.87, 'X_RAY_SPEC_INDEX':2.16}
theta = p21.AstroParams(params_dict)
prediction_dict = emulator_instance.predict(astro_params = theta)
```
