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

## JavaScript / v8



## Python / CPython

## Python / MicroPython

## Ruby ???

## WebAssembly / ???

Fox