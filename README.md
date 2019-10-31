# Angular + Ivy + webpack externals/UMD

- Serving: ``ng serve -o``
- Building with externals: npm run ``build:externals``
- Includes polyfills for web components in IE 11

## Findings 

1. All dependencies are part of the ``scripts`` section within ``angular.json``. No need to copy around UMD bundles anymore.
2. To make it work with Ivy, I call ngcc without parameters in the ``postinstall`` script. The original parameters prevent dealing with UMD.

## TODO

- Automate findings with schematics in ``ngx-build-plus``. 
