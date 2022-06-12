## A brief history of containers

The idea of what we now call container technology first appeared in 2000 as **FreeBSD jails**, a technology that allows the *partitioning of a FreeBSD system into multiple subsystems, or jails*. Jails were developed as safe environments that a system administrator could share with multiple users inside or outside of an organization.

In 2001, an implementation of an *isolated environment* made its way into Linux, by way of Jacques Gélinas’ **VServer project**. Once this foundation was set for multiple controlled userspaces in Linux, pieces began to fall into place to form what is today’s Linux container.

Very quickly, more technologies combined to make this isolated approach a reality. **Control groups (cgroups)** is a kernel feature that controls and limits resource usage for a process or groups of processes. And **systemd**, an initialization system that sets up the userspace and manages their processes, is used by cgroups to provide greater control over these isolated processes. Both of these technologies, while adding overall control for Linux, were the framework for how environments could be successful in staying separated.

## Enter Docker

In 2008, **Docker** came onto the scene (by way of dotCloud) with their eponymous(同名) container technology. The docker technology **added a lot of new concepts and tools**—a simple command line interface for running and building new layered images, a server daemon, a library of pre-built container images, and the concept of a registry server. Combined, these technologies allowed users to quickly build new layered containers and easily share them with others.

**There are 3 major standards to ensure interoperability of container technologies—the OCI Image, Distribution, and Runtime specifications.** Combined these specifications allow community projects, commercial products, and cloud providers to build interoperable container technologies (think pushing your custom built images into a cloud provider’s registry server - you need that to work). Today Red Hat and Docker, among many others, are members of the Open Container Initiative (OCI)—are enabling an open, industry standardization of container technologies.