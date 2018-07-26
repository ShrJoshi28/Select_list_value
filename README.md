# Select_list_value
#how to set the default value select list is select when click on reset button


#html code
<div class="form-group">
                  <label>Text Justification
                    <sup class="mandatory">*</sup>
                  </label>
                  <select class="form-control" style="width: 100%;" name="Text_Justification" #Text_Justification="ngModel" [(ngModel)]="languageService.selectedLanguage.Text_Justification"
                    required>
                    <option [ngValue]="null" disabled selected>--Select--</option>
                    <option value="L">Left</option>
                    <option value="R">Right</option>
                  </select>
                  <div class="validation-error" *ngIf="Text_Justification.invalid && Text_Justification.touched">Text Justification is required</div>
                </div>
                
                
                
                #component.ts
                # on reset button function
                
                
                resetForm(form?: NgForm) {
    if (form != null)
      form.reset()
    this.languageService.selectedLanguage = {
      Language_Code: '',
      Language_Name: '',
      Text_Justification:null,    //it set to default value to select list after click on reset buuton
    }
  }
