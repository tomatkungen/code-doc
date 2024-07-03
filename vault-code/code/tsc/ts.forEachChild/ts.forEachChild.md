```typescript
import ts from 'typescript';
import { sourceFile } from "./createSourceFile";

function printRecursiveFrom(
	node: ts.Node, indentLevel: number, sourceFile: ts.SourceFile
) {
	const indentation = "-".repeat(indentLevel);
	const syntaxKind = ts.SyntaxKind[node.kind];
	const nodeText = node.getText(sourceFile);

	console.log(`${indentation}${syntaxKind}: ${nodeText}`);

	node.forEachChild(child =>
		printRecursiveFrom(child, indentLevel + 1, sourceFile)
	);
}

printRecursiveFrom(sourceFile, 0, sourceFile);
```

```typescript
// Output

SourceFile: const test: number = 1 + 2;
-FirstStatement: const test: number = 1 + 2;
--VariableDeclarationList: const test: number = 1 + 2
---VariableDeclaration: test: number = 1 + 2
----Identifier: test
----NumberKeyword: number
----BinaryExpression: 1 + 2
-----FirstLiteralToken: 1
-----PlusToken: +
-----FirstLiteralToken: 2
-EndOfFileToken:
```