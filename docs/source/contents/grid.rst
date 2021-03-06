This template has a built-in grid system that provides all the Bootstrap
layout building flexibily and powerful responsive behaviour.

Sections
--------

Content area is divided in three horizontal sections
(rows, named "1", "2", "3"), each of which includes the same,
rich structure of block positions.

.. image:: ../images/full_grid.png


Block Positions
---------------

Every section block position has a numeric prefix that identifies the
parent section (eg. 1, 2, 3).

We'll use '{}' to generalize the prefix.

+------------------------+---------------------------------+
| Position               | Description                     |
+========================+=================================+
| **menu-1**             | Main menu                       |
+------------------------+---------------------------------+
| **banner**             | Main banner                     |
+------------------------+---------------------------------+
| **menu-2**             | Secondary menu                  |
+------------------------+---------------------------------+
| **breadcrumbs**        | Breadcrumbs                     |
+------------------------+---------------------------------+
| **{}-top-a**           | Top area, position A            |
+------------------------+---------------------------------+
| **{}-top-b**           | Top area, position B            |
+------------------------+---------------------------------+
| **{}-top-c**           | Top area, position C            |
+------------------------+---------------------------------+
| **{}-mid-top-a**       | Middle-Top area, position A     |
+------------------------+---------------------------------+
| **{}-mid-top-b**       | Middle-Top area, position B     |
+------------------------+---------------------------------+
| **{}-mid-top-c**       | Middle-Top area, position C     |
+------------------------+---------------------------------+
| **{}-left-a**          | Left area, position A           |
+------------------------+---------------------------------+
| **{}-left-b**          | Left area, position B           |
+------------------------+---------------------------------+
| **{}-center-top-a**    | Center-Top area, position A     |
+------------------------+---------------------------------+
| **{}-center-top-b**    | Center-Top area, position B     |
+------------------------+---------------------------------+
| **{}-center-top-c**    | Center-Top area, position C     |
+------------------------+---------------------------------+
| **{}-center-content**  | Center content                  |
+------------------------+---------------------------------+
| **{}-center-bottom-a** | Center-Bottom area, position A  |
+------------------------+---------------------------------+
| **{}-center-bottom-b** | Center-Bottom area, position B  |
+------------------------+---------------------------------+
| **{}-center-bottom-c** | Center-Bottom area, position C  |
+------------------------+---------------------------------+
| **{}-mid-bottom-a**    | Middle-Bottom area, position A  |
+------------------------+---------------------------------+
| **{}-mid-bottom-b**    | Middle-Bottom area, position B  |
+------------------------+---------------------------------+
| **{}-mid-bottom-c**    | Middle-Bottom area, position C  |
+------------------------+---------------------------------+
| **{}-bottom-a**        | Bottom area, position A         |
+------------------------+---------------------------------+
| **{}-bottom-b**        | Bottom area, position B         |
+------------------------+---------------------------------+
| **{}-bottom-c**        | Bottom area, position C         |
+------------------------+---------------------------------+


Blocks ratio
------------

Every block position has a specific Bootstrap style class that define
its ratio in the parent area (top, middle-top, etc...).

There is a Django template block surrounding HTML class attribute to
permit an easy override in custom templates based on this.

