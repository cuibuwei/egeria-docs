<!-- SPDX-License-Identifier: CC-BY-4.0 -->
<!-- Copyright Contributors to the ODPi Egeria project. -->

# Data Governance Roles

Data governance defines how an organization will make best use of data whilst also keeping it safe and managed with a reasonable level of cost and resources. Done well, data governance creates a sense of responsibility for data across every person in an organization plus an appreciation of its value to their work.

Of course, not everyone is responsible for everything.  An individual will have different skills and interests.  Therefore data governance breaks down the work that needs to happen into tasks and groups related tasks into what are called roles.

A role is assigned to a person with a scope.  This makes them responsible for performing the tasks for the role, within the assigned scope.

The scope defines the specific data sets and/or processing that this person must perform the tasks for.

For example, the data stewardship role lists all the tasks related to making a data set fit for purpose, such as correcting errors in it. There may be a data steward assigned to customer records, another for supplier records and another for the financial accounts.

Where data is flowing from system to system, responsibility may be handed off from one data steward to another as the data moves between their scopes of responsibility.

![Hand-off between roles with different scopes](role-scopes.png)

Except in very large enterprises, the data governance roles are typically assigned to individuals in addition to their main role in the organization. Some of these roles are permanently assigned, and other may just be for a project or particular incident.

Roles typically are clustered together defining related types of interactions that need to occur.  The roles below are those most important to data governance.  In some larger organizations, these roles may be staffed by a dedicated team, or further sub-divided into more specific roles.  However, for most organizations, they represent just part of an individual's responsibility.

![Role Summary](role-summary.png)

## Organizational Leadership (general)

Roles that lead in an organization:

??? tip "Manager Role."
    ### Manager Role

    ![Icon](manager-role.png)

    The manager is responsible for coordinating the work of other employees. They are often also responsible for the well-being, recognition and rewards of these employees.

    The manager role if often used as a target for exceptions and approvals of governance actions that occur within their team.

??? tip "Executive Role."
    ### Executive Role
    
    ![Icon](executive-role.png)
    
    The executive is responsible for leading the direction of the organization and speaking on its behalf.  Executives are responsible for the organization's compliance to regulation.
    
    #### Further information
    
    * [Extensions to the executive role for privacy](/practices/data-privacy-pack/role-extensions-for-privacy)
    

## External Parties

Roles that interact with the organization:

??? tip "Supplier Role."
    ### Supplier Role
    
    ![Icon](supplier-role.png)
    
    The supplier is a business partner that provides goods and/or services to the organization.
    
    #### Further information
    
    * [Extensions to the supplier role for privacy](/practices/data-privacy-pack/role-extensions-for-privacy)


??? tip "Customer Role."
    ### Customer Role
    
    ![Icon](customer-role.png)
    
    The customer is responsible for choosing an asset offered by the organization and then setting up the agreements and contracts necessary before the asset can be used.
    
    #### Further information
    
    * [Extensions to the customer role for privacy](/practices/data-privacy-pack/role-extensions-for-privacy/practices)
    
??? tip "Regulator Role."
    ### Regulator Role
    
    ![Icon](regulator-role.png)
    
    The regulator is the named authority for a regulation.  They define the rules, issue guidance on how to be compliant and investigate suspected breaches in the regulation.


## Governance Leadership roles

Roles that occur when governance programs are in place:

??? tip "Governance Officer"
    ### Governance Officer Role
    
    A person who is responsible for leading a governance domain is called a governance officer.
    The governance officer is supported by the [Governance Program OMAS](/concepts/omas/governance-program/overview).
    Below are specific examples of governance officers.

    ??? tip "Data Officer Role."
        ### Data Officer Role
    
        ![Icon](data-officer-role.png)
    
        The data officer is responsible for setting the data strategy and leading the data governance program.
    
        The data officer supports asset owners as they plan the investments in key assets with expertise and research into the latest data capture and processing capabilities.  
    
        #### Further information
    
        * [Extensions to the data officer role for privacy](/practices/data-privacy-pack/role-extensions-for-privacy)
    
    ??? tip "Security Officer Role."
        ### Security Officer Role
    
        ![Icon](security-officer-role.png)
    
        The  security officer is responsible for the protection of data and resources through the management and enforcement of security policies.
    
        #### Further information
    
        * [Extensions to the security officer role for privacy](/practices/data-privacy-pack/role-extensions-for-privacy)
        * The security officer is supported by the [Security Officer OMAS](/concepts/omas/security-officer/overview).


??? tip "Incident Owner Role."
    ### Incident Owner Role
    
    ![Icon](incident-owner-role.png)
    
    The incident owner role is responsible for coordinating the activity and resolution of a specific incident that is detected by the organization.
    
    An example of an incident is a data breach, or a major system outage, or some suspicious activity that could be fraud.
    
    #### Further information
    
    * [Extensions to the incident owner role for privacy](/practices/data-privacy-pack/role-extensions-for-privacy)
    
??? tip "Subject Area Owner Role."    
    ### Subject Area Owner Role
    
    ![Icon](subject-area-owner-role.png)
    
    The subject area owner role is responsible for the definition of a subject area.
    

## Data Privacy

Roles that lead in data privacy discussions:

