# SimMotor

Requires EPICS base, Asyn and Sncseq.

The build process is a bit weird...

```
> make
> cd modules/motorMotorSim/iocs/motorSimIOC/iocBoot/iocMotorSim
> EPICS_HOST_ARCH=darwin-aarch64 make
```
Replace the above `EPICS_HOST_ARCH` as required

Need to manual fix `TOP` in `envPaths`:
```
change from:
  epicsEnvSet("TOP","<path to top directory>/modules/motorMotorSim/iocs/motorSimIOC")

to:
  epicsEnvSet("TOP","<path to top directory>")
```

Start the IOC like so:
```
> cd /modules/motorMotorSim/iocs/motorSimIOC
> 
```
