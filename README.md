# Po-Roman-Transport

The network model was created using the ArcGIS Network Analyst Suite, Version 10.8.1. 

In each folder, the vector shapefiles for each layer of the network model can be found. 

# Building the Network Dataset
The steps here outline the process to join the separate vector shapefiles representing the rivers, roads, canals, and sealanes of Northern Italy into a single network
dataset. ArcCatalog is used to create the network dataset from shapefiles contained within a file geodatabase. Note. Within ArcGIS, the Network Analyst Suite must be active.

1.	Select Network and create New Network Dataset.
2.	Name Network PoNetwork_ND
3.	Click Next.
4.	Select all files to be included. 
5.	Click Next.
6.	Click Yes for modelling turns.
7.	Click Next. 
8.	Click Connectivity.
9.	Increase Group Columns to 4. 
10.	Select Connectivity Groups, ensuring that juctions are selected for their corresponding vector layers.
11.	Click OK.
12.	Click Next.
13.	For Modelling Elevation Fields, select None.
14.	Click Next.
15.	Click Ok.
16.	Select Cost and click Evaluators.
17.	Select all Junctions and right click. 
18.	From Type select Field. 
19. From Value select STOPCOST. 
20.	Click OK. 
21.	Click Next.
22.	Click Next. 
23.	Select No for Establishing Driving Directions. 
24.	Click Next.
25.	Select Build Service Area Index. 
26.	Click Next. 
27.	Click Finish. 
28.	Click Yes. 

# Building the Service Area Index
The Service Area Index is used to generate the cost-surface polygons that map all accessible areas within a specified impedance from a set starting point or points.
ArcMap is used to create the polygons using the network dataset imported from ArcCatalog. Note. Within ArcGIS, the Network Analyst Suite must be active.

1. Under the Network Analyst toolbar, click New Service Area.
2. From the directory, select the site/sites you wish to act as the starting point for transport.
3. Drag the site/sites to the Facilities folder within the Layers box.
4. Click the Service Area Properties button in the top right-hand side of the Layers box to bring up the analysis layer’s Layer Properties dialogue box.
5. Select the Analysis Settings tab from the analysis layer’s Layer Properties dialog box.
6. Select Cost from the Impedance drop-down box.
7. Within the Default Breaks box, list multiples of 100 to act as the cost breaks between polygons.
8. Select Direction: Away from Facility.
9. Select U-Turns Allowed from the U-Turns at Junctions box.
10. Select the Polygon Generation tab from the analysis layer’s Layer Properties dialog box.
11. For Polygon Type, select Detailed.
12. Trim Polygons to 15 km.
13. Select Merge Polygons if using multiple facilities.
14. Click OK.
15. Click the ’Solve’ button on the Network Analyst toolbar to run the analysis.


