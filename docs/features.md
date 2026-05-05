# Feature Roadmap

This document captures product directions that are outside the current CLI
surface but align with Disk Space Manager's Unix-like disk maintenance goals.

## Cloud Archive Targets

Future archive destinations may include object storage such as AWS S3 and
Google Cloud Storage. This should include restore workflows, not just upload,
so users can recover archived files while preserving the original directory
structure.

## Backup Restore

Archive metadata could support listing, verifying, and restoring archived
content from local drives or cloud targets. Restore behavior should preserve
the current safety model with dry-run previews, confirmation, and action
logging.

## Secret Handling

Cloud-backed workflows will need careful credential handling. Prefer standard
platform secret stores or cloud-provider credential helpers over storing
secrets directly in project config files.

## Platform Generalization

The project should stay framed as a Unix-like disk maintenance tool for macOS
and Linux. Documentation and CLI wording should avoid Mac-only language unless
describing a specifically macOS implementation detail such as `diskutil`.
