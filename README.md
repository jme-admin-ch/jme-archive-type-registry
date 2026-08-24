# JME Archive Type Registry 

## Overview

The Archive Type Registry is a structured Git repository for managing archive data schemas that must remain unchanged after publication so archived data stays readable over time.
Archive types are maintained per system and uniquely identified by system name, archive type name, and version. Avro is the recommended format because Java bindings can be generated from it and the Process Archive Service can validate data against the schema before storing it. The registry is checked during the Maven build and can publish Java bindings for the defined archive type versions.

## Structure

Schemas live under `archive-types/<system>/<archive-type>/`, one folder per archive type, each containing one
`.avdl` file per published version plus a `.json` descriptor (`Archive Type Registry Maven Plugin` output). This
registry defines the archive types for the `jme` system used by the JME examples:

- `decree` — versioned across `Decree_v1.avdl`, `Decree_v2.avdl` and `Decree_v3.avdl`, showing how an archive
  type's schema evolves across versions while old versions remain readable.
- `decreesummary` and `decreedocument` — related archive types referencing shared definitions.
- `diagram` — an example of a simpler, single-version archive type.

`archive-types/jme/_common/` holds Avro definitions shared across the archive types above (e.g. `DecreeReference`).

## Note

This repository is part of the open source distribution of jEAP. See [github.com/jeap-admin-ch/jeap](https://github.com/jeap-admin-ch/jeap)
for more information.

## License

This repository is Open Source Software licensed under the [Apache License 2.0](./LICENSE).
