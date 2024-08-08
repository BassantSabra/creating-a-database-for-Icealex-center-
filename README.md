# README: ICEALEX_Startup Project Database 

## Entities and Attributes

### 1. **Startups**
   - **Attributes:**
     - `code`: A unique identifier for each startup.
     - `FounderName`: Name of the founder of the startup.
     - `Co-FounderName`: Name of the co-founder, if any.
     - `email`: Contact email of the startup.
     - `PhoneNumber`: Contact phone number of the startup.
     - `Sector`: The sector or industry in which the startup operates.
     - `Governorate`: The regional location of the startup.
     - `Legal Registration`: Legal status or registration details of the startup.
     - `CurrentStage`: Current stage of the startup (e.g., ideation, seed, growth).
     - `NoTeamMembers`: Number of team members involved in the startup.
     - `StartupBrief`: A brief description of the startup.
     - `pitchDeck`: A link or reference to the startup's pitch deck.
     - `Led_gender`: Gender of the leader or founder.
   
   - **Relations:**
     - **Funding**: A startup can have multiple funding records.
     - **Projects**: A startup can initiate or join multiple projects.
     - **Stakeholders**: A startup may have multiple stakeholders.
     - **External Partnerships**: A startup can have multiple external partnerships.

### 2. **Funding**
   - **Attributes:**
     - `FundingID`: A unique identifier for each funding record.
     - `ExternalFund Name`: Name of the external fund.
     - `ExternalFund Amount`: The amount of funding provided.
     - `ExternalFund Currency`: The currency in which the funding is provided.
   
   - **Relations:**
     - A startup can **have** one or more funding records.

### 3. **Projects**
   - **Attributes:**
     - `ProjectID`: A unique identifier for each project.
     - `ProjectName`: Name of the project.
     - `Project_year`: The year the project was initiated or joined.
   
   - **Relations:**
     - A startup can **Join** one or more projects.

### 4. **Stakeholders**
   - **Attributes:**
     - `stakeholder_ID`: A unique identifier for each stakeholder.
     - `Stakeholder`: The name or description of the stakeholder.
   
   - **Relations:**
     - A startup can **have** one or more stakeholders.

### 5. **External Partnership**
   - **Attributes:**
     - `partnership_ID`: A unique identifier for each partnership.
     - `partnership_name`: The name or description of the external partnership.
   
   - **Relations:**
     - A startup can **have** one or more external partnerships.

## Relationships Between Entities

### Startups and Funding
- A one-to-many relationship exists between `Startups` and `Funding`, meaning that a single startup can receive multiple funding instances. This is represented by the relationship "have" between `startups` and `Funding`.

### Startups and Projects
- A many-to-many relationship exists between `Startups` and `Projects`, indicating that startups can participate in multiple projects and a project can involve multiple startups. This is represented by the associative entity "Join" between `startups` and `projects`.

### Startups and Stakeholders
- A one-to-many relationship exists between `Startups` and `Stakeholders`, meaning that a single startup can have multiple stakeholders. This is represented by the relationship "have" between `startups` and `stakeholder`.

### Startups and External Partnerships
- A one-to-many relationship exists between `Startups` and `External Partnership`, indicating that a single startup can have multiple external partnerships. This is represented by the relationship "have" between `startups` and `External Partnership`.

## Usage
This database schema is ideal for managing data related to startups, tracking their funding sources, managing projects, recording stakeholder information, and maintaining records of external partnerships. The relationships are structured to ensure that the database can scale as more startups, projects, funding, and partnerships are added.

By organizing the data in this manner, it is easier to query and analyze the involvement of startups in various projects, their funding history, and the external partnerships that support their growth.
