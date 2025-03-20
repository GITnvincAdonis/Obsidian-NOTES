---
creation date: <% tp.file.creation_date() %>
---

> [!Quote] States of a package

    state :en_route_to_warehouse, initial: true
    state :delivered_by_courier
    state :package_at_warehouse
    state :in_transit_to_guyana
    state :landed_in_guyana
    state :available_for_pickup
    state :delivered



> [!Quote] States of a Shipment

    state :booked, initial: true
    state :in_transit
    state :landed
    state :available


> [!NOTE] Changes
> 1. 'Shipped_on' -> 'flight_at' name change
> 2. Add state between package_at_warehouse and in transit_to_guyana:
>    -> Added_to_shipment
>    When a package is added to a shipment on our system, an event must be fired, automatically setting the packages state to this
> 3. Add drop-down to shipment to change states
> 4. When a shipment is in transit, all attached packages should also be in transit
> 5. When a shipment lands, all attached packages should also be "landed_in_guyana"
> 6. Packages from state "landed_in_guyana" and onward must be updated manually. A dropdown must be provided on packages. When a package is of a state before landed_in_guyana, disable the dropdown.


> [!Danger] When a package is
> 1. in transit to guyana || landed in guyana:
>    related to the attached shipment state
> 2. Avaliable_for_pickup || delivered"
>    Set manually on the edit page of a package on the admin side

Link to original: [[2025-03-18 notes on shoponline app]]