??? tip "Privacy Officer Role." 
    ### Privacy Officer Role
    
    ![Icon](privacy-officer-role.png)
    
    The privacy officer sets and enforces policies to establish and manage data rights of data subjects base on the expressed intent of the data subjects and in accordance to regulations and company policies.  They are a [Governance Officer](#governance-officer) that leads the privacy governance domain.
    #### Further information
    
    * [Data Privacy Pack](/practices/data-privacy-pack/overview)

??? tip "Data Subject Role."
    ### Data Subject Role
    
    ![Icon](data-subject-role.png)
    
    The data subject is the person that personal data is about.
    
    #### Further information
    
    * [Data Privacy Pack](/practices/data-privacy-pack/overview)
    

## Resource (Data and related IT) Management

Roles involved in the day-to-day use of an organization's resources:

??? tip "Asset Owner Role"
    ### Asset Owner Role
    
    ![Icon](asset-owner-role.png)
    
    A person who is accountable for the proper use and protection of a [Digital Resource](/concepts/digital-resource).  This includes the maintenance of the resource's [Asset](/concepts/asset).
 
    Most employees in an organization will be an owner of at least one resource. The size and importance of the resource in question will determine the level of seniority of the individual that is the asset owner.
    
    The asset owner is responsible for investment decisions related to the resource.  This includes decisions to extend or update the resource and when to dispose of it. They also make choices on investment in security infrastructure and support verses new function.
    
    As such the governance team need to ensure that the asset owner is responsible for planning for the resource as well its functionality.
    
    Assets can be transferred between owners. However, there should never be a time when the asset has no owner.
    
    Some assets are composed, or are dependent on assets owned by different people.  The asset owner of the composite is responsible for ensuring the consumed assets that are used according to their license and service level agreements.
    
    For example, for digital services and systems, the asset owner makes choices relating to the types of data that are collected by their offering, the processing that is performed on data, what data is stored, shared and how long is it kept.
    
    #### Further information
    
    * [Extensions to the asset owner role for privacy](/practices/data-privacy-pack/role-extensions-for-privacy)
    * The Asset Owner is supported by the [Asset Owner OMAS](/concepts/omas/asset-owner/overview).

??? tip "Asset Consumer Role."
    ### Asset Consumer Role
    
    ![Icon](asset-consumer-role.png)
    
    The asset consumer is an individual that consumes an asset.  This may be a data set or a digital service, or both.
    
    #### Further information
    
    * [Extensions to the asset consumer role for privacy](/practices/data-privacy-pack/role-extensions-for-privacy)
    

??? tip "Data Steward Role."
    ### Data Steward Role
    
    ![Icon](data-steward-role.png)
    
    The data steward is responsible for ensuring data is fit for purpose. This may involve correcting errors in the data, improving its metadata  description and responding to questions about the data.

??? tip "Data Custodian Role."
    ### Data Custodian Role
    
    ![Icon](data-custodian-role.png)
    
    The data custodian is responsible for ensuring data from a third party is managed and used according to its licence.
    

## Digital Services

Roles for building and using digital services:

??? tip "Advocate Role."
    ### Advocate Role
    
    ![Icon](advocate-role.png)
    
    The advocate is responsible for the selling the value of an asset to potential asset consumers.  This may be an internal role, or one that involves contracts and other agreements before the asset can be used.
    
    #### Further information
    
    * [Extensions to the advocate role for privacy](/practices/data-privacy-pack/role-extensions-for-privacy)
    

??? tip "Architect Role."
    ### Architect Role
    
    ![Icon](architect-role.png)
        
    The architect is responsible for the structural design of digital systems ensuring it is fit for purpose, resilient, secure and cost effective.
    
    Typically, there is an architect responsible for the design of a digital service.  This covers the interfaces, data and infrastructure.
    
    #### Architect Specialities
    
    As organizations and the number of IT systems grows, specializations in architecture emerge.  For example,
    
    * *Enterprise Architect* - There are architects that take an enterprise view - looking at how the
    systems and organization around then are supporting the organization's needs.
    These are called enterprise architects.
    
    * *Information Architect* -  There are architects that focus on the structure and flow of information around the organization.  They are called information architects.
    
    These architects then complement the architects assigned to digital services.
    
    #### Further information
    
    * [Extensions to the architect role for privacy](/practices/data-privacy-pack/role-extensions-for-privacy)
    

??? tip "Project Manager Role."
    ### Project Manager Role
    
    ![Icon](project-lead-role.png)

    A project manager is a person who leads a [project](/concepts/project).  They are responsible for the delivery of a project on time and within budget.

    #### Further information

    * The project manager role is supported by the [Project Management OMAS](/concepts/omas/project-management/overview).
    

??? tip "Developer Role."
    <!-- SPDX-License-Identifier: CC-BY-4.0 -->
    <!-- Copyright Contributors to the ODPi Egeria project. -->
    
    ### Developer Role
    
    ![Icon](developer-role.png)
    
    The developer is responsible for designing, coding and testing software.
    
    #### Further information
    
    * [Extensions to the developer role for privacy](/practices/data-privacy-pack/role-extensions-for-privacy)
    

??? tip "Systems Administrator Role."
    ### Systems Administrator Role

    ![Icon](systems-administrator-role.png)

    The systems administrator manages the IT infrastructure of an organization

    #### Further information

    * [Extensions to the systems administrator role for privacy](/practices/data-privacy-pack/role-extensions-for-privacy)


??? tip "Team Leader"
    ### Team Leader
    The leader of a [team](/concepts/organization/#team).

??? tip "Team Member"
    ### Team Member
    A member of a [team](/concepts/organization/#team).





--8<-- "snippets/abbr.md"