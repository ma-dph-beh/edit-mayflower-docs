# Pagination

## Overview

Pagination is used to aid users when navigating between a large number of items and should be leverage when there are too many items to show at once. This will be most useful in things like table listings, search results, and directories. What constitutes 'too many' can be influenced by factors like:

* Load time
* Amount of data in each entry
* Screen space

![](../../.gitbook/assets/pagination%20%281%29.png)

The pagination molecule includes:

* **Previous & Next Buttons**: Allow users to move forwards and backwards through a set of items/pages.
* **Pages**: Allow users to navigate to a specific page.
* **Spacers**: Spacer are used to truncate between pages, if numerous.

### Accessibility & Best Practices

## Code

### Pagination

{% tabs %}
{% tab title="HTML" %}
```markup
<div class="ma__pagination js-pagination">
  <div class="ma__pagination__container">
    <button class="ma__pagination__prev js-pagination-prev" type="button">
      Previous
    </button>
    <button class="ma__pagination__page js-pagination-page" type="button" data-page="1">1</button>
    <span class="ma__pagination__spacer">&hellip;</span>
    <button class="ma__pagination__page js-pagination-page" type="button" data-page="3">3</button>
    <button class="ma__pagination__page js-pagination-page is-active" type="button" data-page="4">4</button>
    <button class="ma__pagination__page js-pagination-page" type="button" data-page="5">5</button>
    <span class="ma__pagination__spacer">&hellip;</span>
    <button class="ma__pagination__page js-pagination-page" type="button" data-page="10">10</button>
    <button class="ma__pagination__next js-pagination-next" type="button">
      Next
    </button>
  </div>
</div>
```
{% endtab %}

