# SimMotor

Requires EPICS base, Asyn and Sncseq.

The build process is a bit weird...

```
> make
> cd modules/motorMotorSim/iocs/motorSimIOC/iocBoot/iocMotorSim
> EPICS_HOST_ARCH=darwin-aarch64 make
```
Replace the above `EPICS_HOST_ARCH` as required

Need to manually fix `TOP` in `envPaths`:
```
change from:
  epicsEnvSet("TOP","<path to top directory>/modules/motorMotorSim/iocs/motorSimIOC")

to:
  epicsEnvSet("TOP","<path to top directory>/modules/motorMotorSim")
```

Start the IOC like so:
```
> cd modules/motorMotorSim/iocs/motorSimIOC/iocBoot/iocMotorSim
> ../../../../bin/darwin-aarch64/motorSim st.cmd
```
