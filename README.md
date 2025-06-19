# SSCCE: proj4 type incompatibility with ol

See: 

* https://github.com/geojupyter/jupytergis/issues/777
* https://github.com/geojupyter/jupytergis/pull/576#issuecomment-2988238616
* https://github.com/proj4js/proj4js/pull/509
* https://github.com/proj4js/proj4js/issues/510


## Reproduce

```bash
npm run build
```


## Presentation

```bash
$ npm run build

> ol-proj4-compat@0.0.1 build
> tsc -p .

index.ts:4:10 - error TS2345: Argument of type 'ProjectionDefinition' is not assignable to parameter of type 'typeof import("/home/robatt/_test/proj4-type/ol-proj4-compat/node_modules/proj4/dist/lib/index")'.
  Property 'proj4' is missing in type 'ProjectionDefinition' but required in type 'typeof import("/home/robatt/_test/proj4-type/ol-proj4-compat/node_modules/proj4/dist/lib/index")'.

4 register(proj4.defs("EPSG:3413"));
           ~~~~~~~~~~~~~~~~~~~~~~~

  node_modules/proj4/dist/lib/index.d.ts:1:1
    1 export default proj4;
      ~~~~~~~~~~~~~~~~~~~~~
    'proj4' is declared here.


Found 1 error in index.ts:4
```
