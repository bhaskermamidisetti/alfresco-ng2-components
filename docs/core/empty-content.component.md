---
Added: v2.4.0
Status: Active
Last reviewed:
---

# Empty Content Component

Provides a generic "Empty Content" UI and can used as a placeholder for components that need to show different content when being empty.

## Properties

| Name | Type | Description |
| --- | --- | --- |
| icon | string | Material Icon to use |
| title | string | String or Resource Key for the title |
| subtitle | string | String or Resource Key for the subtitle |

## Examples

```html
<adf-document-list>
    <empty-folder-content>
        <ng-template>
            <adf-empty-content
                icon="star_rate"
                title="APP.BROWSE.FAVORITES.EMPTY_STATE.TITLE"
                subtitle="APP.BROWSE.FAVORITES.EMPTY_STATE.TEXT">
            </adf-empty-folder>
        </ng-template>
    </empty-folder-content>
</adf-document-list>
```

![Favorites screen](../docassets/images/empty-content-favorites.png)

You can also use multiple lines instead of the subtitle section:

```html
<adf-document-list>
    <empty-folder-content>
        <ng-template>
            <adf-empty-content
                icon="delete"
                title="APP.BROWSE.TRASHCAN.EMPTY_STATE.TITLE">
                <p class="adf-empty-content__text">{{ 'APP.BROWSE.TRASHCAN.EMPTY_STATE.FIRST_TEXT' | translate }}</p>
                <p class="adf-empty-content__text">{{ 'APP.BROWSE.TRASHCAN.EMPTY_STATE.SECOND_TEXT' | translate }}</p>
            </adf-empty-content>
        </ng-template>
    </empty-folder-content>
</adf-document-list>
```

![Trashcan screen](../docassets/images/empty-content-trashcan.png)