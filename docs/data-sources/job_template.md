---
page_title: "aap_job_template Data Source - terraform-provider-aap"
description: |-
  Get an existing JobTemplate.
---

# aap_job_template (Data Source)

Get an existing JobTemplate.



<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `id` (Number) JobTemplate id
- `name` (String) Name of the JobTemplate
- `organization_name` (String) The name for the organization to which the JobTemplate belongs

### Read-Only

- `description` (String) Description of the JobTemplate
- `named_url` (String) The Named Url of the JobTemplate
- `organization` (Number) Identifier for the organization to which the JobTemplate belongs
- `url` (String) Url of the JobTemplate
- `variables` (String) Variables of the JobTemplate. Will be either JSON or YAML string depending on how the variables were entered into AAP.

## Job Template Look Up

You can look up Job Templates by using either the `id` or a combination of `name` and `organization_name`.

```terraform
data "aap_job_template" "sample" {
  id = 1
}

data "aap_job_template" "sample" {
  name = "My Job Template"
  organization_name = "My Organization"
}
```