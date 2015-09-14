# swagger-soap-ui

## Version 0.1 unstable
Version ui only SOAP webservice 
to REST
https://github.com/swagger-api/swagger-ui

Swagger UI Version | Release Date | Swagger Spec compatibility | Notes | Status
------------------ | ------------ | -------------------------- | ----- | ------
0.1                | 2015-01-29   | 0.1                        | [tag v0.1](https://github.com/samuelsantosdev/swagger-soap-ui)|


##Examples

      into onComplete SwaggerUi
      $('input.parameter').swaggerSOAP({
        'startDag' : 'SOAP-ENV',
        'swaggerUi' : swaggerUi,
        'swaggerApi' : swaggerApi
      });

      Example:
      $(function () {
        var url = 'http://localhost/ui-soap/resolve.json';		
        window.swaggerUi = new SwaggerUi({
          url: url,
          dom_id: "swagger-ui-container",
          supportedSubmitMethods: ['post'],
          onComplete: function(swaggerApi, swaggerUi){
          
          $('input.parameter').swaggerSOAP({
            'startDag' : 'SOAP-ENV',
            'swaggerUi' : swaggerUi,
            'swaggerApi' : swaggerApi
          });
          
          },
          onFailure: function(data) {
            console.log("Erro to load");
          },
          docExpansion: "list",
          sorter : "alpha"
        });
        window.swaggerUi.load();
      });
