# Use Cases

# for

# MANGA/COMIC WEB APPLICATION

**Version 1.0 approved**

**Prepared by M. Oskhar Mub**

**UIN Syarif Hidayatullah Jakarta**

**4 January 2024**

**Table of Contents**


[1. Introduction	3](#1.-introduction	3)
[2. Explanation of Use Case Contents	3](#2.-explanation-of-use-case-contents	3)
[3. Product Use Case	4](#3.-product-use-case	4)
[3.1. User Registration	4](#3.1.-user-registration	4)
[3.2. Authentication and Authorization	5](#3.2.-authentication-and-authorization	5)
	[User Authentication:	5](#user-authentication:	5)
	[User Authorization:	5](#user-authorization:	5)
	[Admin Authentication:	5](#admin-authentication:	5)
	[Admin Authorization:	6](#admin-authorization:	6)
[3.3. User Recommender System	6](#3.3.-user-recommender-system	6)
[3.4. Manga Discovery with Advanced Filters	8](#3.4.-manga-discovery-with-advanced-filters	8)
[3.5. Language Selection and Content Localization	9](#3.5.-language-selection-and-content-localization	9)
[3.6. User Leaving Comment	10](#3.6.-user-leaving-comment	10)
[3.7. User Giving Rating	11](#3.7.-user-giving-rating	11)
[3.8. Reporting Inappropriate Content	12](#3.8.-reporting-inappropriate-content	12)
[3.9. User Following an Author	13](#3.9.-user-following-an-author	13)
[3.10. User Bookmarking Manga	13](#3.10.-user-bookmarking-manga	13)
[3.11. User Notification Inbox	14](#3.11.-user-notification-inbox	14)
[3.12. Author Registration and Onboarding	15](#3.12.-author-registration-and-onboarding	15)
[3.13. Author Profile Management	16](#3.13.-author-profile-management	16)
[3.14. Manga Creation and Management	16](#3.14.-manga-creation-and-management	16)
[3.15. Chapter Management	18](#3.15.-chapter-management	18)
[3.16. Manga Trend Statistics for Authors	18](#3.16.-manga-trend-statistics-for-authors	18)
[3.17. User Interaction Tracking	20](#3.17.-user-interaction-tracking	20)
[3.18. Notification Management	21](#3.18.-notification-management	21)
[4. System Use Case	21](#4.-system-use-case	21)
[4.1. Admin Managing Users	21](#4.1.-admin-managing-users	21)
[4.2. Admin Managing Authors	22](#4.2.-admin-managing-authors	22)
[4.3. Admin Managing Manga	23](#4.3.-admin-managing-manga	23)
[4.4. Admin Managing Web View Reports	24](#4.4.-admin-managing-web-view-reports	24)
[4.5. Admin Managing Follows	25](#4.5.-admin-managing-follows	25)
[4.6. Admin Giving Warning to Author	26](#4.6.-admin-giving-warning-to-author	26)
[4.7. Admin Sending Message to Author	26](#4.7.-admin-sending-message-to-author	26)
[5. Sponsor Acceptance	28](#5.-sponsor-acceptance	28)
# 

# Introduction

The Use Case Document is a business document which provides a story of how a system, and its actors, will be utilized to achieve a specific goal.  An effective Use Case should provide a detailed step-by-step description of how the system will be used by its actors to achieve the planned outcome.  The purpose of the Use Case is to tie the business needs of the system to the design parameters of the system to ensure that the completed system achieves the goals established by the business requirements.  The level of detail in Use Cases may vary greatly depending on the size and complexity of the system being designed.

This Use Case has been developed for ABC Corporation’s new system for ordering material based on the design team’s gathering of business and functional area requirements.  The Material Ordering System will replace the manual material ordering processes currently utilized by ABC Corp.  ABC Corp. has identified business needs for reducing man hours for material ordering and leveraging existing software platforms (i.e. SAP) to help manage material ordering and inventory management.  The new Material Ordering System will be designed to meet these business needs and improve ABC Corp.’s overall business strategy.

# Explanation of Use Case Contents

Use Case formats and contents may vary based on system requirements, organizational standards, or unique situations.  However, a majority of Use Cases consist of some fundamental contents which may be applied across a wide range of system types.  This section will provide explanations for each section of the Use Case.

Name of Use Case:  Provide a short name for the use case which should lend itself to the objective of the system.

Description:  This section should provide a description of both the reason for using the use case and the expected outcome of the use case.

Actors: Actors may be primary or secondary. Primary actors are the people who will be initiating the system described in the use case.  Secondary actors are those will participate in the completion of the use case.

Precondition: This section should describe any conditions that must be true or activities that must be completed prior to executing the use case.

Postcondition: This section should describe the state of the system at the conclusion of the use case.  Postconditions may include conditions for both successful and unsuccessful execution of the use case.

Flow: This section should describe all actions of the user and the expected system responses for planned normal execution of the use case.  The description should be sequential and provide adequate detail to understand all user actions and system responses.

Alternative Flows: Many use cases have varying or special extensions or conditions which are separate from the main flow but also necessary. Alternative flows are usually the result of options or exceptions built into the use case which may alter the primary flow.

Exceptions: When use cases are executed, there may be various conditions which result in errors.  This section should describe any errors that may result during use case execution and how the system will react or respond to those errors.

Requirements:  This section should describe any non-functional or special requirements for the system as the use case is executed.  These requirements may consist of legal or regulatory requirements, quality standards, or organizational requirements that are outside of the functional requirements the system is expected to perform.

# Product Use Case

1. User Registration

| Name of Use Case: | User Registration |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 20/1/2024 |  | Last Revision Date: | 20/1/2024 |
| Description: |  | This use case describes the process of a new user registering on the web comic/manga application. |  |  |
| Actors: |  | Guest (New User), System |  |  |
| Preconditions: |  | The user does not have an existing account. |  |  |
| Postconditions: |  | The user's account is successfully created, and they are ready to log in. |  |  |
| Flow: |  | User provides a unique username, a valid email, and a secure password.
The application validates the provided information.
The user is registered with a default role set as 'User'.
The system sends a confirmation email to the user.
User confirms the registration by clicking the link in the confirmation email. |  |  |
| Alternative Flows:
 |  | If the email confirmation link is not clicked within a certain time, the registration may expire, and the user needs to register again. |  |  |
| Exceptions: |  | If the email confirmation link is not clicked within a specified time, the registration becomes invalid, and the user must re-register. |  |  |
| Requirements:
 |  | The system must validate the uniqueness of usernames and ensure that email addresses are valid.
Confirmation emails must be sent securely and promptly. |  |  |

2. Authentication and Authorization

| Name of Use Case: | Authentication and Authorization |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 20/1/2024 |  | Last Revision Date: | 20/1/2024 |
| Description: |  | This use case involves the processes of authentication and authorization to ensure secure and controlled access to the manga platform. |  |  |
| Actors: |  | User, Admin, Guest |  |  |
| Preconditions: |  | The user or admin interacts with the platform. |  |  |
| Postconditions: |  | The user gains appropriate access to their account features.
The admin gains access to the administrative features. |  |  |
| Flow: |  | User Authentication:
Users access the platform.
User initiates the login process.
Enter Credentials: The user provides a valid combination of username/email and password.
System verifies user credentials.
Check against Database: Verify the entered credentials against stored user data.
Two-Factor Authentication (optional): If enabled, the system prompts the user for a second form of authentication.
Users gain access to their account.
User Authorization:
System checks user roles and permissions.
User Role Assignment: Assign appropriate roles (e.g., regular user, premium user) to the authenticated user.
Check Permissions: Ensure the user has the necessary permissions for the requested action.
User performs actions within authorized scope.
Admin Authentication:
Admin accesses the platform.
Admin initiates the login process.
Enter Credentials: The admin provides valid credentials.
System verifies admin credentials.
Check against Database: Verify the entered credentials against stored admin data.
Two-Factor Authentication (optional): If enabled, the system prompts the admin for a second form of authentication.
Admin gains access to administrative features.
Admin Authorization:
System checks admin roles and permissions.
Admin Role Assignment: Assign appropriate roles (e.g., content moderator, super admin) to the authenticated admin.
Check Permissions: Ensure the admin has the necessary permissions for the requested administrative action.
Admin performs actions within authorized scope. |  |  |
| Alternative Flows:
 |  | User Forgot Password:
If a user forgets their password, the system provides a password reset option through email or other verification methods. |  |  |
| Exceptions: |  | Invalid Credentials:
If credentials are invalid, the system informs the user or admin and prompts for correct credentials.
Account Lockout (optional):
After multiple unsuccessful login attempts, the system may temporarily lock the account for security reasons. |  |  |
| Requirements:
 |  | Secure Storage of Credentials: Ensure passwords are securely stored using encryption.
Two-Factor Authentication (optional): Provide an option for an additional layer of authentication.
Role-Based Access Control (RBAC): Implement RBAC for both users and admins.
Password Reset Mechanism: Allow users to reset their password through secure methods. |  |  |

3. User Recommender System

| Name of Use Case: | User Recommender System |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 20/1/2024 |  | Last Revision Date: | 20/1/2024 |
| Description: |  | This use case involves the implementation of a User Recommender System to provide personalized manga recommendations based on user preferences and behavior. |  |  |
| Actors: |  | User |  |  |
| Preconditions: |  | The user is registered and logged into their account.
The user has interacted with manga content on the platform. |  |  |
| Postconditions: |  | The system generates and displays personalized manga recommendations for the user. |  |  |
| Flow: |  | User navigates to the homepage or recommendation section.
User initiates the Recommender System.
System analyzes user behavior and preferences.
User Interaction Tracking: The system considers the user's history, including viewed titles, liked/disliked content, and previous searches.
User Genre Preferences: Analyzing the genres the user has engaged with the most.
System generates personalized manga recommendations.
Collaborative Filtering: Utilizing collaborative filtering algorithms to suggest manga based on similar users' preferences.
Content-Based Filtering: Considering characteristics of manga the user has liked to recommend similar content.
Recommendations are displayed to the user.
Option to Provide Feedback: User can provide feedback on individual recommendations (like/dislike) for further refinement. |  |  |
| Alternative Flows:
 |  | aIf the user has not interacted with enough content:
The system informs the user that more interactions are needed to improve recommendations. |  |  |
| Exceptions: |  | Insufficient User Interaction Data:
If the user has not interacted with enough content, the system informs the user and encourages more interactions for better recommendations. |  |  |
| Requirements:
 |  | User Interaction Tracking: The system must track and analyze user interactions with manga content.
Collaborative Filtering Algorithm: Implementation of collaborative filtering to suggest manga based on similar users.
Content-Based Filtering Algorithm: Consideration of manga characteristics for personalized recommendations.
Feedback Mechanism: Users should have the option to provide feedback on recommendations. |  |  |

4. Manga Discovery with Advanced Filters

| Name of Use Case: | Manga Discovery with Advanced Filters |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 20/1/2024 |  | Last Revision Date: | 20/1/2024 |
| Description: |  | This use case involves an advanced search functionality known as "Catch all manga," allowing users to discover manga titles based on various filters such as search keywords, length, start status, genre, and release year. |  |  |
| Actors: |  | User |  |  |
| Preconditions: |  | User has accessed the manga discovery section. |  |  |
| Postconditions: |  | Users are presented with a refined list of manga titles based on selected filters. |  |  |
| Flow: |  | User navigates to the manga discovery section.
User initiates the "Catch all manga" advanced search.
View Available Filters: User views a list of available filters, including search keywords, length, start status, genre, and release year.
User sets desired filters for manga search.
Search Keywords: User enters keywords for the manga title.
Length Filter: User sets the desired length range (e.g., short, medium, long).
Start Status Filter: User selects whether to include ongoing, completed, or both types of manga.
Genre Filter: User selects one or multiple genres from the available options.
Release Year Filter: User specifies the release year or range.
System processes user-selected filters and refines the manga list.
User is presented with a list of manga titles based on the applied filters. |  |  |
| Alternative Flows:
 |  | Reset Filters:
User has the option to reset all filters to their default values |  |  |
| Exceptions: |  | No Matching Manga:
If no manga titles match the specified filters, the system informs the user and suggests adjusting the filters. |  |  |
| Requirements:
 |  | Advanced Search Interface: Implement a user-friendly interface allowing easy selection and modification of filters.
Filter Persistence: Ensure that user-selected filters persist during the browsing session.
Real-time Filtering: Provide real-time updates to the manga list as the user adjusts filters.
Responsive Design: Ensure the system is responsive and works well across different devices. |  |  |

5. Language Selection and Content Localization

| Name of Use Case: | Language Selection and Content Localization |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 20/1/2024 |  | Last Revision Date: | 20/1/2024 |
| Description: |  | This use case involves enabling users to select their preferred language and ensuring content is displayed in the chosen language, supporting Internationalization (i18n) and Localization (l10n). |  |  |
| Actors: |  | User |  |  |
| Preconditions: |  | Users access the platform. |  |  |
| Postconditions: |  | User interfaces and content are displayed in the selected language. |  |  |
| Flow: |  | Users access the platform.
User navigates to the settings or profile section.
User initiates the language selection process.
View Available Languages: User views a list of available languages.
Select Preferred Language: User selects their preferred language from the list.
System saves the selected language preference in the user's profile.
User interfaces and content are displayed in the selected language.
Dynamic Content Localization: All dynamic content, including menus, buttons, and labels, is displayed in the chosen language.
Static Content Localization: Static content, such as help sections and informational text, is presented in the selected language. |  |  |
| Alternative Flows:
 |  | Fallback to Default Language:
If the selected language translation is unavailable for certain content, the system falls back to the default language. |  |  |
| Exceptions: |  | Unavailable Language:
If the selected language is not available, the system informs the user and suggests an alternative. |  |  |
| Requirements:
 |  | Multilingual Support: Provide support for a range of languages to accommodate diverse user preferences.
Language Preference Persistence: Ensure that the user's language preference is saved for future visits.
Content Localization Resources: Establish a system for translating and managing content in different languages.
Fallback Mechanism: Implement a mechanism to gracefully handle situations where translations are not available. |  |  |

6. User Leaving Comment

| Name of Use Case: | User Leaving Comment |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 20/1/2024 |  | Last Revision Date: | 20/1/2024 |
| Description: |  | Describes the process of a user leaving a comment on a chapter of the manga. |  |  |
| Actors: |  | User |  |  |
| Preconditions: |  | User is logged in and viewing a chapter of the manga. |  |  |
| Postconditions: |  | The user's comment is successfully added to the system. |  |  |
| Flow: |  | User navigates to a manga or chapter.
User decides to leave a comment and enters the content.
User submits the comment.
The application associates the comment with the user, manga, and chapter. |  |  |
| Alternative Flows:
 |  | Users can reply to existing comments, creating a threaded discussion. |  |  |
| Exceptions: |  | If the comment content is empty, the system prompts the user to enter valid content. |  |  |
| Requirements:
 |  | The system should allow users to engage in threaded discussions by replying to existing comments. |  |  |

7. User Giving Rating

| Name of Use Case: | User Giving Rating |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 20/1/2024 |  | Last Revision Date: | 21/1/2024 |
| Description: |  | Describes the process of a user providing a rating and optional review comment for a manga. |  |  |
| Actors: |  | User |  |  |
| Preconditions: |  | User is logged in and viewing a manga. |  |  |
| Postconditions: |  | The user's rating is successfully added to the system. |  |  |
| Flow: |  | User navigates to the manga they want to rate.
User provides a numerical rating (1 to 5) and an optional review comment.
User submits the rating.
The application associates the rating with the user and manga. |  |  |
| Alternative Flows:
 |  | If the user chooses not to leave a review comment, they can skip that part of the process. |  |  |
| Exceptions: |  | If the rating input is invalid, the system prompts the user to provide a valid rating. |  |  |
| Requirements: |  | The system must validate the numerical rating provided by the user. |  |  |

8. Reporting Inappropriate Content

| Name of Use Case: | Reporting Inappropriate Content |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 20/1/2024 |  | Last Revision Date: | 21/1/2024 |
| Description: |  | Describes the process of a user reporting inappropriate content or spam. |  |  |
| Actors: |  | User, System |  |  |
| Preconditions: |  | User identifies inappropriate content while using the application. |  |  |
| Postconditions: |  | A web view report is submitted to the system. |  |  |
| Flow: |  | User identifies inappropriate content.
User initiates the report, providing details such as the type of content and a description.
User submits the report.
The application associates the report with the user, manga, and chapter. |  |  |
| Alternative Flows:
 |  | Users can select the type of inappropriate content from predefined categories. |  |  |
| Exceptions: |  | If the report details are incomplete, the system prompts the user to provide all required information. |  |  |
| Requirements: |  | Inappropriate content reports should include predefined categories for ease of classification. |  |  |

9. User Following an Author

| Name of Use Case: | User Following an Author |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 20/1/2024 |  | Last Revision Date: | 21/1/2024 |
| Description: |  | Describes the process of a user following an author to receive updates. |  |  |
| Actors: |  | User |  |  |
| Preconditions: |  | User is logged in and viewing an author's profile. |  |  |
| Postconditions: |  | The user successfully follows the author, and the follow action is recorded. |  |  |
| Flow: |  | User navigates to an author's profile.
User clicks the 'Follow' button.
The application records the follow action, including a timestamp. |  |  |
| Alternative Flows:
 |  | Users can unfollow an author by clicking an 'Unfollow' button. |  |  |
| Exceptions: |  | If the user is not logged in, the system prompts them to log in before following an author. |  |  |
| Requirements: |  | The follow mechanism must be robust, allowing users to unfollow authors if desired. |  |  |

10. User Bookmarking Manga

| Name of Use Case: | User Following an Author |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 20/1/2024 |  | Last Revision Date: | 21/1/2024 |
| Description: |  | Describes the process of a user bookmarking a manga to save it for future reading. |  |  |
| Actors: |  | User |  |  |
| Preconditions: |  | User is logged in and browsing manga titles. |  |  |
| Postconditions: |  | The selected manga is successfully bookmarked in the user's profile for future reference. |  |  |
| Flow: |  | User navigates to the list of available manga titles.
Users click on a specific manga title they want to bookmark.
User selects the option to "Bookmark" the manga.
The application adds the manga to the user's list of bookmarked titles. |  |  |
| Alternative Flows:
 |  | If the user accidentally clicks on the "Bookmark" option, they can undo the action by selecting "Remove Bookmark." |  |  |
| Exceptions: |  | If there is an error in bookmarking the manga, the system prompts the user to try again. |  |  |
| Requirements: |  | The system must provide a user-friendly interface for managing bookmarked manga titles.
Users should be able to quickly access their bookmarked titles from their profile. |  |  |

11. User Notification Inbox

| Name of Use Case: | User Notification Inbox |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 20/1/2024 |  | Last Revision Date: | 21/1/2024 |
| Description: |  | This use case involves providing users with a dedicated notification inbox within the web comic/manga application. |  |  |
| Actors: |  | User,System |  |  |
| Preconditions: |  | User is logged into their account. |  |  |
| Postconditions: |  | Users can conveniently review and manage notifications within the dedicated inbox. |  |  |
| Flow: |  | Users access the notification inbox from their profile.
The system displays a chronological list of notifications.
Users can mark notifications as read, unread, or delete them. |  |  |
| Alternative Flows:
 |  | If the user misses a notification, the system retains it in the inbox for a certain period.
If the user clicks on a notification, the system directs them to the relevant content (e.g., manga, chapter). |  |  |
| Exceptions: |  | If there is an issue retrieving notifications, the system displays an error message and prompts the user to try again.
If a user marks a notification as unread, but the action fails, the system logs the error for further investigation.
If the user attempts to delete a notification that is critical for system updates, the system prompts for confirmation to avoid accidental deletion. |  |  |
| Requirements: |  | The system must provide real-time updates for time-sensitive notifications.
Notification inbox must support filtering and search capabilities.
Notifications should be retained for a reasonable period, even if the user is not actively checking the inbox.
The system should offer a seamless transition from the notification inbox to the associated content. |  |  |

12. Author Registration and Onboarding

| Name of Use Case: | Author Registration and Onboarding |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | This use case involves the registration and onboarding process for new authors. |  |  |
| Actors: |  | Admin, Author |  |  |
| Preconditions: |  | Admin is logged into the admin dashboard. |  |  |
| Postconditions: |  | New authors are successfully registered and added to the platform. |  |  |
| Flow: |  | Admin accesses the Author Management section.
Admin initiates the author registration process.
Author completes the registration form, providing necessary details.
The application validates the information and creates a new author profile. |  |  |
| Alternative Flows:
 |  | If the registration form is incomplete, the system prompts the admin to ensure all required fields are filled. |  |  |
| Exceptions: |  | If the registration process encounters technical errors, the system logs the issue for further investigation. |  |  |
| Requirements: |  | The system must enforce unique usernames and email addresses.
Secure transmission and storage of registration data. |  |  |

13. Author Profile Management

| Name of Use Case: | Author Profile Management |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | This use case covers the management of author profiles, including updating information. |  |  |
| Actors: |  | Admin, Author |  |  |
| Preconditions: |  | Author is logged into their account. |  |  |
| Postconditions: |  | Author profile details are successfully updated. |  |  |
| Flow: |  | Author accesses their profile from the dashboard.
Author edits profile information such as pen name, biography, and social media links.
The application validates and updates the author's profile. |  |  |
| Alternative Flows:
 |  | If the profile update includes invalid data, the system prompts the author to correct the errors. |  |  |
| Exceptions: |  | If there are issues with updating the profile picture, the system allows the author to retry or select a new image. |  |  |
| Requirements: |  | The system must support the upload and storage of profile pictures.
Real-time validation of social media links. |  |  |

14. Manga Creation and Management

| Name of Use Case: | Manga Creation and Management |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | This use case involves the creation and management of manga titles by authors, with an added focus on genre classification and tagging. |  |  |
| Actors: |  | Author |  |  |
| Preconditions: |  | The author is logged into their account. |  |  |
| Postconditions: |  | New manga titles are successfully created and associated with the author's profile, including genre classification and tagging. |  |  |
| Flow: |  | Author navigates to the dashboard's manga management section.
Author initiates the process of adding a new manga.
Author provides details such as title, description, genre, and cover image.
Support for multiple genres: Author can select multiple genres for each manga.
The application associates the new manga with the author's profile.
Validation of unique titles: The system ensures that each title is unique for the author. |  |  |
| Alternative Flows:
 |  | If the manga details are incomplete:
The system prompts the author to fill in the required fields.
If there is an issue with uploading the cover image:
The system allows the author to retry or select a different image. |  |  |
| Exceptions: |  | Incomplete Manga Details:
If the manga details are incomplete, the system prompts the author to fill in the required fields.
Issue with Cover Image:
If there is an issue with uploading the cover image, the system allows the author to retry or select a different image. |  |  |
| Requirements: |  | Support for multiple genres for each manga.
Validation of unique titles for each author. |  |  |

15. Chapter Management

| Name of Use Case: | Chapter Management |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | This use case involves the creation and management of chapters within a manga. |  |  |
| Actors: |  | Author, System |  |  |
| Preconditions: |  | The author is logged into their account. |  |  |
| Postconditions: |  | New chapters are successfully added to the selected manga. |  |  |
| Flow: |  | Author selects a manga from their dashboard.
Author initiates the process of adding a new chapter.
Author provides details such as title, chapter number, and content.
The application associates the new chapter with the selected manga. |  |  |
| Alternative Flows:
 |  | If the chapter details are incomplete, the system prompts the author to fill in the required fields. |  |  |
| Exceptions: |  | If there is an issue with uploading chapter content, the system allows the author to retry or choose a different content file. |  |  |
| Requirements: |  | Support for various content formats (images, text) for chapters.
Automatic chapter numbering. |  |  |

16. Manga Trend Statistics for Authors

| Name of Use Case: | Manga Trend Statistics for Authors |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | This use case enables authors to view trend statistics derived from user interactions across all manga titles, providing a comprehensive overview of global user engagement. |  |  |
| Actors: |  | Author, System |  |  |
| Preconditions: |  | Author has logged into their account on the manga platform. |  |  |
| Postconditions: |  | Author has access to trend statistics reflecting user interactions across all manga titles. |  |  |
| Flow: |  | Author navigates to the dashboard or analytics section.
Author initiates the "Manga Trend Statistics" feature.
Select Global View: Author selects the option for a global view of trend statistics.
System generates and displays trend statistics.
Aggregate User Interactions: The system aggregates data on user interactions, including views, likes, comments, and bookmarks, across all manga titles.
Time-Based Analysis: Author can choose different time intervals (e.g., daily, weekly, monthly) for trend analysis.
Popular Genres: System highlights popular genres based on user engagement.
User Demographics: Optionally, the system may provide insights into user demographics engaging with the manga content.
Author reviews and interprets trend statistics.
Identify Top-performing Manga: Author identifies manga titles with the highest user engagement.
Understand User Preferences: Author gains insights into user preferences, allowing for better decision-making in future content creation.
Adapt Strategies: Authors may adapt their content creation or marketing strategies based on observed trends. |  |  |
| Alternative Flows:
 |  | Filter by Specific Manga:
Author has the option to view trend statistics for a specific manga title. |  |  |
| Exceptions: |  | Insufficient Data:
If there is not enough data available for meaningful trend analysis, the system informs the author and suggests reviewing a longer time period. |  |  |
| Requirements: |  | Comprehensive User Interaction Tracking: Ensure that the system accurately tracks user interactions across all manga titles.
Data Visualization: Implement clear and visually appealing charts or graphs to represent trend statistics.
Custom Time Range Selection: Allow authors to choose custom time ranges for trend analysis.
Privacy Considerations: Ensure that user demographics are presented in an aggregated and anonymized manner to protect user privacy. |  |  |

17. User Interaction Tracking

| Name of Use Case: | User Interaction Tracking |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | This use case involves tracking user interactions with an author's content. |  |  |
| Actors: |  | Author, System |  |  |
| Preconditions: |  | The author is logged into their account. |  |  |
| Postconditions: |  | Author gains insights into user engagement. |  |  |
| Flow: |  | Author accesses the dashboard's analytics section.
Author reviews metrics such as views, comments, and ratings for each manga and chapter.
The application displays user interaction data in a comprehensible format. |  |  |
| Alternative Flows:
 |  | If there is a sudden spike in user engagement, the system provides real-time notifications to the author. |  |  |
| Exceptions: |  | If the analytics data retrieval fails, the system logs the issue for investigation. |  |  |
| Requirements: |  | Real-time updates for user engagement metrics.
Historical data tracking for analytics. |  |  |

18. Notification Management

| Name of Use Case: | Notification Management |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | This use case covers the management of notifications related to user interactions. |  |  |
| Actors: |  | Author, System |  |  |
| Preconditions: |  | Author can efficiently manage and respond to notifications. |  |  |
| Postconditions: |  | Author gains insights into user engagement. |  |  |
| Flow: |  | Author accesses the dashboard's notification center.
Author reviews new comments, ratings, or follow notifications.
The application allows the author to respond or take relevant actions directly from the dashboard. |  |  |
| Alternative Flows:
 |  | If the author receives a large number of notifications, the system provides sorting and filtering options. |  |  |
| Exceptions: |  | If the notification retrieval fails, the system retries or provides an error message. |  |  |
| Requirements: |  | Support for various notification types (comments, ratings, follows).
Bulk actions for efficient notification management. |  |  |

# System Use Case

19. Admin Managing Users

| Name of Use Case: | Admin Managing Users |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | This use case involves the admin managing user accounts and roles within the system. |  |  |
| Actors: |  | Admin |  |  |
| Preconditions: |  | Admin is logged into the admin dashboard. |  |  |
| Postconditions: |  | User accounts and roles are successfully managed. |  |  |
| Flow: |  | Admin navigates to the user management section.
Admin views a list of all users and their details.
Admin has the ability to search for specific users based on username or email.
Admin can view and edit user details, including username, email, and role.
Admin can deactivate or delete user accounts as needed. |  |  |
| Alternative Flows:
 |  | If a user account is deactivated, the system retains the user data but restricts login access. |  |  |
| Exceptions: |  | If there are errors in editing user details, the system prompts the admin to correct them. |  |  |
| Requirements:
 |  | The admin must have the authority to view, edit, deactivate, or delete user accounts.
Deactivated user accounts should not be able to log in. |  |  |

20. Admin Managing Authors

| Name of Use Case: | Admin Managing Users |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | This use case involves the admin managing author profiles and associated manga titles. |  |  |
| Actors: |  | Admin |  |  |
| Preconditions: |  | Admin is logged into the admin dashboard. |  |  |
| Postconditions: |  | Author profiles and manga titles are successfully managed. |  |  |
| Flow: |  | Admin navigates to the author management section.
Admin views a list of all authors and their profiles.
Admin has the ability to search for specific authors based on pen name or email.
Admin can view and edit author details, including pen name and biography.
Admin can deactivate or delete author profiles.
Admin can view a list of manga titles associated with each author.
Admin has the ability to edit or delete individual manga titles. |  |  |
| Alternative Flows:
 |  | If an author profile is deactivated, all associated manga titles are also deactivated. |  |  |
| Exceptions: |  | If there are errors in editing author details or manga titles, the system prompts the admin to correct them. |  |  |
| Requirements:
 |  | The admin must have the authority to view, edit, deactivate, or delete author profiles and associated manga titles. |  |  |

21. Admin Managing Manga

| Name of Use Case: | Admin Managing Manga |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | This use case involves the admin managing manga details, chapters, and user interactions. |  |  |
| Actors: |  | Admin |  |  |
| Preconditions: |  | Admin is logged into the admin dashboard. |  |  |
| Postconditions: |  | Manga details, chapters, and user interactions are successfully managed. |  |  |
| Flow: |  | Admin navigates to the manga management section.
Admin views a list of all manga titles and their details.
Admin has the ability to search for specific manga titles based on title or genre.
Admin can view and edit manga details, including title, description, and cover image.
Admin can deactivate or delete manga titles.
Admin views a list of chapters for each manga and has the ability to edit or delete chapters.
Admin can view user comments and ratings for each manga.
Admin has the authority to delete inappropriate comments or ban users if necessary. |  |  |
| Alternative Flows:
 |  | If a manga title is deactivated, all associated chapters, comments, and ratings are also deactivated. |  |  |
| Exceptions: |  | If there are errors in editing manga details or chapters, the system prompts the admin to correct them. |  |  |
| Requirements:
 |  | The admin must have the authority to view, edit, deactivate, or delete manga titles, chapters, and user interactions. |  |  |

22. Admin Managing Web View Reports

| Name of Use Case: | Admin Managing Web View Reports |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | This use case involves the admin managing web view reports submitted by users. |  |  |
| Actors: |  | Admin, User |  |  |
| Preconditions: |  | Admin is logged into the admin dashboard. |  |  |
| Postconditions: |  | Web view reports are successfully managed. |  |  |
| Flow: |  | Admin navigates to the web view report management section.
Admin views a list of all web view reports with details such as report type and description.
Admin can search for specific reports based on manga title or user.
Admin can view the details of each report, including the reported content and status.
Admin has the ability to mark reports as processed or rejected based on the investigation. |  |  |
| Alternative Flows:
 |  | If a report is marked as processed, the admin may need to take further actions such as content removal or user warning. |  |  |
| Exceptions: |  | If there are errors in processing web view reports, the system prompts the admin to correct them. |  |  |
| Requirements:
 |  | The admin must have the authority to view, process, and manage web view reports. |  |  |

23. Admin Managing Follows

| Name of Use Case: | Admin Managing Follows |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | This use case involves the admin managing user follows on authors. |  |  |
| Actors: |  | Admin, System |  |  |
| Preconditions: |  | Admin is logged into the admin dashboard. |  |  |
| Postconditions: |  | Follow relationships are successfully managed. |  |  |
| Flow: |  | Admin navigates to the follow management section.
Admin views a list of all user follows with details such as follower and following authors.
Admin can search for specific follow relationships based on user or author.
Admin has the ability to view details of each follow relationship, including timestamps.
Admin can delete or modify existing follow relationships if necessary. |  |  |
| Alternative Flows:
 |  | If a following relationship is modified, the timestamp is updated to reflect the last interaction. |  |  |
| Exceptions: |  | If there are errors in managing follow relationships, the system prompts the admin to correct them. |  |  |
| Requirements:
 |  | The admin must have the authority to view, modify, or delete user follow relationships. |  |  |

24. Admin Giving Warning to Author

| Name of Use Case: | Admin Giving Warning to Author |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | Describes the process of an admin issuing a warning to an author for content violations or policy breaches. |  |  |
| Actors: |  | Admin, Author |  |  |
| Preconditions: |  | Admin is logged into the admin dashboard, and the author has violated content policies. |  |  |
| Postconditions: |  | The author receives a warning notification, and the admin's action is recorded. |  |  |
| Flow: |  | Admin identifies a specific author who has violated content policies or breached platform rules.
Admin selects the option to issue a warning to the author.
Admin provides a clear and detailed explanation of the violation or breach.
The application sends a notification to the author about the warning. |  |  |
| Alternative Flows:
 |  | If the violation is severe, the admin may choose to suspend the author's account temporarily. |  |  |
| Exceptions: |  | If there are errors in issuing the warning, the system prompts the admin to correct them. |  |  |
| Requirements:
 |  | The warning system should be transparent, providing authors with a clear understanding of the violation and potential consequences. |  |  |

25. Admin Sending Message to Author

| Name of Use Case: | Admin Sending Message to Author |  |  |  |
| --- |  --- |  --- |  --- |  --- | 
| Created By: | M. Oskhar Mub |  | Last Updated By: | M. Oskhar Mub |
| Date Created: | 28/1/2024 |  | Last Revision Date: | 28/1/2024 |
| Description: |  | Describes the process of an admin sending a direct message to an author for communication purposes. |  |  |
| Actors: |  | Admin, Author |  |  |
| Preconditions: |  | Admin is logged into the admin dashboard, and there is a need for direct communication with the author. |  |  |
| Postconditions: |  | The author receives the admin's message, and both parties can engage in a private conversation. |  |  |
| Flow: |  | Admin navigates to the author management section and selects the specific author.
Admin chooses the option to send a direct message to the author.
Admin composes the message, providing necessary details or instructions.
The application sends the message to the author's inbox, notifying them of the new communication. |  |  |
| Alternative Flows:
 |  | Authors can respond to admin messages, creating a threaded communication history. |  |  |
| Exceptions: |  | If there are errors in sending the message, the system prompts the admin to correct them. |  |  |
| Requirements:
 |  | The messaging system should ensure privacy, and messages should be stored securely for reference purposes. |  |  |

# 

# Sponsor Acceptance 

Approved by the Project Sponsor:

_____________________	Date:_______________________

<Project Sponsor>

<Project Sponsor Title>
