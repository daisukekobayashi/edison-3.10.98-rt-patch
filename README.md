# edison-3.10.98-rt patch

This repository contains rt-preempt patch for intel edison release 3.5.
This patch is unstable. Kernel outputs logs below on boot.

```
[  OK  ] Started Load/Save RF Kill Switch Status of rfkill3.
[  OK  ] Started Load/Save RF Kill Switch Status of rfkill4.
[  OK  ] Started Restore Sound Card State.
[  OK  ] Started User Manager for UID 0.
[   10.460205] BUG: sleeping function called from invalid context at /home/daisuke/build/poky-edison/iot-devkit-yp-poky-edison-20160606/poky/linux-kernel/kernel/rtmutex.c:1077
[   10.460213] in_atomic(): 1, irqs_disabled(): 1, pid: 300, name: hostapd
[   10.460240] Preemption disabled at:[<c12bc6ca>] __setup_irq+0x7a/0x4b0
         Starting PulseAudio Sound System...
[  OK  ] Started udhcpd daemon for hostapd.
[   10.821191] nop dwc3-device.1: failed to start (null): -120
[  OK  ] Started Wyliodrin server.
[  OK  ] Started Wyliodrin hypervisor.
[   11.659346] BUG: sleeping function called from invalid context at /home/daisuke/build/poky-edison/iot-devkit-yp-poky-edison-20160606/poky/linux-kernel/kernel/rtmutex.c:1077
[   11.659354] in_atomic(): 1, irqs_disabled(): 1, pid: 369, name: sh
[   11.659381] Preemption disabled at:[<c124a9fc>] irq_enter+0x4c/0x70
[   12.746925] BUG: sleeping function called from invalid context at /home/daisuke/build/poky-edison/iot-devkit-yp-poky-edison-20160606/poky/linux-kernel/kernel/rtmutex.c:1077
[   12.746933] in_atomic(): 1, irqs_disabled(): 1, pid: 267, name: agetty
[   12.746959] Preemption disabled at:[<c124a9fc>] irq_enter+0x4c/0x70
Poky (Yocto Project Reference Distro) 1.7.3 edison ttyMFD2

edison login: [   13.771444] BUG: sleeping function called from invalid context at /home/daisuke/build/poky-edison/iot-devkit-yp-poky-edison-20160606/poky/linux-kernel/kernel/rtmutex.c:1077
[   13.771453] in_atomic(): 1, irqs_disabled(): 1, pid: 309, name: node
[   13.771481] Preemption disabled at:[<c124a9fc>] irq_enter+0x4c/0x70
[   14.771307] BUG: sleeping function called from invalid context at /home/daisuke/build/poky-edison/iot-devkit-yp-poky-edison-20160606/poky/linux-kernel/kernel/rtmutex.c:1077
[   14.771316] in_atomic(): 1, irqs_disabled(): 1, pid: 334, name: node
[   14.771344] Preemption disabled at:[<c124a9fc>] irq_enter+0x4c/0x70
[   15.771168] BUG: sleeping function called from invalid context at /home/daisuke/build/poky-edison/iot-devkit-yp-poky-edison-20160606/poky/linux-kernel/kernel/rtmutex.c:1077
[   15.771177] in_atomic(): 1, irqs_disabled(): 1, pid: 406, name: node
[   15.771204] Preemption disabled at:[<c124a9fc>] irq_enter+0x4c/0x70
[   16.771032] BUG: sleeping function called from invalid context at /home/daisuke/build/poky-edison/iot-devkit-yp-poky-edison-20160606/poky/linux-kernel/kernel/rtmutex.c:1077
[   16.771041] in_atomic(): 1, irqs_disabled(): 1, pid: 435, name: configure_ediso
[   16.771069] Preemption disabled at:[<c124a9fc>] irq_enter+0x4c/0x70
[   17.770894] BUG: sleeping function called from invalid context at /home/daisuke/build/poky-edison/iot-devkit-yp-poky-edison-20160606/poky/linux-kernel/kernel/rtmutex.c:1077
[   17.770903] in_atomic(): 1, irqs_disabled(): 1, pid: 469, name: node
[   17.770931] Preemption disabled at:[<c124a9fc>] irq_enter+0x4c/0x70
[   18.770847] BUG: sleeping function called from invalid context at /home/daisuke/build/poky-edison/iot-devkit-yp-poky-edison-20160606/poky/linux-kernel/kernel/rtmutex.c:1077
[   18.770855] in_atomic(): 1, irqs_disabled(): 1, pid: 0, name: swapper/0
[   18.770880] Preemption disabled at:[<c18fec21>] schedule_preempt_disabled+0x21/0x30

Poky (Yocto Project Reference Distro) 1.7.3 edison ttyMFD2

edison login:
```
