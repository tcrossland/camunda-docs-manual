---

title: "Delete Local Case Execution Variable"
weight: 240

menu:
  main:
    name: "Delete"
    identifier: "rest-api-case-execution-delete-local-variable"
    parent: "rest-api-case-execution-local-variables"
    pre: "DELETE `/case-execution/{id}/localVariables/{varId}`"

---


Deletes a variable in the context of a given case execution. Deletion does not propagate upwards in the case execution hierarchy.


# Method

DELETE `/case-execution/{id}/localVariables/{varId}`


# Parameters

## Path Parameters

<table class="table table-striped">
  <tr>
    <th>Name</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>id</td>
    <td>The id of the case execution to delete the variable from.</td>
  </tr>
  <tr>
    <td>varId</td>
    <td>The name of the variable to delete.</td>
  </tr>
</table>


# Result

This method returns no content.


# Response Codes

<table class="table table-striped">
  <tr>
    <th>Code</th>
    <th>Media type</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>204</td>
    <td></td>
    <td>Request successful.</td>
  </tr>
</table>


# Example

## Request

DELETE `/case-execution/aCaseExecutionId/localVariables/aVarName`


## Response

Status 204. No content.
