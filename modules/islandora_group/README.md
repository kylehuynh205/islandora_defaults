# Default configuration for Islandora Group module

This module contain default configuration for [Islandora Group module](https://github.com/digitalutsc/islandora-group).

## How to setup 

Follow [this document](https://docs.google.com/document/d/1fy2KyjlURBpseLbwqspD3Yv5iFPpv1HQF_qKClV7zso/edit?usp=sharing) (**starting from step 5** because this module already takes care of step 1-4) for setting up testing evironment for the access control:

### Collection Based Access Control Setup:
 1. Create the following groups: 
      - Restricted Collection 1
      - Restricted Collection 2
      - Restricted Collection 3
     
  2. In each group, setup: 
  - **Group _Restricted Collection 1_** with the following group roles:
     - Anonymous cannot view. 
     - Collection Manager: can create, edit, view
     - General User (ie. cataloguer) can view.
     - Administrator: can create, edit, view, and delete.

  - **Group _Restricted Collection 2_** with the following group roles:
     - Anonymous has the ability to view.
     - Collection Manager: can create, edit, view
     - General User (ie. cataloguer): can edit and view
     - Administrator: can create, edit, view, and delete.

  - **Group _Restricted Collection 3_** with the following group roles: 
     - Anonymous cannot view. 
     - Collection Manager: can create, edit, view and delete.
     - General User (ie. cataloguer): cannot view
     - Administrator: can create, edit, view, and delete.
     
### Role Based Access Control Setup
  1. Create the following groups: 
      - Anonymous
      - Collection Manager 1
      - Collection Manager 2
      - Authenticated User
      - Admin

  2. In each group, configure the group permission `Group Permissions` tab to override the default Group Type group permission if applicable,
 
  - **Group _Anonymous_**
    -  set Anonymous Drupal Role can View node and media
    
  - **Group _Collection Manager 1_**
    -  View, Edit, Create for Nodes and Medias
    
  - **Group _Collection Manager 2_**
    - View, Edit, Create, Delete for Nodes and Medias
    
  - **Group _Authenticated User_**
    - View for Nodes and Medias
    
  - **Group _Admin_**: CRUD all items


