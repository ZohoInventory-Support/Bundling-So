# Bundling-Sales-order
# Auto-create-packages-for-Sales-Orders

Creates Bundle for composite item present in the sales order based on the quantity mentioned in the sales order.

# Steps
# 1. Create Custom function

Settings > Automations > Custom Functions > New Custom Function 

Module: Sales Order

Copy and paste the script Bundling-Sales order

Create connection for Zoho Inventory - zom

# 2. Create connection 
Click on the "Connections" button above the Deluge script section on the top right side.

It will open up Connections Section. Click on "+Add connection".

Scroll down Pick Your Service section and click on Zoho Inventory.

Provide the Connection Name as zom and Give Connection Link name as zom as well.

Also Uncheck the box "Use credentials of Login User".

Under Scopes select ZohoInventory.FullAccess.all

Click Create and Connect, it redirects to a pop up window. Click on Proceed.

Click Accept in the next window and Connection created successfully message will be shown.


# 3. Create workflow

Settings > Automations > Workflow Rules > New Workflow Rule

Module : Sales Order

Workflow Type : Event Based

When a Sales Order is : Created or Edited and execute the workflow when : When any field is updated.

Filter the trigger When a Sales order Status is: Open

Just once or everytime? - Just Once.

Choose the appropriate custom function in the Action.

Save the workflow. On each SO creation workflow automatically creates the bundle.
