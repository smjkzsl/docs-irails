# Views
* Views files are generally referred to as Jinjia2 Template files, which are called by the Controller. The Views folder is always located in the Views directory under the App folder, and is stored separately by the Controller name (naked name). If a Controller is defined with a version (using @ route (version="v1.0") or similar notation), then the version name will be used under the Controller name and stored separately
* The Views syntax is the same as the Jinja2 Template syntax, but the default configuration variable for IRails is ' ${variable or statement} ', but these can be configured in the configuration file
* Link: [Jinja Template Documents](https://jinja.palletsprojects.com/en/3.1.x/templates/)

        file configs/general.yaml:

        view:
            jinja2:
                block_end_string: '%}'
                block_start_string: '{%'
                comment_end_string: '#}'
                comment_start_string: '{#'
                variable_end_string: '}'
                variable_start_string: '${'
            static_format:   ## This section defines the file formats that will be rendered using Jinja2. If not listed in this list, rendering will not be performed           
            - vue
            - html