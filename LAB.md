Lorem Ipsum Master Detail
===

## Code Wars Challenge

Complete [today's Kata.](https://www.codewars.com/kata/my-head-is-at-the-wrong-end)

## Lab

Create a ipsum viewer/editor that:

* Displays a lists of ipsum's and when an ipsum is clicked, it populates a detail view with full information.
* The Detail has an edit button that toggles to a form and allows editing. Includes sample text in html
* Add an input form and button for a title that adds a new ipsum and makes it the selected item. 
(BONUS: Can you get the detail to switch to edit mode?)

## Components

Your app components should be structured as follows:

```
App
  Header
  Ipsums
    AddIpsum
    IpsumList
        IpsumItem
    Ipsum
        IpsumDetail
        IpsumForm
```

## Component Details

* `App` 
    * Top Level Component
* `Header`
    * Logo and Title
* `Ipsums`
    * owns the "ipsum list" state (data, initial import of `data.js`)
        * adds and updates need to be done in this component!
    * owns the "selected" state (initially `null`)
    * passes `IpsumList` list of `ipsums` and a callback function, `onSelect`
    * passes `AddIpsum` a callback function `onAdd`
    * passes `Ipsum` the `ipsum` (it's `selected` data) and an `onUpdate` callback
* `IpsumList`
    * calls the passed `onSelect` when an ipsum is selected, _passing the corresponding object_ to the `onSelect` function
    * show name and category
* `AddIpsum`
    * Form for updating an `ipsum`
    * Has own state for managing data being updated (copy in `created` lifecycle)
    * Receives `animal`, plus `onUpdate` and `onCancel` props 
* `Ipsum`
    * Container for switching between viewer and editor (form)
    * Has "editing" state (data)
    * If `ipsum` is `null` displays message to make a selection
    * Passes IpsumDetail the `ipsum` for display
    * Passes IpsumForm the `ipsum` to edit, a `onCancel` callback function, and the `onUpdate` from `Ipsums`
* `IpsumDetail`
    * gets passed the `ipsum`
* `IpsumForm`
    * gets passed the `ipsum` and `onUpdate` callback
    * copies prop to data on `create`
    * calls `onUpdate` with new data on submit
    * calls `onCancel` when cancel button clicked
    
  

## Rubric

* Follows prescribed project and component structure and organization **1pt**
* Ipsum list **1pt**
* Shows selected detail view **2pts**
* Switch edit/view modes (including cancel and post-update) **1pt**
* Edit Form **1pt**
* Updates Ipsum **1pt**
* Add Ipsum **1pt**
* Integration: Feature/Functionality correct/works **2pts**
