# Issue38980

This is a playground to test out the issue at https://github.com/angular/angular/issues/38980

There are two buttons in AppComponent marked for i18n translation.

```html
<button i18n>
  <icon value="notebook"></icon>
  Edit {{ 1 + 1 // i18n(ph="number") }}
</button>
<button i18n>
  <icon value="pencil"></icon>
  Edit {{ 1 + 1 // i18n(ph="number") }}
</button>
```

The CLI has been configured to generate 9 different translation file outputs:

1) ivy: off + xlf / xlf2 / xmb
2) ivy: on + xlf / xlf2 / xmb
3) ivy: on + legacy message ids disabled + xlf / xlf2 / xmb

According to this issue you would expect to see two different messages extracted in the translation file.
But there appears to be only one.