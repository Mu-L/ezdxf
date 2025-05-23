# Release Notes for v1.4.0
	- Changelog: ((676bc8de-2863-4635-945c-4ef79a74d93e))
- ## New Modules to Find Chains and Loops
	- The `ezdxf.edgeminer` module for seaching of connected edges and closed loops to:
		- build polylines from DXF primitives like LINE, ARC, ELLIPSE, SPLINE
		- build hatch boundary paths from DXF primitives
		- find open chains or closed loops in an unordered heap of DXF primitives (edges)
		- in general: find connections between edges
	- The `ezdxf.edgesmith` module for creating edges from DXF entities and creating polylines and hatches from connected edges:
		- create edges from DXF primitives for processing by the `edgeminer` module:
			- LINE, ARC, ELLIPSE, SPLINE, LWPOLYLINE, POLYLINE
		- create LWPOLYLINE and POLYLINE entities from a sequence of edges.
		- create HATCH boundary paths from a sequence of edges.
		- create `ezdxf.path.Path` objects from a sequence of edges.
	- ### Documentation
		- [EdgeMiner](https://ezdxf.mozman.at/docs/edgeminer.html)
		- [EdgeSmith](https://ezdxf.mozman.at/docs/edgesmith.html)
		- [Tutorial for Finding Chains and Loops](https://ezdxf.mozman.at/docs/tutorials/edges.html)
		- [Examples](https://github.com/mozman/ezdxf/tree/master/examples/edgeminer)
- ## New Methods
	- `Polyline.points_in_wcs()` [docs](https://ezdxf.mozman.at/docs/dxfentities/polyline.html#ezdxf.entities.Polyline.points_in_wcs)
	- `EdgePath.close_gaps()` [docs](https://ezdxf.mozman.at/docs/dxfentities/hatch.html#ezdxf.entities.EdgePath.close_gaps)
	- `BSpline.degree_elevation()` [docs](https://ezdxf.mozman.at/docs/math/core.html#ezdxf.math.BSpline.degree_elevation)
	- `BSpline.point_inversion()` [docs](https://ezdxf.mozman.at/docs/math/core.html#ezdxf.math.BSpline.point_inversion)
	- `BSpline.measure()` [docs](https://ezdxf.mozman.at/docs/math/core.html#ezdxf.math.BSpline.measure)
	- `BSpline.split()` [docs](https://ezdxf.mozman.at/docs/math/core.html#ezdxf.math.BSpline.split)
	- `BSpline.insert_knot()` and `BSpline.knot_refinement()` supports rational splines [docs](https://ezdxf.mozman.at/docs/math/core.html#ezdxf.math.BSpline.insert_knot)
- The v1.4.x releases are the last with Python 3.9 support because Python 3.9 reaches [End of Life](https://devguide.python.org/versions/) in 2025-10.
- # Relase v1.4.1
	- Changelog: ((67d7c218-9aca-4788-bdc7-58b33915832c))
	- Bugfix release