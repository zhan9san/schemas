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
      "additionalProperty": "pre_tasks"
    },
    "schemaPath": "#/$defs/ansible.builtin.import_playbook/additionalProperties"
  },
  {
    "instancePath": "/0",
    "keyword": "additionalProperties",
    "message": "must NOT have additional properties",
    "params": {
      "additionalProperty": "post_tasks"
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
    "instancePath": "/0",
    "keyword": "additionalProperties",
    "message": "must NOT have additional properties",
    "params": {
      "additionalProperty": "handlers"
    },
    "schemaPath": "#/$defs/ansible.builtin.import_playbook/additionalProperties"
  },
  {
    "instancePath": "/0/handlers",
    "keyword": "type",
    "message": "must be array,null",
    "params": {
      "type": [
        "array",
        "null"
      ]
    },
    "schemaPath": "#/type"
  },
  {
    "instancePath": "/0/post_tasks",
    "keyword": "type",
    "message": "must be array,null",
    "params": {
      "type": [
        "array",
        "null"
      ]
    },
    "schemaPath": "#/type"
  },
  {
    "instancePath": "/0/pre_tasks",
    "keyword": "type",
    "message": "must be array,null",
    "params": {
      "type": [
        "array",
        "null"
      ]
    },
    "schemaPath": "#/type"
  },
  {
    "instancePath": "/0/tasks",
    "keyword": "type",
    "message": "must be array,null",
    "params": {
      "type": [
        "array",
        "null"
      ]
    },
    "schemaPath": "#/type"
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
      "filename": "negative_test/playbooks/tasks.yml",
      "path": "$[0]",
      "message": "{'hosts': 'localhost', 'pre_tasks': 'foo', 'post_tasks': {}, 'tasks': 1, 'handlers': 1.0} is not valid under any of the given schemas",
      "has_sub_errors": true,
      "best_match": {
        "path": "$[0]",
        "message": "'handlers', 'hosts', 'post_tasks', 'pre_tasks', 'tasks' do not match any of the regexes: '^(ansible\\\\.builtin\\\\.)?import_playbook$', 'name', 'vars'"
      }
    }
  ]
}
```