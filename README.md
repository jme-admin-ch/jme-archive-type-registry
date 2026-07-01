# JME Archive Type Registry 

## Overview

The Archive Type Registry is a structured Git repository for managing archive data schemas that must remain unchanged after publication so archived data stays readable over time.
Archive types are maintained per system and uniquely identified by system name, archive type name, and version. Avro is the recommended format because Java bindings can be generated from it and the Process Archive Service can validate data against the schema before storing it. The registry is checked during the Maven build and can publish Java bindings for the defined archive type versions.

## Note

This repository is part of the open source distribution of jEAP. See [github.com/jeap-admin-ch/jeap](https://github.com/jeap-admin-ch/jeap)
for more information.

## License

This repository is Open Source Software licensed under the [Apache License 2.0](./LICENSE).
