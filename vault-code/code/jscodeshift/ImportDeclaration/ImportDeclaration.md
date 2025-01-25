* jscodeshift.ImportDeclaration - fetch all imports in a file *.tsx or *.ts

```typescript
// import <func, func..> from <alias>

// ImportDefaultSpecifier
import React from "react"            // export default react

// ImportNamespaceSpecifier
import * as MUI from "@mui/material" // export default react
	
// ImportSpecifier
import { Box } from "@mui/material"   // export {useEffect}
import { Button as Buttons } from "@mui/material"
```

```typescript
interface ImportDeclaration {
	node: {
		source: LiteralKind
		specifiers?: (
			ImportDefaultSpecifier, ImportSpecifier, ImportNamespaceSpecifier
		)[]
	}
}
```

```typescript
// import .. from "@mui/material"
interface LiteralKind: {
	type: "Literal"
	value: string | boolean | null | number | regExp // "@mui/material"
	regExt: {...}
}
```

```typescript
// import React from "react" <- export default React
interface ImportDefaultSpecifier {
	type: "ImportDefaultSpecifier"
	local?: { name: string } // React
}
```

```typescript
// import { Box } from "@mui/material" <- export {Box}
// import { Button as Buttons } from "@mui/material" <- export {Button}
interface ImportSpecifier {
	type: "ImportSpecifier"
	imported: { name: string } // "Box" | "Button"
	local?: { name: string } // "Buttons" | "Box"
}
```

```typescript
// import * as MUI from "@mui/material" <- export namespace My.utils
interface ImportNamespaceSpecifier{
	type: "ImportNamespaceSpecifier"
	local?: { name: string } // "MUI"
}
```