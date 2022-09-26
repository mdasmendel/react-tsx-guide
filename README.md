
### TSX File Names

TSX File names should be Pascal Case. It’s best to have a standard for file naming to keep folders easy to read.

Do:

```
MyFile.tsx
```

Don’t:

```
myFile.tsx
my-file.tsx
my_file.tsx
My_File.tsx
```

### Functional Component Declaration
I prefer const declarations for their succinct nature. Always include the FunctionComponent type to gain access to properties like children

Do:
```
const MyComponent: React.FunctionComponent = () => {}
```
Don’t:
```
const MyComponent = () => {}
function MyComponent() {}
```

### Named Exports
Named exports should be used when a component is part of a component library or any other configuration with many similar exports.
```
export const MyComponent1: React.FunctionComponent = () => {}
export const MyComponent2: React.FunctionComponent = () => {}
```

### Component Property Interfaces
When defining interfaces for component properties, always define variables first and functions second, separated by a space.

Do:
```
interface MyProps {
  var1: string
  var2: boolean
 
  function1(): void
}
const MyComponent: React.FunctionComponent = (props: MyProps) => {}
```
Don’t:
```
interface MyProps { 
  var1: string
  function1(): void
  var2: boolean
}
const MyComponent: React.FunctionComponent = (props: MyProps) => {}
```
