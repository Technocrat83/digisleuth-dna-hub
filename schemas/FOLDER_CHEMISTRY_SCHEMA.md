# FOLDER CHEMISTRY SCHEMA
## DIGISLEUTH_FOLDER_CHEMISTRY_SCHEMA_v1

STATUS: CANONICAL_SCHEMA  
CLASSIFICATION:
- PRE_HYDRATION_VALIDATION_SCHEMA
- CHAMBER_MATURITY_CHECKLIST
- FILESYSTEM_ORGANOGENESIS_MODEL
- MARKDOWN_CRYSTAL_ADMISSIBILITY_GATE

---

# PRIME DIRECTIVE

This schema determines whether a folder chamber is mature enough
to receive Markdown Crystal hydration.

---

# REQUIRED CHAMBER FIELDS

```yaml
folder_chemistry_schema:

  chamber_name:
    type: string
    required: true

  chamber_path:
    type: string
    required: true

  chamber_identity:
    type: string
    required: true

  membrane_boundary:
    type: string
    required: true

  topology_role:
    type: string
    required: true

  upstream_inputs:
    type: list
    required: true

  downstream_outputs:
    type: list
    required: true

  pressure_relationships:
    type: list
    required: true

  semantic_nutrients:
    type: list
    required: true

  produced_residue:
    type: list
    required: true

  governance_constraints:
    type: list
    required: true

  federation_relationships:
    type: list
    required: true

  hydration_readiness:
    type: enum
    values:
      - EMPTY_CONTAINER
      - CHEMISTRY_DECLARED
      - PRESSURE_BOUND
      - GOVERNANCE_BOUND
      - HYDRATED_ORGAN
      - FEDERATION_CONNECTED

  hydration_allowed:
    type: boolean
    required: true
