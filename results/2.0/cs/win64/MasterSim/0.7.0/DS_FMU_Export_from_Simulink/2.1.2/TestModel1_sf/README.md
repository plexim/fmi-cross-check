# Validation of 'TestModel1_sf'

## Variables
Weighted-root-mean-square norm with RelTol = 1e-3 and AbsTol = 1e-3, where
AbsTol is based on max. magnitude of reference values.

```
WRMS(Noise) = 240.07037443135
WRMS(Noise_Filt) = 63.63472896386721
WRMS(Noise_Filt_Sat) = 135.268983507227
WRMS(Sine) = 0.3482045670742671
WRMS(Sine_Filt) = 0.42071296139057535
WRMS(Sine_Filt_Quantized) = 13.976101562712916
```

## MasterSim project file

Below is the project file that was used to successfully simulation the test case.
Mind: project file is copied from working directory, hence relative path to fmu file.

```

tStart                   0.000000 s
tEnd                     10.000000 s
hMax                     30 min
hMin                     1e-6 s
hFallBackLimit           0.001 s
hStart                   0.001000 s
hOutputMin               0.100000 s
adjustStepSize           no
absTol                   1e-6
relTol                   0.001000
MasterMode               GAUSS_JACOBI
ErrorControlMode         NONE
maxIterations            1
writeInternalVariables   yes

simulator 0 0 slave1 #ffff8c00 "..\..\fmi-cross-check\fmus\2.0\cs\win64\DS_FMU_Export_from_Simulink\2.1.2\TestModel1_sf\TestModel1_sf.fmu"


```

