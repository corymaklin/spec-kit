

### Add explicit permissions
We want Claude to work independently for as long as possible so that we can focus my attention on other matters. However, by default, it will ask you to approve its use of tools like Python or the AWS CLI.

Use the wildcard to allow commands with those arguments.

Anything that does not modify the code should be allowed by default.

```json
{
	"permissions": {
		"allow": [
			"WebFetch",
			"Bash(npm install:*)",
			"mcp__context7__get-library-docs"
		]
	}
}
```

### Use subagents to review code
As of now, we will use the main context window for all code modifications. However, we can use subagents with specific domain knowledge to review the code and provide context to the main thread.

`Use ddd-expert to review code`

### Explore options before selecting one

### Stop it immediately when it does something wrong

### Use the spec command (and subsequent commands) for each end-to-end feature
This might ensure you don't need the vertical slice thing

