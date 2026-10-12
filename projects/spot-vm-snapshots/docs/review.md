# Consolidation review

Imported from [source commit](https://github.com/LabsByNateJ/spotvm-snapshot-automation/commit/31cdd788f8164d7916e1cb435e15e5cb8f6bf885). Original code history remains in the source repository; it has not been imported into AFYCloud history. No Azure deployment was run.

## Changes during consolidation

- Corrected README deployment path to Bicep/main.bicep.
- Kept runtime code unchanged for review.
- Replaced tracked local.settings.json with local.settings.example.json. The source file contained emulator settings, not production credentials.
- Added ignore rules for local settings, environment files, virtual environments, and Python cache.

## Findings requiring validation

- function_app.py initializes a Python v2 FunctionApp without a trigger, while SpotSnapshotFunction uses the v1 directory/binding layout. Select and validate one programming model.
- Bicep supplies a Blob endpoint as AzureWebJobsStorage. Review supported host-storage configuration before deployment.
- Managed identity receives resource-group Contributor. Replace with permissions scoped to actual snapshot operations where feasible.
- Snapshot operations are started without waiting for completion; the final log does not confirm success.
- Code snapshots Spot VM OS disks only; data disks are not included.
- Retention and failure handling are not implemented.
- Runtime version, dependency versions, and hosting configuration need current compatibility checks.

Track remediation and testing in [AFYCloud issue #8](https://github.com/LabsByNateJ/AFYCloud/issues/8). Do not interpret this imported project as a validated backup solution.
