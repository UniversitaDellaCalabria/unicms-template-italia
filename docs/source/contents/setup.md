Install
-------

````
pip install unicms-template-italia
````

Setup
-----

Add these block positions in your ```settings.py```

````
CMS_TEMPLATE_BLOCK_SECTIONS = (
                                ('pre-head', _('Pre-Header')),

                                ('head', _('Header')),

                                ('menu-1', _('Navigation Main Menu')),
                                ('menu-2', _('Navigation Menu 2')),
                                ('menu-3', _('Navigation Menu 3')),
                                ('menu-4', _('Navigation Menu 4')),

                                ('banner', _('Banner/Slider')),
                                ('slider-2', _('Carousel/Slider 2')),

                                ('pre-footer', _('Pre-Footer')),
                                ('footer', _('Footer')),
                                ('post-footer', _('Post-Footer')),

                                # breadcrumbs
                                ('breadcrumbs', _('Breadcrumbs')),

                                # section 1
                                ('section-1',
                                    (
                                       ('1-top-a', _('Section 1 - Top A')),
                                       ('1-top-b', _('Section 1 - Top B')),
                                       ('1-top-c', _('Section 1 - Top C')),
                                       ('1-mid-top-a', _('Section 1 - Middle Top A')),
                                       ('1-mid-top-b', _('Section 1 - Middle Top B')),
                                       ('1-mid-top-c', _('Section 1 - Middle Top C')),
                                       ('1-left-a', _('Section 1 - Left A')),
                                       ('1-left-b', _('Section 1 - Left B')),
                                       ('1-center-top-a', _('Section 1 - Center Top A')),
                                       ('1-center-top-b', _('Section 1 - Center Top B')),
                                       ('1-center-top-c', _('Section 1 - Center Top C')),
                                       ('1-center-content', _('Section 1 - Center Content')),
                                       ('1-center-bottom-a', _('Section 1 - Center Bottom A')),
                                       ('1-center-bottom-b', _('Section 1 - Center Bottom B')),
                                       ('1-center-bottom-c', _('Section 1 - Center Bottom C')),
                                       ('1-right-a', _('Section 1 - Right A')),
                                       ('1-right-b', _('Section 1 - Right B')),
                                       ('1-mid-bottom-a', _('Section 1 - Middle Bottom A')),
                                       ('1-mid-bottom-b', _('Section 1 - Middle Bottom B')),
                                       ('1-mid-bottom-c', _('Section 1 - Middle Bottom C')),
                                       ('1-bottom-a', _('Section 1 - Bottom A')),
                                       ('1-bottom-b', _('Section 1 - Bottom B')),
                                       ('1-bottom-c', _('Section 1 - Bottom C')),
                                    )
                                ),

                                # section 2
                                ('section-2',
                                    (
                                       ('2-top-a', _('Section 2 - Top A')),
                                       ('2-top-b', _('Section 2 - Top B')),
                                       ('2-top-c', _('Section 2 - Top C')),
                                       ('2-mid-top-a', _('Section 2 - Middle Top A')),
                                       ('2-mid-top-b', _('Section 2 - Middle Top B')),
                                       ('2-mid-top-c', _('Section 2 - Middle Top C')),
                                       ('2-left-a', _('Section 2 - Left A')),
                                       ('2-left-b', _('Section 2 - Left B')),
                                       ('2-center-top-a', _('Section 2 - Center Top A')),
                                       ('2-center-top-b', _('Section 2 - Center Top B')),
                                       ('2-center-top-c', _('Section 2 - Center Top C')),
                                       ('2-center-content', _('Section 2 - Center Content')),
                                       ('2-center-bottom-a', _('Section 2 - Center Bottom A')),
                                       ('2-center-bottom-b', _('Section 2 - Center Bottom B')),
                                       ('2-center-bottom-c', _('Section 2 - Center Bottom C')),
                                       ('2-right-a', _('Section 2 - Right A')),
                                       ('2-right-b', _('Section 2 - Right B')),
                                       ('2-mid-bottom-a', _('Section 2 - Middle Bottom A')),
                                       ('2-mid-bottom-b', _('Section 2 - Middle Bottom B')),
                                       ('2-mid-bottom-c', _('Section 2 - Middle Bottom C')),
                                       ('2-bottom-a', _('Section 2 - Bottom A')),
                                       ('2-bottom-b', _('Section 2 - Bottom B')),
                                       ('2-bottom-c', _('Section 2 - Bottom C')),
                                    )
                                ),

                                # section 1
                                ('section-3',
                                    (
                                       ('3-top-a', _('Section 3 - Top A')),
                                       ('3-top-b', _('Section 3 - Top B')),
                                       ('3-top-c', _('Section 3 - Top C')),
                                       ('3-mid-top-a', _('Section 3 - Middle Top A')),
                                       ('3-mid-top-b', _('Section 3 - Middle Top B')),
                                       ('3-mid-top-c', _('Section 3 - Middle Top C')),
                                       ('3-left-a', _('Section 3 - Left A')),
                                       ('3-left-b', _('Section 3 - Left B')),
                                       ('3-center-top-a', _('Section 3 - Center Top 1')),
                                       ('3-center-top-b', _('Section 3 - Center Top 2')),
                                       ('3-center-top-c', _('Section 3 - Center Top 3')),
                                       ('3-center-content', _('Section 3 - Center Content')),
                                       ('3-center-bottom-a', _('Section 3 - Center Bottom A')),
                                       ('3-center-bottom-b', _('Section 3 - Center Bottom B')),
                                       ('3-center-bottom-c', _('Section 3 - Center Bottom C')),
                                       ('3-mid-bottom-a', _('Section 3 - Middle Bottom A')),
                                       ('3-mid-bottom-b', _('Section 3 - Middle Bottom B')),
                                       ('3-mid-bottom-c', _('Section 3 - Middle Bottom C')),
                                       ('3-bottom-a', _('Section 3 - Bottom A')),
                                       ('3-bottom-b', _('Section 3 - Bottom B')),
                                       ('3-bottom-c', _('Section 3 - Bottom C')),
                                    )
                                ),
                              )
````

Run ```./manage.py unicms_collect_templates``` to load new template files.
