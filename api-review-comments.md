# API Review Comments

@tomkralidis
- working to implement in [pygeoapi](https://github.com/geopython/pygeoapi)
- `/getcube/1.0.0/collections/{collectionId}/items`
- suggest the following patterns
  - have version as x.y (bug fixes implicit) i.e .`/cube/1.0/collections/
  - `/cube/1.0/collections` is a list of collections
  - `/cube/1.0/collections/{collectionId}/` describes the coverage or function
  - `/cube/1.0/collections/{collectionId}/items` should provide the data or at least a form
