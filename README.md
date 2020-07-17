## FluentUI List Component Bug Repro

This project reproduces an error in the `@fluentui/react-northstar` `<List>` component (version `0.50.0`). The issue is tracked in [bug #14091](https://github.com/microsoft/fluentui/issues/14091).

To see it, run the app (which contains a simple `<List>` component with the `selectable` property set to `true`). Then select a different item on the list. You will see this error in your console:

```
index.js:27 Warning: Cannot update a component (`ListItem`) while rendering a different component (`ContextSelector.Provider`). To locate the bad setState() call inside `ContextSelector.Provider`, follow the stack trace as described in https://fb.me/setstate-in-render
    in ContextSelector.Provider (created by List)
    in ul (created by FocusZone)
    in FocusZone (created by List)
    in List (at example.js:22)
    in ListExampleSelectable (at index.js:13)
    in div (created by SandboxApp)
    in KnobProvider (created by SandboxApp)
    in div (created by Provider)
    in ThemeProvider (created by Provider)
    in RendererProvider (created by Provider)
    in Provider (created by Provider)
    in Provider (created by SandboxApp)
    in SandboxApp (at index.js:12)
```
