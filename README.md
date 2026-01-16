# Contoso-Power-Apps-Project
Developed a canvas app, **model-driven** app, power automate flow, and power BI report for Microsoft's Power Up Challenge.

## Repository Structure
- **ContosoParkingChallenge_1_0_0_3/**: Unpacked solution export (full source files)
  - `customizations.xml`**(ContosoParkingChallenge_1_0_0_3/customizations.xml)**: All Dataverse customizations, including the model-driven app
  - `CanvasApps`: Canvas app files (e.g., .msapp, background images)
    
## Model-Driven App: Parking Review Model App Details:
The model-driven app ("Parking Review Model App") allows parking admins to review and manage parking requests and inspections.

**Note**: In Power Platform solution exports, model-driven apps are embedded in `customizations.xml` (not in a separate folder like the canvas app).

**Core Model-Driven App definition** 
The definition for the model-driven app (such as app properties, components, and roles) can be found in the 'customizations.xml' file inside of the `ContosoParkingChallenge_1_0_0_3` folder. The data for the Model-Driven app starts with container "<AppModules>" and can be found here: [customizations.xml (Model-Driven App definition, lines 5367–5401)](ContosoParkingChallenge_1_0_0_3/customizations.xml?plain=1#L5367-L5401)

**Sitemap/Navigation** 
The code for the sitemap of this model-driven app starts with the container "<AppModuleSiteMaps>" here: [customizations.xml (Model-Driven App definition, lines 5343–5366)](ContosoParkingChallenge_1_0_0_3/customizations.xml?plain=1#L5343-L5366)

To view/edit: Import the solution back into Power Apps maker portal or repack with PAC CLI (`pac solution pack ...`).

Questions? Feel free to open an issue!
