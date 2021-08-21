Lists components are simply different layout types for displaying your collection data in the most appropriate way. You can display your collections as Table, Kanban, Map, Calendar, Gallery, and Timeline. For example, you get a collection of tabular data from your resources - you can display it as a table.

## Adding list component

You can add any component of the list to the page by simply drag-and-drop it:

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_yjFUQOb0qtulqpQI%2F-MG_zuUGhU6jkaossH19%2FGIF92.gif?alt=media&token=ad4cb92b-72ce-4b6a-90fa-7aaf1e3e01ef)

## Layouts

Once you have added a list component to a page, you can add additional display layouts to that component. You can switch between layouts within the same component.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_yjFUQOb0qtulqpQI%2F-MG_zYE_NUmkMbRMVHtp%2FGIF91.gif?alt=media&token=abed70ed-8d30-421b-8ce5-6dc653bec65c)

## Columns

You can customize columns: rearrange, change field type, show/hide.

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_yjFUQOb0qtulqpQI%2F-MGa-WWq4C3HqXhBtAZu%2FGIF93.gif?alt=media&token=cc8649ba-d72b-4823-b35c-e658075f2af5)

## Pagination

You can limit the number of records displayed on a page in the table. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MFcGyQByFg7nDT_BI2r%2F-MFcHmFQem0DEeqcgaHI%2FGIF.gif?alt=media&token=e54e2513-fed9-4327-8b52-e78fbdfd6966)

## Search

For example, If you need to search for customers by a specific name or field. Activate a search and specify the data: resource and list's collection. 

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_yjFUQOb0qtulqpQI%2F-MGa-zIjA58JdBtJAr2-%2FGIF94.gif?alt=media&token=74af0d37-46e3-45f7-ac92-20be7c2600d3)

## Actions

You can also add a button that performs a specific action with the List, such as exporting data, send an email, etc. 

There are 2 types of actions on the list component:

* **Header Actions**. Apply action for all records on the list, such as Export Data.
* **Record Actions**. Perform action for selected fields or specify the action that triggers when the record clicked.

## Selection Action

For example, you want to delete a specific customer, you can add a button that will delete record.

1. Go to the Component Settings then click Record actions

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_yjFUQOb0qtulqpQI%2F-MGa2HHIKAvCquEC7QOA%2FGIF96.gif?alt=media&token=bc4ee65a-8470-427c-9eb4-8440e30ecb1f)

2. Click Add Action when record selected then select`Run Operation` type

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_yjFUQOb0qtulqpQI%2F-MGa33G10CJ5Jk4ot9ea%2FGIF97.gif?alt=media&token=821ebd81-47cd-46c0-bb95-eba27ec88926)

3. Select your resource \(PostgreSQL database in our case\) then select operation `collection name` - `delete` \(randomuser - Delete\)

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_yjFUQOb0qtulqpQI%2F-MGa3pCAm1tTO3tSw9uM%2FGIF98.gif?alt=media&token=4548837f-defc-4deb-a894-3a842fe9dada)

4. Specify `id` parameter to delete record you want

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_yjFUQOb0qtulqpQI%2F-MGa5X-nhszF2wPAQw3K%2FGIF99.gif?alt=media&token=9a4eb5ed-63b3-4ac9-8203-f275fc2c8845)

## Header Action

For example, if you want to add a new customer you need to set header action:

1. Go to the Component Settings then click Header

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_yjFUQOb0qtulqpQI%2F-MGa6ICvRz8ivsSpue_u%2FGIF100.gif?alt=media&token=01f323c4-0349-488d-ad70-b7cf2a3d76d5)

2. Click Add Action then choose action type as `Navigate to Page`

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_yjFUQOb0qtulqpQI%2F-MGa6qmTE5SctfdMP4sC%2FGIF101.gif?alt=media&token=49e15e53-e9ac-4549-bc2b-7f177f1dc7cd)

3. Select `Collection - Create` link in the dropdown list then choose your collection

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_yjFUQOb0qtulqpQI%2F-MGa7qahwWYsAIpqAI_M%2FGIF102.gif?alt=media&token=4e819175-fba1-4009-80a4-7ac4465b9f9f)

4. Run operation to create new user

![](https://gblobscdn.gitbook.com/assets%2F-LQ08RFAKZvFADEiXKFy%2F-MG_yjFUQOb0qtulqpQI%2F-MGa8Fv2mNIbqcEorQRQ%2FGIF103.gif?alt=media&token=6ca243ed-aea6-417b-91ef-933dbfc64ed0)

See our documentation for a detailed configuration of actions.

{% page-ref page="user-guide/data/actions" %}

