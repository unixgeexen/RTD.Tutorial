Welcome to Lumache's documentation!
===================================

**Lumache** (/lu'make/) is a Python library for cooks and food lovers
that creates recipes mixing random ingredients.
It pulls data from the `Open Food Facts database <https://world.openfoodfacts.org/>`_
and offers a *simple* and *intuitive* API.

Check out the :doc:`usage` section for further information, including
how to :ref:`installation` the project.

.. note::

   This project is under active development.
   
   Lumache has its documentation hosted on Read the Docs.
   
uml
==================
@startuml
title Activity diagram\n



start



if (Receive Order) then (accepted)
:Fill Order;
:Order Accepted;


fork
:Ship Order;

fork again
:Send Invoice;

:Receive Payment;

end fork

else (Order Rejected)
:Send Order Declined Notice;

endif


:Close Order;

end

!include ../../plantuml-styles/ae-copyright-footer.txt
@enduml


Contents
--------

.. toctree::

   usage
   api
