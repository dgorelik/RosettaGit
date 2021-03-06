+++
title = "Viua VM assembly"
description = ""
date = 2017-06-15T15:38:58Z
aliases = []
[extra]
id = 21383
[taxonomies]
categories = []
tags = []
+++

{{stub}}

{{language|Viua VM assembly
|site=http://viuavm.org/
|exec=bytecode
|safety=safe
|strength=strong
|checking=dynamic
|parampass=both
|gc=allowed
|express=implicit
|LCT=yes
}}
{{Language programming paradigm|Concurrent}}
{{Language programming paradigm|Imperative}}

Viua VM assembly is the language that is used to program Viua virtual machine.

Programs in written in Viua VM assembly are composed of isolated, lightweight processes running in parallel and communicating via message passing (compare with [[Erlang]]).
Inside every process programs are executed sequentially.

The programming arsenal provided by Viua VM assembly language includes first-class functions, move- and copy-semantics for value movement (inside a single call frame, and for parameter passing), exceptions, deferred calls, safe pointers, and more.

Documentation can be found at http://docs.viuavm.org/
