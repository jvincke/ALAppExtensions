This module introduces a dialog for the user to enter a password.

# Public Objects
## Password Dialog Management (Codeunit 9810)

 Exposes functionality to open dialogs for entering passwords with different settings.
 

### OpenPasswordDialog (Method) <a name="OpenPasswordDialog"></a> 

 Opens a dialog for the user to enter a password and returns the typed password if there is no validation error,
 otherwise an empty text is returned.
 

#### Syntax
```
procedure OpenPasswordDialog(DisablePasswordValidation: Boolean; DisablePasswordConfirmation: Boolean): Text
```
#### Parameters
*DisablePasswordValidation ([Boolean](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/methods-auto/boolean/boolean-data-type))* 

Disables the checks for the password validity. Default value is false.

*DisablePasswordConfirmation ([Boolean](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/methods-auto/boolean/boolean-data-type))* 

If set to true the new password is only needed once. Default value is false.

#### Return Value
*[Text](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/methods-auto/text/text-data-type)*

The typed password, or empty text if the password validations fail.
### OpenPasswordDialog (Method) <a name="OpenPasswordDialog"></a> 

 Opens a dialog for the user to enter a password and returns the typed password if there is no validation error,
 otherwise an empty text is returned.
 

#### Syntax
```
procedure OpenPasswordDialog(DisablePasswordValidation: Boolean): Text
```
#### Parameters
*DisablePasswordValidation ([Boolean](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/methods-auto/boolean/boolean-data-type))* 

Disables the checks for the password validity. Default value is false.

#### Return Value
*[Text](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/methods-auto/text/text-data-type)*

The typed password, or empty text if the password validations fail.
### OpenPasswordDialog (Method) <a name="OpenPasswordDialog"></a> 

 Opens a dialog for the user to enter a password and returns the typed password if there is no validation error,
 otherwise an empty text is returned.
 

#### Syntax
```
procedure OpenPasswordDialog(): Text
```
#### Return Value
*[Text](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/methods-auto/text/text-data-type)*

The typed password, or empty text if the password validations fail.
### OpenChangePasswordDialog (Method) <a name="OpenChangePasswordDialog"></a> 

 Opens a dialog for the user to change a password and returns the old and new typed passwords if there is no validation error,
 otherwise an empty text are returned.
 

#### Syntax
```
procedure OpenChangePasswordDialog(var OldPassword: Text; var Password: Text)
```
#### Parameters
*OldPassword ([Text](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/methods-auto/text/text-data-type))* 

Out parameter, the old password user typed on the dialog.

*Password ([Text](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/methods-auto/text/text-data-type))* 

Out parameter, the new password user typed on the dialog.

### OnSetMinPasswordLength (Event) <a name="OnSetMinPasswordLength"></a> 

 Event to override the Minimum number of characters in the password.
 The Minimum length can only be increased not decreased. Default value is 8 characters long.
 

#### Syntax
```
[IntegrationEvent(false, false)]
internal procedure OnSetMinPasswordLength(var MinPasswordLength: Integer)
```
#### Parameters
*MinPasswordLength ([Integer](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/methods-auto/integer/integer-data-type))* 

The number of characters to be set as minimum requirement.


## Password Dialog (Page 9810)

 A Page that allows the user to enter a password.
 

### GetPasswordValue (Method) <a name="GetPasswordValue"></a> 

 Gets the password value typed on the page.
 

#### Syntax
```
[Scope('OnPrem')]
procedure GetPasswordValue(): Text
```
#### Return Value
*[Text](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/methods-auto/text/text-data-type)*

The password value typed on the page.
### GetOldPasswordValue (Method) <a name="GetOldPasswordValue"></a> 

 Gets the old password value typed on the page.
 

#### Syntax
```
[Scope('OnPrem')]
procedure GetOldPasswordValue(): Text
```
#### Return Value
*[Text](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/methods-auto/text/text-data-type)*

The old password typed on the page.
### EnableChangePassword (Method) <a name="EnableChangePassword"></a> 

 Enables the Change password mode, it makes the old password field on the page visible.
 

#### Syntax
```
[Scope('OnPrem')]
procedure EnableChangePassword()
```
### DisablePasswordValidation (Method) <a name="DisablePasswordValidation"></a> 

 Disables any password validation.
 

#### Syntax
```
[Scope('OnPrem')]
procedure DisablePasswordValidation()
```
### DisablePasswordConfirmation (Method) <a name="DisablePasswordConfirmation"></a> 

 Disables any password confirmation, it makes the Confirm Password field on the page hidden.
 

#### Syntax
```
[Scope('OnPrem')]
procedure DisablePasswordConfirmation()
```

## Change Password (Report 9810)

 Report to change the current user's login password for OnPrem scenarios.
 

