# CNS2027 abstract-submission web app

The public abstract form is implemented as a Google Apps Script web app. The currently deployed project remains the production endpoint until a new Apps Script version is deployed.

## Dynamic author revision

This revision replaces the six fixed author rows with a dynamic author list:

- the presenting-author row is required and cannot be removed;
- coauthors are added with **Add author** and removed individually;
- the default maximum is 30 authors;
- the limit is controlled by `Settings!MAX_AUTHORS` in the administration spreadsheet;
- the complete author list remains stored in the existing `Authors and primary affiliations` cell, so the Submissions table does not require new columns.

## Prepared source files

The updated source is stored in the symposium Google Drive folder as:

- `CNS2027_Code_Dynamic_Authors.gs`
- `CNS2027_Index_Dynamic_Authors.html`
- `CNS2027_Dynamic_Authors_Source.zip`
- `CNS2027_Dynamic_Authors_Deployment_Guide.md`

## Publish while preserving the current public URL

1. Open the existing Apps Script project.
2. Replace the contents of `Code.gs` with the prepared `.gs` file.
3. Replace the contents of `Index.html` with the prepared `.html` file.
4. Select **Deploy > Manage deployments**.
5. Edit the existing web-app deployment, select **New version**, and deploy.
6. Test adding, removing, and submitting multiple authors.

Updating the existing deployment preserves the current `/exec` URL used by the symposium website.