{% tab title="React" %}
[Pagination in React](https://mayflower-react.digital.mass.gov/?knob-href=%23&knob-info=&knob-pagination.pages=[{"active"%3Afalse%2C"text"%3A"1"%2C"ariaLabel"%3A"Go%20to%20Search%20Results%20Page%201"}%2C{"active"%3Atrue%2C"text"%3A"spacer"}%2C{"active"%3Afalse%2C"text"%3A"3"%2C"ariaLabel"%3A"Go%20to%20Search%20Results%20Page%203"}%2C{"active"%3Atrue%2C"text"%3A"4"%2C"ariaLabel"%3A"Go%20to%20Search%20Results%20Page%204"}%2C{"active"%3Afalse%2C"text"%3A"5"%2C"ariaLabel"%3A"Go%20to%20Search%20Results%20Page%205"}%2C{"active"%3Afalse%2C"text"%3A"spacer"}%2C{"active"%3Afalse%2C"text"%3A"10"%2C"ariaLabel"%3A"Go%20to%20Search%20Results%20Page%2010"}]&knob-ButtonSearch.text=Search&knob-pagination.next.text=Next&knob-pagination.prev.text=Previous&knob-HeaderSearch.defaultText=&knob-HeaderSearch.withOrgDropdown=true&knob-pagination.prev.ariaLabel=Go%20to%20Previous%20Search%20Results%20Page&knob-pagination.next.ariaLabel=Go%20to%20Next%20Search%20Results%20Page&knob-ButtonSearch.ariaLabel=Search&knob-tableOptions.feeTable={"head"%3A{"rows"%3A[{"rowSpanOffset"%3Afalse%2C"cells"%3A[{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"Type"}%2C{"heading"%3Atrue%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"Name"}%2C{"heading"%3Atrue%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"Fee"}]}]}%2C"bodies"%3A[{"rows"%3A[{"rowSpanOffset"%3Afalse%2C"cells"%3A[{"heading"%3Atrue%2C"colspan"%3A""%2C"rowspan"%3A"4"%2C"text"%3A"Freshwater%20Fishing"}%2C{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"Resident%20Citizen%20or%20Non-Resident%20Fishing"}%2C{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"%2427.50"}]}%2C{"rowSpanOffset"%3Atrue%2C"cells"%3A[{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"Resident%20Citizen%20or%20Non-Resident%20Minor%20Fishing%20%28Age%2015-17%29"}%2C{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"FREE"}]}%2C{"rowSpanOffset"%3Atrue%2C"cells"%3A[{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"Resident%20Citizen%20Fishing%20%28Age%2065-69%29"}%2C{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"%2416.25"}]}%2C{"rowSpanOffset"%3Atrue%2C"cells"%3A[{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"Resident%20Citizen%20Fishing%20%28Aged%2070%20or%20Over%29"}%2C{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"FREE"}]}]}%2C{"rows"%3A[{"rowSpanOffset"%3Afalse%2C"cells"%3A[{"heading"%3Atrue%2C"colspan"%3A""%2C"rowspan"%3A"4"%2C"text"%3A"Hunting"}%2C{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"Resident%20Citizen%20Hunting"}%2C{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"%2427.50"}]}%2C{"rowSpanOffset"%3Atrue%2C"cells"%3A[{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"Resident%20Citizen%20Hunting%2C%20%28Age%2065-69%29"}%2C{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"%2416.25"}]}%2C{"rowSpanOffset"%3Atrue%2C"cells"%3A[{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"Resident%20and%20Non-Resident%20Citizen%20Hunting"}%2C{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"FREE"}]}%2C{"rowSpanOffset"%3Atrue%2C"cells"%3A[{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"Resident%20Hunting"}%2C{"heading"%3Afalse%2C"colspan"%3A""%2C"rowspan"%3A""%2C"text"%3A"%2427.50"}]}]}]}&knob-button.href=https%3A%2F%2Fmass.gov&knob-HeaderSearch.placeholder=Search%20Mass.gov&knob-button.text=button&knob-button.info=this%20will%20be%20the%20tooltip%20text%20on%20hover&knob-ButtonWithIcon.text=BUTTON&knob-HeaderSearch.buttonSearch.ariaLabel=Search&knob-HeaderSearch.orgDropdown.inputText={"boxed"%3Atrue%2C"label"%3Anull%2C"placeholder"%3A"Search%20an%20organization..."%2C"id"%3A"org-typeahead"%2C"options"%3A[{"text"%3A""%2C"value"%3A""}%2C{"text"%3A"Org%20Having%20%28Parentheses%20in%20the%20Name%29"%2C"value"%3A"org-having-parentheses-in-the-name"}%2C{"text"%3A"Attorney%20General's%20Office"%2C"value"%3A"attorney-general-office"}%2C{"text"%3A"Governor's%20Office"%2C"value"%3A"governors-office"}%2C{"text"%3A"Bureau%20of%20Environmental%20Health"%2C"value"%3A"bureau-of-environmental-health"}%2C{"text"%3A"Department%20of%20Conservation%20%26%20Recreation"%2C"value"%3A"department-of-conservation--recreation"}%2C{"text"%3A"Department%20of%20Unemployment%20Assistance"%2C"value"%3A"department-of-unemployment-assistance"}%2C{"text"%3A"495%2FMetroWest%20Suburban%20Edge%20Community%20Commission"%2C"value"%3A"495metrowest-suburban-edge-community-commission"}%2C{"text"%3A"Administrative%20Council%20on%20Toxics%20Use%20Reduction"%2C"value"%3A"administrative-council-on-toxics-use-reduction"}%2C{"text"%3A"Advisory%20Committee%20to%20the%20Administrative%20Council%20on%20Toxics%20Use%20Reduction"%2C"value"%3A"advisory-committee-to-the-administrative-council-on-toxics-use-reduction"}%2C{"text"%3A"Alcoholic%20Beverages%20Control%20Commission"%2C"value"%3A"alcoholic-beverages-control-commission"}%2C{"text"%3A"Appeals%20Court"%2C"value"%3A"appeals-court"}%2C{"text"%3A"Architectural%20Access%20Board"%2C"value"%3A"architectural-access-board"}%2C{"text"%3A"Berkshire%20District%20Attorney%20Paul%20J.%20Caccaviello"%2C"value"%3A"berkshire-district-attorney-paul-j-caccaviello"}%2C{"text"%3A"Board%20of%20Registration%20in%20Dentistry"%2C"value"%3A"board-of-registration-in-dentistry"}%2C{"text"%3A"Board%20of%20Registration%20in%20Medicine"%2C"value"%3A"board-of-registration-in-medicine"}]%2C"selected"%3A""}&knob-button.outline=true&knob-HeaderSearch.orgDropdown.dropdownButton={"text"%3A"All%20Organizations"%2C"capitalized"%3Atrue}&knob-linkText=Lorem%20ipsum%20dolor%20sit%20amet&knob-HeaderSearch.buttonSearch.text=Search&knob-ButtonWithIcon.icon=chevron&selectedKind=molecules&selectedStory=Pagination&full=0&addons=1&stories=1&panelRight=0&addonPanel=storybooks%2Fstorybook-addon-knobs)
{% endtab %}

{% tab title="Twig PL" %}
[Pagination in Pattern Lab](https://mayflower.digital.mass.gov/?p=molecules-pagination)
{% endtab %}
{% endtabs %}

## Style

### Classnames

| **Name** | **scss Modifiers** |
| :--- | :--- |
| Container | .ma\_\_pagination .ma\_\_pagination\_\_container |
| Next | .ma\_\_pagination\_\_next |
| Spacer | .ma\_\_pagination\_\_spacer |
| Page | .ma\_\_pagination\_\_page |
| Previous | .ma\_\_pagination\_\_prev |
