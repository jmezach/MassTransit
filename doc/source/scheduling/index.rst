Scheduling messages
===================

.. attention:: **This page is obsolete!**

   New documentation is located at http://masstransit-project.com/MassTransit.

   The latest version of this page can be found here_.

.. _here: http://masstransit-project.com/MassTransit/usage/scheduling/

Time is important, especially in distributed applications. Quartz.NET is an excellent scheduler, and is used
in many applications to schedule jobs in a variety of ways.

MassTransit uses Quartz.NET to schedule messages, making it possible to build complex time-based workflows.
Several extensions are available to message consumers, as well as middleware for using message scheduling.

In a production system, Quartz.NET is run as a service with multiple instances active for high availability
and load balancing. Quartz can use any SQL database to coordinate scheduled jobs across servers, making it
suitable for this type of use.

There is a standalone MassTransit service, MassTransit.QuartzService, which can be installed and used on
servers for this purpose. It is configured via the ``app.config`` file and is a good example of how to build
a standalone MassTransit service.

.. note::

    This service will likely move to be hosted in the new MassTransit.Host, making the service
    logic reusable across any message transport.


.. toctree::

    scheduling_api.rst
    in_memory.rst
    redeliver.rst
    servicebusscheduler.rst

