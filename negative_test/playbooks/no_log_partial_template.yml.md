# ajv errors

```json
[
  {
    "instancePath": "/0",
    "keyword": "required",
    "message": "must have required property 'ansible.builtin.import_playbook'",
    "params": {
      "missingProperty": "ansible.builtin.import_playbook"
    },
    "schemaPath": "#/$defs/ansible.builtin.import_playbook/oneOf/0/required"
  },
  {
    "instancePath": "/0",
    "keyword": "required",
    "message": "must have required property 'import_playbook'",
    "params": {
      "missingProperty": "import_playbook"
    },
    "schemaPath": "#/$defs/ansible.builtin.import_playbook/oneOf/1/required"
  },
  {
    "instancePath": "/0",
    "keyword": "oneOf",
    "message": "must match exactly one schema in oneOf",
    "params": {
      "passingSchemas": null
    },
    "schemaPath": "#/$defs/ansible.builtin.import_playbook/oneOf"
  },
  {
    "instancePath": "/0",
    "keyword": "additionalProperties",
    "message": "must NOT have additional properties",
    "params": {
      "additionalProperty": "hosts"
    },
    "schemaPath": "#/$defs/ansible.builtin.import_playbook/additionalProperties"
  },
  {
    "instancePath": "/0",
    "keyword": "additionalProperties",
    "message": "must NOT have additional properties",
    "params": {
      "additionalProperty": "tasks"
    },
    "schemaPath": "#/$defs/ansible.builtin.import_playbook/additionalProperties"
  },
  {
    "instancePath": "/0/tasks/0/no_log",
    "keyword": "type",
    "message": "must be boolean",
    "params": {
      "type": "boolean"
    },
    "schemaPath": "#/oneOf/0/type"
  },
  {
    "instancePath": "/0/tasks/0/no_log",
    "keyword": "pattern",
    "message": "must match pattern \"^\\{\\{.*\\}\\}$\"",
    "params": {
      "pattern": "^\\{\\{.*\\}\\}$"
    },
    "schemaPath": "#/$defs/full-jinja/pattern"
  },
  {
    "instancePath": "/0/tasks/0/no_log",
    "keyword": "oneOf",
    "message": "must match exactly one schema in oneOf",
    "params": {
      "passingSchemas": null
    },
    "schemaPath": "#/oneOf"
  },
  {
    "instancePath": "/0/tasks/0",
    "keyword": "required",
    "message": "must have required property 'block'",
    "params": {
      "missingProperty": "block"
    },
    "schemaPath": "#/required"
  },
  {
    "instancePath": "/0/tasks/0/no_log",
    "keyword": "type",
    "message": "must be boolean",
    "params": {
      "type": "boolean"
    },
    "schemaPath": "#/oneOf/0/type"
  },
  {
    "instancePath": "/0/tasks/0/no_log",
    "keyword": "pattern",
    "message": "must match pattern \"^\\{\\{.*\\}\\}$\"",
    "params": {
      "pattern": "^\\{\\{.*\\}\\}$"
    },
    "schemaPath": "#/$defs/full-jinja/pattern"
  },
  {
    "instancePath": "/0/tasks/0/no_log",
    "keyword": "oneOf",
    "message": "must match exactly one schema in oneOf",
    "params": {
      "passingSchemas": null
    },
    "schemaPath": "#/oneOf"
  },
  {
    "instancePath": "/0/tasks/0",
    "keyword": "anyOf",
    "message": "must match a schema in anyOf",
    "params": {},
    "schemaPath": "#/items/anyOf"
  },
  {
    "instancePath": "/0",
    "keyword": "oneOf",
    "message": "must match exactly one schema in oneOf",
    "params": {
      "passingSchemas": null
    },
    "schemaPath": "#/items/oneOf"
  }
]
```

# check-jsonschema

stdout:

```json
{
  "status": "fail",
  "errors": [
    {
      "filename": "negative_test/playbooks/no_log_partial_template.yml",
      "path": "$[0]",
      "message": "{'hosts': 'localhost', 'vars': {'some_var': True}, 'tasks': [{'ansible.builtin.debug': {'msg': 'foo'}, 'no_log': 'foo-{{ some_var }}'}]} is not valid under any of the given schemas",
      "has_sub_errors": true,
      "best_match": {
        "path": "$[0]",
        "message": "'hosts', 'tasks' do not match any of the regexes: '^(ansible\\\\.builtin\\\\.)?import_playbook$', 'name', 'vars'"
      }
    }
  ]
}
```