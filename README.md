# CycloneDX Property Taxonomy

This is the official Finite State CycloneDX property namespace and name taxonomy. It documents all custom key/value `properties` that may be added to components in CycloneDX SBOMs created using the Finite State software.

For more information about CycloneDX property taxonomies, refer to the [official documentation](https://github.com/CycloneDX/cyclonedx-property-taxonomy).

## `finitestate` Namespace Taxonomy

| Namespace              | Description                                                                                                             |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `finitestate:metadata` | Namespace for all Finite State-specific properties dealing with top-level metadata values about products and firmwares. |
| `finitestate:sbom`     | Namespace for all Finite State-specific properties dealing with SBOM values.                                            |

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
