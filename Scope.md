# Scope

The initial release [number, date] of the FinOps Open Billing specification will include the following:
Specifications: 
  - a Common Billing Format consisting of a list of all the dimensions and metrics a customer would use to analyze cloud cost and usage in aggregate. 
    This specification will be cloud neutral, service neutral, and vendor neutral.
  - Metadata about the Common Billing Format dataset related to its delivery, structure, formatting, frequency, recency, content, file size, etc. 
  - a number of source-specific mappings of the Common Billing Format to a particular source of cloud usage or cost data 
    (e.g. cloud vendor, software license vendor, etc.) including mappings, rationale for mappings, gaps where mapping cannot occur, 
    recommendations for workarounds, methods of accessing the data, the source data format, etc. 
    There will be one source-specific mapping for each source of data.
    Initial sources will include but not be limited to the AWS CUR file, Azure Billing File, GCP Billing data, MongoDB invoice
  - Cloud Service Provider Service-specific versions of mappings will also be developed where required and feasible
    These will include specific logic and mappings for specific types of services (e.g. EC2, S3, Google Compute Engine, BigQuery) 
    usually required where the mapping of cost metrics requires combinations of multiple service cost measures or allocation of fixed and variable 
    costs for a service to achieve compliance with the Common Billing Format
  - Mappings to OpenTelemetry project data taxonomy, indicating how elements of the Common Billing Format map to OpenTelemetry data structures
  - Mappings to ITFM/TBM data taxonomy, indicating how elements of the Common Billing Format map to the Towers and Cost Pools of TBM. 

Reference Implementations: 
  - Software which can be used to ingest any supported source of cost or usage data and translate its content to the common billing format
    Using the specification logic, and passing it to a common billing format intake API.
  - Software which can receive common billing format data and store it in a repository in one or more cloud environments
    Software would be executed in an environment owned and operated by a customer, or operated by a third party
  - Software which supports query access to the common billing format data once stored.

Use Cases: 
  - Examples of analysis you can do as a customer on the CBF. 
  - Persona or cloud or service specific use cases implemented in some specific way using the specifications and reference implementations.

Any changes of Scope are not retroactive. 
