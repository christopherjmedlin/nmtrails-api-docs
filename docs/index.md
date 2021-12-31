# NMTrails API

This is the documentation for NMTrail's REST API.

## Collections

### Trails

#### List Trails

URI: **GET** /trails/

Returns a list of trails sorted by popularity

**Query Parameters**:

| Name | Description|
|------|------------|
| name | A search query for the name of the trail |
| page | Page number |
| pageSize | Size of page |

#### Trail Extent

URI: **GET** /trails/extent

Returns a bounding box for the trail(s) specified by the id(s) (in GeoJSON format)

**Query Parameters**:

| Name | Description |
|------|-------------|
| ids | Comma seperated list of trail ids |

#### Get Trail

URI: **GET** /trails/{id}

Returns the trail specified by the id.

#### Get Segments

URI: **GET** /trails/{id}/segments

Returns every segment (LineString) associated with this trail.

### Regions

#### List Regions

URI: **GET** /regions/

Returns a list of every region.

**Query Parameters**

| Name | Description |
|------|-------------|
| page | Page number |
| pageSize | Size of page |


#### Trails in Region

URI: **GET** /regions/{id}/trails

Gives every trail contained in the specified region

#### Featured Region

URI: **GET** /regions/featured

Gives a random region.


