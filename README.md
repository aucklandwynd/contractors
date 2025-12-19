# [Contractors](https://aucklandwynd.github.io/contractors/)
A community-curated directory of recommended contractors, organized by service type. 

## Adding New Contractors
To add a new contractor, edit the `data/contractors.yml` file and add a new entry.

### 1. Create a New Git Branch
Navigate to https://github.com/aucklandwynd/contractors/branches and select **New branch**. Enter a branch name following the pattern `contractors/new-contractor-name` where `new-contractor-name` is the name of the contractor being added. 

Make sure that the **Source** option is `prod`. 

For example to add "Smith Electric" the branch name will be `contractors/smith-electric`.

### 2. Add Contractor Details
Return to the repository summary page, https://github.com/aucklandwynd/contractors, and select your new branch from the drop-down on the left of the page under the "contractors" heading. By default this drop-down will show the name `prod`.

You should now be at `https://github.com/aucklandwynd/contractors/tree/contractors/new-contractor-name`.

Navigate to the `data` directory and then select `contractors.yml`. 

Press **Edit this file** button, the pencil-icon button on the right of the screen, and add the contractor's details. The contractors shoulds be listed alphabetically.

```yaml
- name: "Contractor Name"
  contact: "email@example.com"
  phone: "555-0000"
  website: "https://example.com"  # Leave empty ("") if no website
  services:
    - service1
    - service2
  recommended_by:
    - "Person Name"
  notes: "Any additional notes"
```

**!!** These details will be posted publically and accessible by **anyone** online. Make sure that you are not publishing any information that either the contractor or yourself are not willing to share publically.

#### Available Service Categories
Current services include:
- electrical
- handyman
- joinery
- landscaping
- painting
- plumbing
- heating
- mvhr

Feel free to add new service categories as needed, editing the `README.md` file to capture those here.

### 3. Commit your Changes
Once you have added the contractor details to `contractors.yml` push the **Commit changes** button and add a brief description of the change you have made.

### 4. Create a Pull Request

1. Navigate to the original repository on GitHub, https://github.com/aucklandwynd/contractors.
2. Click the **Pull Requests** tab
3. Click the **New Pull Request** button
5. Select your `contractors/new-contractor-name` branch as the source
6. Select test as the base branch
7. Fill out the Pull Request template:
    * A clear title
    * Description of your changes
    * Any related issue numbers
8. Submit the pull request
9. Wait for Review

A maintainer will review your pull request. They may request changes or ask questions. Once approved, your changes will be merged into the test branch and shortly therafter be reflected on the live webpage.