+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| Class Django block                      | Description (class value of)                            | Value                         |
+=========================================+=========================================================+===============================+
| **{% block section_{}_classes %}**      | section-{}                                              | py-5                          |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block section_2_classes %}**       | section-2                                               | py-5 neutral-2-bg             |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_top_abc_a %}**            | {}-top-a if A,B,C are visible                           | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_top_abc_b %}**            | {}-top-b if A,B,C are visible                           | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_top_abc_b %}**            | {}-top-c if A,B,C are visible                           | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_top_ab_a %}**             | {}-top-a if A,B are visible                             | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_top_ab_b %}**             | {}-top-b if A,B are visible                             | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_top_ac_a %}**             | {}-top-a if A,C are visible                             | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_top_ac_c %}**             | {}-top-c if A,C are visible                             | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_top_bc_b %}**             | {}-top-a if B,C are visible                             | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_top_bc_c %}**             | {}-top-c if B,C are visible                             | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_top_abc_a %}**        | {}-mid-top-a if A,B,C are visible                       | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_top_abc_b %}**        | {}-mid-top-b if A,B,C are visible                       | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_top_abc_b %}**        | {}-mid-top-c if A,B,C are visible                       | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_top_ab_a %}**         | {}-mid-top-a if A,B are visible                         | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_top_ab_b %}**         | {}-mid-top-b if A,B are visible                         | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_top_ac_a %}**         | {}-mid-top-a if A,C are visible                         | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_top_ac_c %}**         | {}-mid-top-c if A,C are visible                         | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_top_bc_b %}**         | {}-mid-top-a if B,C are visible                         | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_top_bc_c %}**         | {}-mid-top-c if B,C are visible                         | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_left_ab %}**              | {}-left column if left A,B are visible                  | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_left_a %}**               | {}-left column if left A is visible                     | col-12 col-md-3               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_left_b %}**               | {}-left column if left B is visible                     | col-12 col-md-2               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_left_ab_a %}**            | {}-left-a column if A,B are visible                     | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_left_ab_b %}**            | {}-left-b column if A,B are visible                     | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_left_no_center_ab %}**    | {}-left column if left A,B are visible but no center    | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_left_no_center_a %}**     | {}-left column if left A is visible but no center       | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_left_no_center_b %}**     | {}-left column if left B is visible but no center       | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_left_no_center_ab_a %}**  | {}-left-a column if A,B are visible but no center       | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_left_no_center_ab_b %}**  | {}-left-b column if A,B are visible but no center       | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_left_ab %}**       | {}-center column if left A,B are visible                | col                           |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_left_a %}**        | {}-center column if left A is visible                   | col                           |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_left_b %}**        | {}-center column if left B is visible                   | col offset-md-1               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center %}**               | {}-center column if left is not visible                 | col                           |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_top_abc_a %}**     | {}-center-top-a column if A,B,C are visible             | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_top_abc_b %}**     | {}-center-top-b column if A,B,C are visible             | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_top_abc_c %}**     | {}-center-top-c column if A,B,C are visible             | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_top_ab_a %}**      | {}-center-top-a column if A,B are visible               | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_top_ab_b %}**      | {}-center-top-b column if A,B are visible               | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_top_ab_a %}**      | {}-center-top-a column if A,C are visible               | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_top_ac_c %}**      | {}-center-top-c column if A,C are visible               | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_top_bc_b %}**      | {}-center-top-b column if B,C are visible               | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_top_bc_c %}**      | {}-center-top-c column if B,C are visible               | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_bottom_abc_a %}**  | {}-center-bottom-a column if A,B,C are visible          | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_bottom_abc_b %}**  | {}-center-bottom-b column if A,B,C are visible          | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_bottom_abc_c %}**  | {}-center-bottom-c column if A,B,C are visible          | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_bottom_ab_a %}**   | {}-center-bottom-a column if A,B are visible            | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_bottom_ab_b %}**   | {}-center-bottom-b column if A,B are visible            | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_bottom_ab_a %}**   | {}-center-bottom-a column if A,C are visible            | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_bottom_ac_c %}**   | {}-center-bottom-c column if A,C are visible            | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_bottom_bc_b %}**   | {}-center-bottom-b column if B,C are visible            | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_center_bottom_bc_c %}**   | {}-center-bottom-c column if B,C are visible            | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_right_ab %}**             | {}-right column if A,B are visible                      | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_right_a %}**              | {}-right column if A is visible                         | col-12 col-md-3               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_right_b %}**              | {}-right column if B is visible                         | col-12 col-md-2 offset-md-1   |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_right_ab_a %}**           | {}-right-a column if A,B are visible                    | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_right_ab_b %}**           | {}-right-b column if A,B are visible                    | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_right_no_center_ab %}**   | {}-right column if right A,B are visible but no center  | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_right_no_center_a %}**    | {}-right column if right A is visible but no center     | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_right_no_center_b %}**    | {}-right column if right B is visible but no center     | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_right_no_center_ab_a %}** | {}-right-a column if A,B are visible but no center      | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_right_no_center_ab_b %}** | {}-right-b column if A,B are visible but no center      | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_abc_a %}**         | {}-bottom-a if A,B,C are visible                        | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_abc_b %}**         | {}-bottom-b if A,B,C are visible                        | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_abc_b %}**         | {}-bottom-c if A,B,C are visible                        | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_ab_a %}**          | {}-bottom-a if A,B are visible                          | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_ab_b %}**          | {}-bottom-b if A,B are visible                          | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_ac_a %}**          | {}-bottom-a if A,C are visible                          | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_ac_c %}**          | {}-bottom-c if A,C are visible                          | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_bc_b %}**          | {}-bottom-a if B,C are visible                          | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_bc_c %}**          | {}-bottom-c if B,C are visible                          | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_bottom_abc_a %}**     | {}-mid-bottom-a if A,B,C are visible                    | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_bottom_abc_b %}**     | {}-mid-bottom-b if A,B,C are visible                    | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_bottom_abc_b %}**     | {}-mid-bottom-c if A,B,C are visible                    | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_bottom_ab_a %}**      | {}-mid-bottom-a if A,B are visible                      | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_bottom_ab_b %}**      | {}-mid-bottom-b if A,B are visible                      | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_bottom_ac_a %}**      | {}-mid-bottom-a if A,C are visible                      | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_bottom_ac_c %}**      | {}-mid-bottom-c if A,C are visible                      | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_bottom_bc_b %}**      | {}-mid-bottom-a if B,C are visible                      | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_mid_bottom_bc_c %}**      | {}-mid-bottom-c if B,C are visible                      | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_abc_a %}**         | {}-bottom-a if A,B,C are visible                        | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_abc_b %}**         | {}-bottom-b if A,B,C are visible                        | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_abc_b %}**         | {}-bottom-c if A,B,C are visible                        | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_ab_a %}**          | {}-bottom-a if A,B are visible                          | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_ab_b %}**          | {}-bottom-b if A,B are visible                          | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_ac_a %}**          | {}-bottom-a if A,C are visible                          | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_ac_c %}**          | {}-bottom-c if A,C are visible                          | col-12 col-md-6               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_bc_b %}**          | {}-bottom-a if B,C are visible                          | col-12 col-md-4               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+
| **{% block {}_bottom_bc_c %}**          | {}-bottom-c if B,C are visible                          | col-12 col-md-8               |
+-----------------------------------------+---------------------------------------------------------+-------------------------------+



