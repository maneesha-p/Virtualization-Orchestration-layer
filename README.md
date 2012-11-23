Virtualization-Orchestration-layer
==============================
An orchestration suite provides a number of services and allows the users access to these in
the form of service endpoints.A cloud orchestration suite acts as  a transparency layer. It combines all the
resources and shows them as one(a cloud) to the users. Users can demand variable resources
from the orchestration layer and pay as per the usage.

Lets take a closer look at each step taken in the orchestration layer.

●Resource Discovery: Recourse Discovery refers to the component which search/discovers the available
hardware recourses in the given setup.
● Request Verification - A web server(apache or your own code) will be listening on port
80 for incoming requests. Once the request is received, based on the URL, the required
action will be decided.
● Scheduler - At this step The scheduler’s job is to decide which hosts are suitable for spawning these VMs.
● Order VM Creation - Once the hosts are decided, libvirt is used to contact the hypervisors.
The benefit of using libvirt is the ease of controlling various types of hypervisors using the same code.
● Status Reporting to User - The user must be notified about the status (success/failure) of
the request.