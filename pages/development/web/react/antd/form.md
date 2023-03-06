# Working with Antd Form

Antd have built in form management and support complex usage. It might seem overwhelming and hard to work with it for beginner or antd first time user. Here are some notes I tried to collect for my own future reference.

## Preparations / Basics

1. Wrap the whole form with [`Form`](https://4x.ant.design/components/form/) component.
2. Create form hook through `Form.useForm`:

```js
const [form] = Form.useForm()
```

3. Make sure to wrap each fields with `Form.Item` and define `name` (similar concept like `react-hook-form` or `formik`).

## Things to Aware with Form

1. Attach `form` state to `Form`.
2. Define `initialValues` with state / immutable, not normal object.
   Why? Turns out anything passed to `initialValues` is prone to be unstable / becomes mutable. I tried to work around it with making sure passing state into it as state is immutable. This must be awared especially after switching back and forth between pages.
3. `Form` provide `onFinish` that will only be triggered when submit and validation is success.
4. `Form` provide `onFailure` that will be triggered when submit and validation is not passing.
5. `Form.Item` provide `rules` to define field validation.

## Things to Aware with Inputs

Input, Select, NumberInput

1. For general purpose inputs, use `Input` component.
2. For numeric inputs and expecting form state to also receive number, use `NumberInput` component.
3. For formatted number input, use `NumericInput` of `react-number-format` and set customInput prop as `Input`.

## Working with Array fields

1. `Form.List` can be used for array property / attribute of the form shape.
2. `Form.List` provide render function children: `(fields, { add, remove, move }) => React.ReactNode`
3. We can combine `Form.List` with `Table` and pass `fields` as Table's `dataSource`.

## Useful References

- https://ant.design/components/form
- https://codesandbox.io/s/antd-rich-list-demo-v2-z7wjf?file=/index.js
