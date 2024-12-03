---
layout: pattern
title: Help users to... Update prefilled information
draft: true
permalink: /patterns/help-users-to/update-prefilled-information
sub-section: [help-users-to]
intro-text: Follow this pattern to help users update prefilled information in an application.
research-title: Help users update prefilled information
figma-link: https://www.figma.com/design/1z3bAkQl4uR1IvAxmtyqZi/AE-Design-Patterns---Update-Prefill?node-id=4013-14358&t=GYX9RT423zMZrhat-1
status: use-with-caution-available
anchors:
  - anchor: Usage
  - anchor: How to design and build
  - anchor: Examples
  - anchor: Code usage
  - anchor: Content considerations
  - anchor: Research findings
---


## Usage
### When to use this pattern
- **When you prefill the user’s data into an application, like a form.** This pattern helps users understand how they can edit their prefilled information, especially sensitive information that requires calling a VA center to change. Additionally, this pattern informs users where their changes will be saved—either to the form, or to their form and VA.gov profile. See the related ["Help users to... Know when their information is prefilled"](https://design.va.gov/patterns/help-users-to/know-when-their-information-is-prefilled) pattern for guidance on how to display the prefilled information.

#### Design Principals
- **Visibility of system status.** This pattern demonstrates the usability principle of communicating the current state to help users feel in control and take appropriate action. [Learn more about Visibility of system status](https://www.nngroup.com/articles/visibility-system-status/).
- **User control and freedom.** This pattern also gives users control over their own information. [Learn more about User Control and Freedom](https://www.nngroup.com/articles/user-control-and-freedom/).

### When not to use this pattern
- **When prefilled information is not used.** If the form does not include prefilled information, there is no need to inform users how to update their prefilled information.

### When to use caution
- **When data that cannot be changed online.** This pattern accounts for cases in which the user needs to call VA to change their information, such as changing their name and social security number. Form developers should confirm that the phone number listed is the correct number for Veterans to call and update this specific information. If there are cases where information cannot be changed, even by calling VA, this should be explained to the user.

## How to design and build
### Anatomy or layout details
This pattern involves these types of pages found in VA.gov forms:

- **Personal information page:** Usually the first page of a form after the user signs in. Has personal details that typically cannot be edited online, like name, date of birth, Social Security number, etc.
- **Prefill check page:** Any page of a form that displays prefilled information users can edit within the form.

See the related ["Help users to... Know when their information is prefilled"](https://design.va.gov/patterns/help-users-to/know-when-their-information-is-prefilled) pattern for other pages related to prefilled content.

#### Personal information page
_(coming soon - in the interim, view this [Figma file](https://www.figma.com/design/1z3bAkQl4uR1IvAxmtyqZi/AE-Design-Patterns---Update-Prefill?node-id=3-127&t=GYX9RT423zMZrhat-1))_

#### Prefill check page
_(coming soon - in the interim, view this [Figma file](https://www.figma.com/design/1z3bAkQl4uR1IvAxmtyqZi/AE-Design-Patterns---Update-Prefill?node-id=3-127&t=GYX9RT423zMZrhat-1))_

### How this pattern works

#### Communicate information that cannot be edited
This pattern communicates information that cannot be edited with:
- **Uneditable prefilled information displayed in a gray card.** Prefilled information (such as legal name, date of birth, and Social Security number) is displayed in a card component. This is often one of the first pages in a form.
- **Directions for updating uneditable information.** Inforational text is added under the card that has the bolded word “note” and directions to update this information offline.

#### Communicate information that can be edited
This pattern communicates information that can be edited with:
- **Editable prefilled information displayed in a white card with an edit link.** Prefilled information that is editable is displayed in a card component with a link to edit the information. This information may include contact information, such as phone, email, or mailing address.

#### Communicate where changes will save
- **In most cases, save changes to the VA.gov profile.** In [user research](https://github.com/department-of-veterans-affairs/va.gov-team/tree/master/products/authenticated-patterns/Design%20and%20Research/2024-09%20Research%20Initiative%202%20-%20Update%20Prefill), most users indicated that they want changes they make to their information to update the information stored on their VA.gov profile. On the edit page, display an informational alert informing users that these changes will impact their profile information.

#### Where needed, give users the choice of where to save
- **In some cases, users want to choose where to save their information.** This is especially relevant for information that may change over time, like mailing address. This might be especially relevant in cases where forms or perscriptions will be sent to users within the coming days or weeks. In this case, on the edit page, do not display the informational alert informing them where their changes will save--instead, display a required radio button below the fields asking them if they also want to update this information in their VA.gov profile.

#### Display success alerts when information has been saved
- **Inform users where the changes were saved.** Display a success alert informing users "We've made these changes to this form and your VA.gov profile" or "We've made these changes to only this form.” Use a standard alert within the form steps. Use a slim alert if the user made changes from the final review page.

### Components used in this pattern
- [Alert](https://design.va.gov/components/alert/)
- [Radio button](https://design.va.gov/components/form/radio-button)
- [Additional info](https://design.va.gov/components/additional-info)

### Page templates available for this pattern

List of links to page templates or layouts used to build any pages for this pattern.

## Examples

Informational text before a set of uneditable information, informing the user that they need to call VA to update this information
_(coming soon - in the interim, view this [Figma file](https://www.figma.com/design/1z3bAkQl4uR1IvAxmtyqZi/AE-Design-Patterns---Update-Prefill?node-id=3-127&t=GYX9RT423zMZrhat-1))_

Success alert informing user that their change was successfully made to the form and to their VA.gov profile

<img width="251" alt="Alert - form and profile" src="https://github.com/user-attachments/assets/ef433269-06d3-43b7-b4f3-930241893298">

A success alert informating users their change has been saved to the form and their VA.gov profile. If the change was only saved to the form, the alert should read "We've made these changes to only this form."

<img width="290" alt="Success alert - saved to form and profile" src="https://github.com/user-attachments/assets/88770c2a-accb-469b-a5ba-4ed1198db056">

A radio button asking users if they want to save their changes to their VA.gov profile

<img width="240" alt="Radio button asking where to save" src="https://github.com/user-attachments/assets/a9d4ba37-a778-4a4e-931e-c422e6731d0e">

### Examples in production
Coming soon!

## Code usage
Coming soon!

## Content considerations

### Directions for updating uneditable information
Directions for updating information that can’t be updated online vary. Instructions should be updated based on the context of the form or application used. General guidelines are:

- If it’s **benefits**-related, include the content that has the VA benefits hotline. For example:
> test

- If it’s **health**-related, include the content that has the VA benefits hotline _and_ the content to contact your local medical center.
> test

## Research findings
The Authenticated Experience Design Patterns team [conducted user research](https://github.com/department-of-veterans-affairs/va.gov-team/tree/master/products/authenticated-patterns/Design%20and%20Research/2024-09%20Research%20Initiative%202%20-%20Update%20Prefill) in late 2024 about how users prefer to see their editable and non-editable information, and how they prefer to be informed about how to edit it. The majority of participants want updates to save to their VA.gov profile, but some also want the ability to choose where the data saves, in the case that they are using a temporary address or other temporary situation.
