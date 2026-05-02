#!/bin/bash
# TaskStart hook

INPUT=$(cat)
WORKSPACE=$(echo "$INPUT" | jq -r '.workspaceRoots[0] // empty')

# Read project info if available
if [[ -f "$WORKSPACE/.project-context" ]]; then
  CONTEXT=$(cat "$WORKSPACE/.project-context")
  echo "{\"cancel\":false,\"contextModification\":\"Project context: $CONTEXT\"}"
else
  echo '{"cancel":false}'
fi