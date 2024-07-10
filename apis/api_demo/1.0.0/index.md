---
# NOTICE: Copyright 2024 Talend SA, Talend, Inc., and affiliates. All Rights Reserved. Customer’s use of the software contained herein is subject to the terms and conditions of the Agreement between Customer and Talend.
layout: "apiDefinition_1.1.0"
api-definition:
  specVersion: "4.1.0"
  info:
    name: "API_DEMO"
    version: "1.0.0"
    description: "No description"
    license: {}
    contact: {}
  contract:
    baseUrls:
    - url: "https://2ig912ru1eka29u.eu.api-mocks.com"
      description: "This is your API mock endpoint. When called, it will simulate the behavior of your API."
      isPublished: true
    - url: "http://www.das.com"
      description: "Das"
      isPublished: true
    mediaTypes:
    - "application/json"
    sections:
    - name: "Objects"
      elementOrder:
      - "#/contract/types/be4cb0d4-957e-4fc0-83e0-af65db44b0d3"
      - "#/contract/types/668e95b9-73a6-4da1-8053-71734a7a2671"
    - name: "Operations"
      description: "Define operation that we can do with our API"
      elementOrder:
      - "#/contract/resources/996b150e-082e-4681-9afd-969f2f2659ff"
      - "#/contract/resources/a027eb2e-0120-48b1-b978-0fa883747cfc"
    - name: "About"
      description: "Help"
      elementOrder:
      - "#/contract/texts/9712a5fd-2227-4c56-a163-572d5a4a6d4e"
    resources:
      "996b150e-082e-4681-9afd-969f2f2659ff":
        path: "/Customers"
        section: "#/contract/sections/577c3b7a-6fbf-4d34-b78f-cd87dc398789"
        operations:
          "92a3d96b-0a8c-4d09-9693-4a54e26b73de":
            name: "List Customers"
            method: "GET"
            description: "List All customers"
            responses:
              e26d65a6-9d89-4e4f-a3d9-03861854d551:
                status: "200"
                description: "Result OK"
                bodies:
                - type: "#/contract/types/668e95b9-73a6-4da1-8053-71734a7a2671"
                  description: "Return All Customers"
                  examples:
                  - value: |-
                      {
                      "Customers":[
                          {
                              "ID": "1234",
                              "NAME": "Alice",
                              "LAST_NAME": "Khayati",
                              "MAIL": "Sofiene.Khayati@agilos.com",
                              "PHONE": "0465784646",
                              "STREET_NUMBER": "11",
                              "CITY": "Brussels",
                              "DEPARTMENT": "Brussels",
                              "REGION": "Brussels",
                              "COUNTRY": "Belgium",
                              "POSTAL_CODE": "1000"
                          },
                          {
                              "ID": "1920",
                              "NAME": "Sofiene",
                              "LAST_NAME": "Khayati",
                              "MAIL": "Sofiene.Khayati@agilos.com",
                              "PHONE": "0465784646",
                              "STREET_NUMBER": "12",
                              "CITY": "Ixelles",
                              "DEPARTMENT": "Brussels",
                              "REGION": "Brussels",
                              "COUNTRY": "Belgium",
                              "POSTAL_CODE": "1050"
                          },
                          {
                              "ID": "1920",
                              "NAME": "Lina",
                              "LAST_NAME": "Khayati",
                              "MAIL": "Sofiene.Khayati@agilos.com",
                              "PHONE": "0465784646",
                              "STREET_NUMBER": "12",
                              "CITY": "Ixelles",
                              "DEPARTMENT": "Brussels",
                              "REGION": "Brussels",
                              "COUNTRY": "Belgium",
                              "POSTAL_CODE": "1050"
                          },
                          {
                              "ID": "1920",
                              "NAME": "Henri",
                              "LAST_NAME": "Van Den Berghe",
                              "MAIL": "Sofiene.Khayati@agilos.com",
                              "PHONE": "0465784646",
                              "STREET_NUMBER": "1",
                              "CITY": "Saint Gilles",
                              "DEPARTMENT": "Brussels",
                              "REGION": "Brussels",
                              "COUNTRY": "Belgium",
                              "POSTAL_CODE": "1060"
                          }
                      ]
                      }
      a027eb2e-0120-48b1-b978-0fa883747cfc:
        path: "/Customer"
        section: "#/contract/sections/577c3b7a-6fbf-4d34-b78f-cd87dc398789"
        operations:
          "27b45d47-012d-4316-989d-792cd3d439af":
            name: "Add Customer"
            method: "POST"
            bodies:
            - type: "#/contract/types/be4cb0d4-957e-4fc0-83e0-af65db44b0d3"
              examples:
              - value: |-
                  {"ID": "1920",
                  "NAME": "Sofiene",
                  "LAST NAME": "Khayati",
                  "MAIL": "Sofiene.Khayati@agilos.com",
                  "PHONE": "0465784646",
                  "STREET_NUMBER": "12",
                  "CITY": "Ixelles",
                  "DEPARTMENT": "Brussels",
                  "REGION": "Brussels",
                  "COUNTRY": "Belgium",
                  "POSTAL_CODE": "1050"}
            responses:
              "582859b3-b64f-4ec7-a392-37be19a01ef9":
                status: "200"
                description: "Customer Added"
    types:
      be4cb0d4-957e-4fc0-83e0-af65db44b0d3:
        name: "Customer"
        type: "OBJECT"
        description: "Customer informations"
        section: "#/contract/sections/0cf12b8a-ed78-44ff-a60e-3276936c40bc"
        required: false
        properties:
        - name: "ID"
          type: "INTEGER"
          description: "Customer ID"
          required: true
        - name: "NAME"
          type: "STRING"
          description: "Customer Name"
          required: true
        - name: "LAST NAME"
          type: "STRING"
          description: "Customer Last Name"
          required: true
        - name: "MAIL"
          type: "STRING"
          description: "Customer Email"
          required: false
        - name: "PHONE"
          type: "STRING"
          description: "Customer Phone"
          required: false
        - name: "STREET_NUMBER"
          type: "STRING"
          description: "Customer Adress Street Number"
          required: false
        - name: "CITY"
          type: "STRING"
          description: "Customer City"
          required: false
        - name: "DEPARTMENT"
          type: "STRING"
          description: "Customer Department"
          required: false
        - name: "REGION"
          type: "STRING"
          description: "Customer Region"
          required: false
        - name: "COUNTRY"
          type: "STRING"
          description: "Customer Country"
          required: false
        - name: "POSTAL_CODE"
          type: "INTEGER"
          description: "Customer Zip Code"
          required: false
        examples:
        - value: "{\r\n\"ID\": \"000001\",\r\n\"NAME\": \"Sofiene\",\r\n\"LAST NAME\": \"Khayati\",\r\n\"MAIL\": \"Sofiene.Khayati@agilos.com\",\r\n\"PHONE\": \"0465784646\",\r\n\"STREET_NUMBER\": \"1\",\r\n\"CITY\": \"Ixelles\",\r\n\"DEPARTMENT\": \"Brussels\",\r\n\"REGION\": \"Brussels\",\r\n\"COUNTRY\": \"Belgium\",\r\n\"POSTAL_CODE\": \"1050\"\r\n}"
      "668e95b9-73a6-4da1-8053-71734a7a2671":
        name: "Customers"
        type: "OBJECT"
        description: "List Customers"
        section: "#/contract/sections/0cf12b8a-ed78-44ff-a60e-3276936c40bc"
        required: false
        properties:
        - name: "Customers"
          type: "ARRAY"
          required: false
          items:
            type: "OBJECT"
            required: false
            properties:
            - name: "ID"
              type: "STRING"
              required: false
            - name: "NAME"
              type: "STRING"
              required: false
            - name: "LAST_NAME"
              type: "STRING"
              required: false
            - name: "MAIL"
              type: "STRING"
              required: false
            - name: "PHONE"
              type: "STRING"
              required: false
            - name: "STREET_NUMBER"
              type: "STRING"
              required: false
            - name: "CITY"
              type: "STRING"
              required: false
            - name: "DEPARTMENT"
              type: "STRING"
              required: false
            - name: "REGION"
              type: "STRING"
              required: false
            - name: "COUNTRY"
              type: "STRING"
              required: false
            - name: "POSTAL_CODE"
              type: "STRING"
              required: false
        examples:
        - value: "{\r\n\"Customers\":[\r\n    {\r\n        \"ID\": \"1234\",\r\n        \"NAME\": \"Alice\",\r\n        \"LAST_NAME\": \"Khayati\",\r\n        \"MAIL\": \"Sofiene.Khayati@agilos.com\",\r\n        \"PHONE\": \"0465784646\",\r\n        \"STREET_NUMBER\": \"11\",\r\n        \"CITY\": \"Brussels\",\r\n        \"DEPARTMENT\": \"Brussels\",\r\n        \"REGION\": \"Brussels\",\r\n        \"COUNTRY\": \"Belgium\",\r\n        \"POSTAL_CODE\": \"1000\"\r\n    },\r\n    {\r\n        \"ID\": \"1920\",\r\n        \"NAME\": \"Sofiene\",\r\n        \"LAST_NAME\": \"Khayati\",\r\n        \"MAIL\": \"Sofiene.Khayati@agilos.com\",\r\n        \"PHONE\": \"0465784646\",\r\n        \"STREET_NUMBER\": \"12\",\r\n        \"CITY\": \"Ixelles\",\r\n        \"DEPARTMENT\": \"Brussels\",\r\n        \"REGION\": \"Brussels\",\r\n        \"COUNTRY\": \"Belgium\",\r\n        \"POSTAL_CODE\": \"1050\"\r\n    },\r\n    {\r\n        \"ID\": \"1920\",\r\n        \"NAME\": \"Lina\",\r\n        \"LAST_NAME\": \"Khayati\",\r\n        \"MAIL\": \"Sofiene.Khayati@agilos.com\",\r\n        \"PHONE\": \"0465784646\",\r\n        \"STREET_NUMBER\": \"12\",\r\n        \"CITY\": \"Ixelles\",\r\n        \"DEPARTMENT\": \"Brussels\",\r\n        \"REGION\": \"Brussels\",\r\n        \"COUNTRY\": \"Belgium\",\r\n        \"POSTAL_CODE\": \"1050\"\r\n    },\r\n    {\r\n        \"ID\": \"1920\",\r\n        \"NAME\": \"Henri\",\r\n        \"LAST_NAME\": \"Van Den Berghe\",\r\n        \"MAIL\": \"Sofiene.Khayati@agilos.com\",\r\n        \"PHONE\": \"0465784646\",\r\n        \"STREET_NUMBER\": \"1\",\r\n        \"CITY\": \"Saint Gilles\",\r\n        \"DEPARTMENT\": \"Brussels\",\r\n        \"REGION\": \"Brussels\",\r\n        \"COUNTRY\": \"Belgium\",\r\n        \"POSTAL_CODE\": \"1060\"\r\n    }\r\n]\r\n}"
    texts:
      "9712a5fd-2227-4c56-a163-572d5a4a6d4e":
        title: "Designed with Talend API Designer"
        content: "**Designed with Talend API Designer**"
        section: "#/contract/sections/0665d612-102d-44cd-bb00-67b587b98cf2"
  components: {}
