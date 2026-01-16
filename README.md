# Contoso Power Apps Project

Developed a **canvas app**, **model-driven** app, Power Automate flow, and Power BI report for Microsoft's Power Up Challenge.

## Repository Structure

This repository contains the **unpacked** export of the Contoso Parking Challenge solution (version 1.0.0.3). Unpacking converts the binary .zip into human-readable files for better version control and review.

- **ContosoParkingChallenge_1_0_0_3/** — Root folder of the unpacked solution
  - **[customizations.xml](ContosoParkingChallenge_1_0_0_3/customizations.xml)**  
    All Dataverse customizations (tables, forms, views, **model-driven app** definition, sitemap, security roles, etc.), inlcuding the data for the model-driven app (see "Model-Driven App: Parking Review Model App" section below).
  - **`CanvasApps/`**  
    Canvas app files (e.g., .msapp source, background images, identity JSON)
  - **`Formulas/`**  
    YAML files defining calculated columns/fields (formulas, rollups, calculated values) on Dataverse tables
  - **`Workflows/`**  
    XML files for classic workflows (legacy processes/business rules)
  - **`[Content_Types].xml`**  
    Required manifest file (Office Open XML content types) needed for repacking the solution correctly
  - **`solution.xml`**  
    High-level solution metadata (publisher, version, description, etc.)

**Outside the root folder:**
- **`PowerUp Parking Challenge Report.pbix`**  
  Power BI report files/export for the parking challenge (likely .pbix or exported artifacts)
-**`Contoso Canvas App Screenshot 1.png`**, **`Contoso Canvas App Screenshot 2.png`**, **`Contoso Model Driven App Screenshot 1.png`**, and **`Contoso Model Driven App Screenshot 2.png`** are screenshots of the canvas app and model-driven app, respectively.

## Model-Driven App: Parking Review Model App

The model-driven app ("Parking Review Model App") allows parking admins to review and manage parking requests and inspections.

**Note**: In Power Platform solution exports, model-driven apps are embedded in `customizations.xml` (not in a separate folder like canvas apps).

### Core App Definition
App properties, included components (tables like VehicleInfos), security roles, etc.  
→ **[View lines 5367–5401](ContosoParkingChallenge_1_0_0_3/customizations.xml?plain=1#L5367-L5401)**  
(Look for `<AppModules>` → `<AppModule>` with `<UniqueName>hq_ParkingReviewModelApp</UniqueName>`)

### Sitemap / Navigation (Left Menu)
Defines the menu structure (Home, VehicleInfos, ParkingRequestInfos, ParkingInspectionInfos, etc.)  
→ **[View lines 5343–5366](ContosoParkingChallenge_1_0_0_3/customizations.xml?plain=1#L5343-L5366)**  
(Look for `<AppModuleSiteMaps>` → `<AppModuleSiteMap>` with `<SiteMapUniqueName>hq_ParkingReviewModelApp</SiteMapUniqueName>`)

**To view or edit the app:**
- Import the full solution back into the Power Apps maker portal (make.powerapps.com)  
- Or repack into a .zip using Power Platform CLI:  
  `pac solution pack --folder ContosoParkingChallenge_1_0_0_3 --zipFile new-solution.zip`

Questions? Feel free to open an issue!
