# Abaqus-Plug-in-for-Cohesive-Elements

An ABAQUS Plug-in for Generating Cohesive Elements

Plug-in features
1. It is applicable to inserting zero-thickness cohesive elements with/without pore-pressure nodes in 2D and 3D solid parts.

2. It is applicable to parts with multiple element types. In the 2D case, there can be both triangular and quadrilateral elements in the mesh; In the 3D case, there can be tetrahedral elements, triangular prism elements, and hexahedral elements in the mesh at the same time.

3. The insertion speed is very fastest. It takes about 190 seconds to insert 3 million cohesive elements into a part.

4. The position where the cohesive elements are inserted can be set flexibly. They can be inserted globally, on the interface between element sets, on the boundary, or in the interior of regions at the same time. When setting, you need to set a “matrix” set and several optional “inclusion” sets. The matrix set and the inclusion sets cannot have public elements (the plug-in will automatically detect). The matrix set can have public nodes with the inclusion sets, but there can be no public nodes between the inclusion sets. For both matrix and inclusion sets, you can choose whether to insert cohesive elements into the set, which is very flexible.

5. Automatically create cohesive element sets according to the settings. For the cohesive elements generated inside a region, add "-cohesives" after the original set name, such as “set-1-cohesives”; The set name for the elements generated on the boundary is named as set1’s name + "-by-" + set2’s name + "-cohesives", such as “set-1-by-set-2-cohesives”.

6. With the “special set” function, you can create a cohesive set separately for the edges set (2D) and faces set (3D) during element insertion to facilitate subsequent material attribute assignment. Common occasions: rock joint surface and crystal grain interface. Two sets are created: the cohesives set on the specified face and the set of remaining cohesive elements, so as to assign material attributes respectively.

7. Using the “create coherent set after insertion” function, you can subdivide the cohesive element into subsets after insertion. Common occasions: generating cohesive element sets for multiple material properties in recycled aggregate modeling; Interface element differentiation of multilayer composites.

8. Select the "add pore pressure nodes" option to insert the pore-pressure cohesive elements and create a pore-pressure node (intermediate node) set “PorePressure Midnodes”.

Notices: if cohesive elements are not on the boundaries(interfaces), you can insert elements only once for the origin part.

More details can be found at 
https://abaquscohesiveelementplugin.quora.com/An-ABAQUS-Plug-in-for-Generating-Cohesive-Elements

Video tutorial
https://youtu.be/Pqs16uhnaWs


Trial download and Purchase

The installation of ABAQUS plug-ins can be found by Google. Before the plug-in is activated by the license file, it can only be used for parts with no more than 1000 elements. There will be no limits on the number of elements and use time after activating.
Applicable to abaqus6.14 and above.
Any questions about the Plug-in, please contact the author by Skype “live:672366751”
or Email 672366751@qq.com (mailto:672366751@qq.com)