api-tryin: |-
  {
    "version" : 6,
    "entities" : [ {
      "entity" : {
        "type" : "Project",
        "name" : "API_DEMO 1.0.0",
        "description" : "No description",
        "importedFrom" : "3d54d70e-dd2f-4bb5-b2b8-b8fb3215a10d"
      },
      "children" : [ {
        "entity" : {
          "type" : "Service",
          "name" : "Objects"
        }
      }, {
        "entity" : {
          "type" : "Service",
          "name" : "Operations",
          "description" : "Define operation that we can do with our API"
        },
        "children" : [ {
          "entity" : {
            "type" : "Request",
            "id" : "92a3d96b-0a8c-4d09-9693-4a54e26b73de",
            "name" : "List Customers",
            "description" : "List All customers",
            "uri" : {
              "host" : "${\"BaseUrl\"}",
              "path" : "/Customers"
            },
            "method" : {
              "link" : "",
              "name" : "GET"
            },
            "headers" : [ {
              "enabled" : true,
              "name" : "Accept",
              "value" : "application/json"
            } ],
            "headersType" : "Form"
          }
        }, {
          "entity" : {
            "type" : "Request",
            "id" : "27b45d47-012d-4316-989d-792cd3d439af",
            "name" : "Add Customer",
            "uri" : {
              "host" : "${\"BaseUrl\"}",
              "path" : "/Customer"
            },
            "method" : {
              "link" : "",
              "name" : "POST",
              "requestBody" : true
            },
            "headers" : [ {
              "enabled" : true,
              "name" : "Content-Type",
              "value" : "application/json"
            } ],
            "headersType" : "Form",
            "body" : {
              "bodyType" : "Text",
              "textBody" : "{\"ID\": \"1920\",\n\"NAME\": \"Sofiene\",\n\"LAST NAME\": \"Khayati\",\n\"MAIL\": \"Sofiene.Khayati@agilos.com\",\n\"PHONE\": \"0465784646\",\n\"STREET_NUMBER\": \"12\",\n\"CITY\": \"Ixelles\",\n\"DEPARTMENT\": \"Brussels\",\n\"REGION\": \"Brussels\",\n\"COUNTRY\": \"Belgium\",\n\"POSTAL_CODE\": \"1050\"}"
            }
          }
        } ]
      }, {
        "entity" : {
          "type" : "Service",
          "name" : "About",
          "description" : "Help"
        }
      } ]
    } ],
    "environments" : [ {
      "name" : "API_DEMO 1.0.0",
      "importedFrom" : {
        "projectId" : "3d54d70e-dd2f-4bb5-b2b8-b8fb3215a10d"
      },
      "variables" : {
        "05150db7-e293-47b8-861a-0dc69a5ff23a" : {
          "name" : "BaseUrl",
          "value" : "https://2ig912ru1eka29u.eu.api-mocks.com",
          "enabled" : true,
          "private" : false
        }
      }
    }, {
      "name" : "API_DEMO 1.0.0",
      "importedFrom" : {
        "projectId" : "3d54d70e-dd2f-4bb5-b2b8-b8fb3215a10d"
      },
      "variables" : {
        "7cc7ba68-4742-4fc2-9062-5b558d305b1b" : {
          "name" : "BaseUrl",
          "value" : "http://www.das.com",
          "enabled" : true,
          "private" : false
        }
      }
    } ]
  }
---
