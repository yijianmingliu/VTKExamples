### Description

This demonstrates a simple visualization pipeline. A polygonal representation of a sphere is created with the source object (vtkSphereSource). The sphere is passed through a filter (vtkElevationFilter) that computes the height of each point of the sphere above a plane. The plane is perpendicular to the z-axis, and passes through the point (0,0,-1). The data is finally mapped (vtkDataSetMapper) through a lookup table. The mapping process converts height value into colors, and interfaces the sphere geometry to the rendering library. The mapper is assigned to an actor, and then the actor is displayed.

The execution of the pipeline occurs implicitly when we render the actor. Each actor asks its mapper to update itself. The mapper in turn asks its input to update itself. This process continues until a source object is encountered. Then the source will execute if modified since the last render.

!!! info
    See [Figure 4-19](/VTKBook/04Chapter4/#Figure%204-19) in [Chapter 4](/VTKBook/04Chapter4) the [VTK Textbook](/VTKBook/01Chapter1).
    
