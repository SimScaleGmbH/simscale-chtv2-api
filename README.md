# SimScale_CHTv2
The main goal of this code is to demonstrate how to run conjugate heat transfer (CHTv2) simulations on SimScale via the API. 

The repository already contains a working example that can be used for testing, which is a cold cooling plate for a battery system. 

This code should serve the purpose of showing: (All the functions can be found in the utilities.py file) 
1. How to setup the API connection. 
2. How to create a project and upload geometries 
3. How to retrieve entity IDs of parts and surfaces, so that they can be used for assignment of boundary conditions, advanced concepts, etc.
4. How to define a material directly from the default SimScale material library via the API 
5. How to apply boundary conditions via the API (almost all boundary conditions are coded in the utilities file for reference) 
6. How to define advanced concepts (power sources, momentum sources, porous media: would be added in the future)
7. How to define result control items (area averages, area integrals, probe points) 
8. How to define geometry primitives( points, cartesian box, cylinders) 
9. How to create a mesh and add mesh refinements 
10. How to check for the computing resources of a mesh and a simulation 
11. Run the simulation 
12. Download results 

To use the code, you need to have a SimScale API key

Note: When running a CHTv2 simulation via the API, defining contacts is not required. 
In CHTv2.0 the addition of contacts is not necessary for the heat transfer through the interfaces. The relationship in those interfaces is automatically detected by the meshing algorithm and defined as a coupled interface (perfect heat transfer across the interface - behind the scenes). Meaning those interfaces between the solid and the flow volume are accounted for and heat transfer is expected to occur out of the box.
