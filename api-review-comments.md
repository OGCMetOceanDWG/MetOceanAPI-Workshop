# API Review Comments

API comments against `http://HOST/getcube/1.0.0`

@tomkralidis
- working to implement in [pygeoapi](https://github.com/geopython/pygeoapi)
- working to test common OpenAPI bits against OWSLib WFS 3.0 client
  - then create a MetOceanAPI client

- suggest the following patterns
  - have version as `x.y` (bug fixes implicit) i.e. `/cube/1.0/collections/`
  - `/cube/1.0/collections` is a list of collections
    - align w/ WFS 3.0
      - `name`, `title`, `description`, `links`
    - `/cube/1.0/collections/{collectionId}`
    - describes the coverage or function
    - describes the functions that are available
  - `/cube/1.0/collections/{collectionId}/items` provides the data
  
@benjwadams
- `timePeriod` description says "ISO8601 time range which covers the time period that the data represents"  There are quite a few valid ISO8601 date/time forms.  Are we supporting all of these or primarily just "YYYY-MM-DDTHH:MM:SS.ssssZ" ?
