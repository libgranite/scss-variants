# SCSS Variants

This project provides a scss module to generate breakpoint variants for css rules.

## Usage

The following can be used to load the module from a scss file.

```
@use 'path/to/@libgranite/variants/entry' as variants with (
  $varients_list: (
    (
      'prefix': 'example',
      'media': '(100px < width < 200px)'
    )
  )
);

@include variants('class') {
  /** rules **/
}

```

The above code will generate the following css.

```
.class {
  /** rules **/
}

.prefix\:class {
  /** rules **/
}
```

## Defaults

A set of default breakpoints is provided.

 - `sm:` - Small - Width: 0 plus
 - `md:` - Medium - Width: 480px plus
 - `lg:` - Large - Width: 769px plus
 - `xl:` - Extra-Large - Width: 1280px plus

