# Search kit

Search kit is a new search interface which as of writing (5.36) is
in beta mode. It ships as an extension when you can enable on 
the extensions screen in releases from 5.29 onwards. However it has
developed rapidly and we strongly recommend that if you are exploring
it you do so on the latest version of CiviCRM. The functionality
that is in this section is based on CiviCRM 5.36 and may not
be present in earlier versions. It may also change visually.

!!! note Search kit ships as an extension as part of our strategy of
putting significant functionality leaps into extensions rather than 
overhauling existing code. This allows us to demarcate rapidly evolving
code and to keep long-standing code more stable. People can opt into 
the extension or not. However it is maintained as part of core against
the specific release it ships with (as it is closely tied to apiv4 
functionality).

# Search components

There are 3 components to search kit. Depending on what you are doing you
may not use all 3

1) The search screen 
   - this is where the search criteria and available fields are configured
2) Search displays
   - a search can have no search displays or it can have one or multiple.
    search displays currently available are table views, list views or smart 
     groups
3) Search form
   - in order to add a search form it is necessary to have the form
    builder (afform gui) extension that ships with core enabled.

# The search screen

The search screen is reached from the search listing page (Search->Search Kit)
![img.png](../img/the-user-interface/search-kit/search-listing.png)

The screen below shows a very basic search for contacts with no entry for
camera skill level. This is 
![img.png](../img/the-user-interface/search-kit/basic-search.png)

# Search displays

Search displays are added from the Search screen once a search has 
been saved.

![img.png](../img/the-user-interface/search-kit/search-display.png)

# Search forms

Search forms are forms that can be exposed as web pages
or as dashlets (in future other options will exist). They 
can have exposed filters. For example

![img.png](../img/the-user-interface/search-kit/search-dashlet.png)

They are added via the search listing

![img.png](../img/the-user-interface/search-kit/add-form.png)

