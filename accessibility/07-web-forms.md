# Web Forms

- Navigating web forms
  - Vision impaired people might rely on screen readers,
  - Cognitive impaired people may rely on clear labels...
- `<label>`, `for`, `id`
- Input data formats like date / text validations / maxlength...
  - Extra constraint info provided in the label. `<label for="dob">Date of Birth (dd/mm/yyyy)</label>`
- Required input
  - red asterisk is not accessible enough for screen readers / color impaired users.
  - `<label for="dob">Date of Birth (dd/mm/yyyy required)</label>`
  - Add `required` but avoid `optional` on the label. The user only has to know what is needed to successfully submit a form.
- Grouping related controls - `fieldset & legend`
  - Gives better description and context for radio btns, checkbox controls...
- Error handling
  - Visual error message may not be announced by the screen reader or its relationship with the input control may not be well established.
  - Add accessible inline error messages within the label element.
    - This is not the only way, this is just a complementary way. Use it by combining with other techniques.
  - Suggest corrections
    - Use simple language.
    - Extend inline error messages within the label element.
  - Validation Summary - primary mechanism for errors identification.
    - Grouping error messages & suggestions at the top of the form.
    - All errors grouped under a list.
    - Red color with prominent borders to show its importance.
    - On submit & error, place focus on the validation summary.
    - Advisory technique.