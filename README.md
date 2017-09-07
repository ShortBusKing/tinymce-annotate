# tinymce-annotate
This is the wordpress independant version pulled and changed from v1.1.2 here: https://wordpress.org/plugins/tinymce-annotate/

## Setup example

                tinymce.init({
                      plugins: ['tma_annotate'],
                      external_plugins: {
                          'tma_annotate':'plugins/tinymce-annotate/plugin.js'
                      },
                      menu : {
                            view   : {title : 'View'  , items : 'tma_annotatehide'},
                      }, // currently only annotatehide will show on the menu
                      tma_annotate_user_callback: this.getAnnotateUser.bind(this),
                      toolbar: 'tma_annotate tma_annotatedelete tma_annotatehide'
                });
                
                getAnnotateUser(){
                     return {
                        'ID': '1234',
                        'display_name': 'Test'
                    };
                }
