# CycloneDX Property Taxonomy

This is the official Finite State CycloneDX property namespace and name taxonomy. It documents all custom key/value `properties` that may be added to components in CycloneDX SBOMs created using the Finite State software.

For more information about CycloneDX property taxonomies, refer to the [official documentation](https://github.com/CycloneDX/cyclonedx-property-taxonomy).

## `finitestate` Namespace Taxonomy

| Namespace              | Description                                                                                                             |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `finitestate:metadata` | Namespace for all Finite State-specific properties dealing with top-level metadata values about products and firmwares. |
| `finitestate:sbom`     | Namespace for all Finite State-specific properties dealing with SBOM values.                                            |
| `finitestate:finding`  | Namespace for all Finite State-specific properties dealing with 'Finding' / vulnerability values.                       |

## `finitestate:metadata` Namespace Taxonomy

| Property Name                              | Description                                                                              |
| ------------------------------------------ | ---------------------------------------------------------------------------------------- |
| `finitestate:metadata:organization_id`     | Internal Finite State identifier for the organization that uploaded the given firmware   |
| `finitestate:metadata:product_firmware_id` | Internal Finite State identifier for relationship between the given product and firmware |
| `finitestate:metadata:product_id`          | Internal Finite State identifier for product the SBOM applies to                         |
| `finitestate:metadata:firmware_id`         | Internal Finite State identifier for firmware the SBOM applies to                        |

## `finitestate:sbom` Namespace Taxonomy

| Property Name                     | Description                                                                                                            |
| --------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `finitestate:sbom:component_type` | Type of the component as listed in the Finite State SBOM (such as package, subcomponent, or kernel module)             |
| `finitestate:sbom:sbom_entry_id`  | The Finite State-specific identifier for the given entry in the SBOM. Formatted as a 64-character alphanumeric string. |
| `finitestate:sbom:component_id`   | The Finite State-specific ID for the given component. Formatted as a 64-character alphanumeric string.                 |
| `finitestate:sbom:confidence`     | The 0.0 - 1.0 confidence value that Finite State analysis has assigned to this component.                              |
| `finitestate:sbom:comments`       | Stringified JSON list of dictionaries containing comments made on this component in the Finite State analysis UI.      |
| `finitestate:sbom:resolutions`    | Stringified JSON list of dictionaries containing resolutions made on this component in the Finite State analysis UI.   |

## `finitestate:vulnerability` Namespace Taxonomy

| Property Name                     | Description                                                                                                                                        |
| --------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `finitestate:vulnerability:confidence`  | The 0.0 - 1.0 confidence value that Finite State analysis has assigned to this vulnerability.                                                |
| `finitestate:vulnerability:evidence`    | Stringified JSON dictionary of the evidence (CPE, PURL, etc) used by Finite State analysis to determine applicability of this vulnerability. |
| `finitestate:vulnerability:comments`    | Stringified JSON list of dictionaries containing comments made on this vulnerability in the Finite State analysis UI.                        |
| `finitestate:vulnerability:resolutions` | Stringified JSON list of dictionaries containing resolutions made on this vulnerability in the Finite State analysis UI.                     |

## `finitestate:finding` Namespace Taxonomy

These properties will only appear on `vulnerability` entries in Finite State-produced CycloneDX documents.

| Property Name                                | Description                                                                 |
| -------------------------------------------- | --------------------------------------------------------------------------- |
| `finitestate:finding:affected_file_path`     | The file path affected by the vulnerability entry.                          |
| `finitestate:finding:affected_file_hash`     | The SHA256 of the contents of the file affected by the vulnerability entry. |
| `finitestate:finding:affected_function_name` | The name of the funciton directly affected by the vulnerability.            |
| `finitestate:finding:affected_line_number`   | The line number in the specified file at which the vulnerability occurs.    |
| `finitestate:finding:affected_file_offset`   | The offset into the given file at which the vulnerability occurs.           |
