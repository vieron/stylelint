# block-opening-brace-newline-before

Require a newline or disallow whitespace before the opening brace of blocks.

```css
  a
    { color: pink; }
/** ↑
 * The newline before this brace */
```

## Options

`string`: `"always"|"always-single-line"|"never-single-line"|"always-multi-line"|"never-multi-line"`

### `"always"`

There *must always* be a newline before the opening brace.

The following patterns are considered warnings:

```css
a{ color: pink; }
```

```css
a{ color: pink;
}
```

The following patterns are *not* considered warnings:

```css
a
{ color: pink; }
```

```css
a
{
color: pink; }
```

### `"always-single-line"`

There *must always* be a newline before the opening brace in single-line blocks.

The following patterns are considered warnings:

```css
a{ color: pink; }
```

The following patterns are *not* considered warnings:

```css
a
{ color: pink; }
```

```css
a{
color: pink; }
```

### `"never-single-line"`

There *must never* be whitespace before the opening brace in single-line blocks.

The following patterns are considered warnings:

```css
a { color: pink; }
```

The following patterns are *not* considered warnings:

```css
a{ color: pink; }
```

```css
a {
color: pink; }
```

### `"always-multi-line"`

There *must always* be a newline before the opening brace in multi-line blocks.

The following patterns are considered warnings:

```css
a{
color: pink; }
```

The following patterns are *not* considered warnings:

```css
a{ color: pink; }
```

```css
a {
color: pink; }
```

### `"never-multi-line"`

There *must never* be whitespace before the opening brace in multi-line blocks.

The following patterns are considered warnings:

```css
a {
color: pink; }
```

The following patterns are *not* considered warnings:

```css
a { color: pink; }
```

```css
a{
color: pink;}
```
