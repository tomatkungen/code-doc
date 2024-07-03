* type of syntax, plusToken, FirstStatement
* enum ts.SyntaxKind 

```typescript
const node: ts.Node;

ts.SyntaxKind(node.kind);
```

```typescript
enum SyntaxKind {
    ...
    FirstStatement = 243,
    VariableStatement = 243,
    DebuggerStatement = 259,
    LastStatement = 259,
    ...
}
```
