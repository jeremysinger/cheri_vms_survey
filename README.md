# CHERI Virtual Machines Survey

This is a list of programming language virtual machines
and runtime systems that have been ported to pure capability CHERI
platforms. For each project, we include a link and a brief
status summary. Please feel free to make pull requests to
update this survey document.

## C,C++ / BoehmGC

The Boehm-Demers-Weiser conservative garbage collector (GC)
has been ported to CheriBSD/Morello and CheriBSD/RISC-V.
At the moment, the GC only works in single-threaded mode.

Some CHERI purecap support is upstreamed at https://github.com/ivmai/BDWGC
with slightly more extensive support at https://github.com/capablevms/BDWGC

This work has been documented in a short research paper at [VEE 2022](https://dl.acm.org/doi/10.1145/3516807.3516823).

Contacts: Dejice Jacob and Jeremy Singer, University of Glasgow

## Java / OpenJDK

The OpenJDK runtime has been ported to CheriBSD/Morello, with
JIT compilation and GC enabled. This code is not yet available
as open-source, since it is still an active research project
at the University of Manchester.


## JavaScript / JSC

The JavaScriptCore runtime within Webkit was ported to purecap
CHERI as part of a [PhD research project](https://www.repository.cam.ac.uk/items/7d72d9da-bb2e-44a9-86e9-6c245479f6a2). Build instructions are  available
at https://www.cl.cam.ac.uk/research/security/ctsrd/cheri/cheri-webkit.html

This work is experimental.

## JavaScript / Microvium

The Microvium VM is a tiny JavaScript interpreter that targets
microcontroller devices. This runtime has been ported to CHERIoT-RTOS,
as described at https://cheriot.org/javascript/vm/2025/04/10/microvium-javascript.html

Contact: David Chisnall at SCI Semiconductor

## JavaScript,WebAssembly / V8

The V8 language runtime used by projects such as Chromium, NodeJS
and Electron has an initial purecap port to CheriBSD/Morello available
on [GitHub](https://github.com/ctsrd-cheri/v8). The port supports
execution of much of JavaScript found on real-world websites. It also
supports an initial port of both 32-bit and 64-bit WebAssembly (memory64).
The latest status update on the work is a talk at [CHERI Blossoms](https://cheri-alliance.org/events/speakers/domagoj-stolfa/).
The talk concludes with a demo of JavaScript inside the purecap port of
Chromium. The V8 port is still under active development and currently has
numerous limitations, such as not yet having support for pointer compression.

Contact: Domagoj Stolfa at University of Cambridge (V8), Graeme Jenkinson at Capabilities Ltd (Chromium)

## Lua / ?

No CHERI ports of Lua, to the best of our knowledge.


## Python / CPython

Work is ongoing to port the CPython runtime to purecap CHERI.
There is an experimental port with a limited feature set,
available on [github](https://github.com/CTSRD-CHERI/cpython). 

## Python / MicroPython

The MicroPython interpreter has been ported for purecap execution
on CheriBSD/Morello and CHERIoT-RTOS. The ports are slightly
out-of-date with respect to the latest platform releases.

The forked [Github repository](https://github.com/glasgowpli/micropython)
has branches for Morello and CHERIoT-RTOS, and there are write-ups in
research papers at [MPLR 2023](https://dl.acm.org/doi/10.1145/3617651.3622991) and [CC 2025](https://dl.acm.org/doi/10.1145/3708493.3712694).

Contacts: Duncan Lowther and Jeremy Singer, University of Glasgow

## Ruby / ?

No CHERI ports of Ruby, to the best of our knowledge.

## WebAssembly / WAMR

The WebAssembly Micro Runtime (WAMR) interpreter
has been modified to support pure capability execution
with some compartmentalization features on CheriBSD/Morello.
There is a
[github repository](https://github.com/Verifoxx-LTD/verifoxx-cheri-wamr). 

This work was conducted as a pilot study, in a short-term funded
research project.

Contact: VeriFoxx