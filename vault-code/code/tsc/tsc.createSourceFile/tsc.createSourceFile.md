* Create sourcefile

```typescript
// Example
import * as ts from "typescript";

const filename = "test.ts";
const code = `const test: number = 1 + 2;`;

// Create source file
const sourceFile = ts.createSourceFile(
	filename,
	code,
	ts.ScriptTarget.Latest
);

console.log(sourceFile.fileName)
console.log(sourceFile.text)
```

```typescript
function createSourceFile(
	fileName: string,
	sourceText: string,
	languageVersionOrOptions: ScriptTarget | CreateSourceFileOptions,
	setParentNodes?: boolean,
	scriptKind?: ScriptKind
): SourceFile;

interface SourceFile {
	getLineAndCharacterOfPosition(pos: number): LineAndCharacter;
	getLineEndOfPosition(pos: number): number;
	getLineStarts(): readonly number[];
	getPositionOfLineAndCharacter(line: number, character: number): number;
	update(newText: string, textChangeRange: TextChangeRange): SourceFile;
}
interface SourceFile extends Declaration, LocalsContainer {
	readonly kind: SyntaxKind.SourceFile;
	readonly statements: NodeArray<Statement>;
	readonly endOfFileToken: Token<SyntaxKind.EndOfFileToken>;
	fileName: string;
	text: string;
	amdDependencies: readonly AmdDependency[];
	moduleName?: string;
	referencedFiles: readonly FileReference[];
	typeReferenceDirectives: readonly FileReference[];
	libReferenceDirectives: readonly FileReference[];
	languageVariant: LanguageVariant;
	isDeclarationFile: boolean;
	hasNoDefaultLib: boolean;
	languageVersion: ScriptTarget;
	impliedNodeFormat?: ResolutionMode;
}
```

