# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.0] - 2024-12-24

### Added

- `Hasher` class for managing record hashing and hash chains
  - `hash_record()` - Hash individual records and link them to the chain
  - `hash_batch()` - Process multiple records as a batch with Merkle root computation
  - `compute_merkle_root()` - Compute Merkle root from a list of hashes
  - `verify_chain()` - Verify hash chain continuity and detect tampering
  - `verify_batch()` - Verify batch integrity via Merkle root comparison
  - `set_last_hash()` - Resume chains from a checkpoint
- `HashableRecord` protocol for flexible record type integration
  - Runtime checkable protocol using Python's `typing.Protocol`
  - Supports any class that implements `get_hash_content() -> bytes`
- Full type hint support with `py.typed` marker (PEP 561)
- Comprehensive test suite with 63 tests covering unit and integration scenarios

[0.1.0]: https://github.com/lokryn-llc/merkle-tree/releases/tag/v0.1.0
