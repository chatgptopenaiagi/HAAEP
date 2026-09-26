# Packs

Status: **CONCEPT catalog boundary; no packs or installation mechanism**.

A pack groups coherent technology-specific engines, adapters, providers, tools,
and human surfaces. A future Java pack could group JDK/JVM inspection, compiler
and build-system adapters, task requirements, and an environment playground.

See [ENGINE_PACKS](../docs/ENGINE_PACKS.md) for composition, compatibility, and
trust boundaries. Different installations may choose different packs. Installing
or discovering a pack must not imply permission to execute its capabilities.

Future catalog entries should name purpose, included capabilities, dependencies,
contract compatibility, declared permissions, provenance, supported/tested
environments, playground coverage, limitations, and status. This directory is not
a marketplace, plugin loader, package registry, or authorization mechanism.
