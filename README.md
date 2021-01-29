# SimMotor
A version of the EPICS Motor Record with all the non-simulated motor stuff removed.

Requires EPICS base and asyn.

To build:

* Edit configure/RELEASE so it points at the correct location for EPICS base and asyn
* Run make

To run:
```
cd iocBoot/iocSim
../../bin/darwin-x86/WithAsyn  st.cmd.unix
```
