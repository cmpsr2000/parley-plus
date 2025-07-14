---
description: |
  Upgrading
---

This guide covers how to upgrade Parley. To use this guide properly, navigate to
the version from which you are upgrading and work your way upwards. Unless
stated otherwise, it is mandatory to follow every upgrade step from the version
your are on.

## Prerequisites

- Parley is [installed](./installation.md) and running in your Godot Editor.

## Version `1.x.x` to `2.x.x`

1. Download and [install](./installation.md) Parley `v2.x.x`.
2. Replace of extensions of `FactInterface` with `ParleyFactInterface`.
3. Within each Fact definition, rename the `execute` method to `evaluate` and
   adjust the method contract by changing the type of the `ctx` parameter with
   `ParleyContext`.
4. Within each Action definition, rename the `execute` method to `run` and
   adjust the method contract by changing the type of the `ctx` parameter with
   `ParleyContext`.
5. Replace `Parley.start_dialogue` with `Parley.run_dialogue` and ensure the
   `ctx` parameter is of type: `ParleyContext`.
6. Replace any interface of `ParleyDialogueSequenceAst.process_next` with
   `ParleyDialogueSequenceAst.next` and adjust the interface as appropriate.
