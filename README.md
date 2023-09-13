# API Integration Documentation

This comprehensive documentation is intended for partners who are integrating their systems with your Django-based system. It provides a detailed overview of available API endpoints, request methods, request payloads, and response payloads for each specified model. Properly integrating with these endpoints will enable you to access and manipulate data within your system.

### Authentication

Before accessing the API, ensure that your system is configured to use token-based authentication. Clients should include an `Authorization` header with a valid token to authenticate their requests.

## Owner API

### Retrieve Owners

#### GET /api/owners/
- **Description**: Retrieve a list of all owners.
- **Response**:
  - `200 OK`: Returns a JSON array containing owner objects.
    ```json
    [
        {
            "id": "1e56c59d-1c2e-4a9b-869d-34123c9a8b6e",
            "full_name": "John Doe",
            "nationality": "US",
            "email": "johndoe@example.com",
            "address": "123 Main St",
            "town": "Anytown",
            "officer": "John Smith"
        },
        {
            "id": "e4d8c7f1-b4fc-4aa2-8e78-2b40f01d8764",
            "full_name": "Jane Smith",
            "nationality": "UK",
            "email": "janesmith@example.com",
            "address": "456 Oak Ave",
            "town": "Othertown",
            "officer": "Jane Johnson"
        }
    ]
    ```
  - `404 Not Found`: Returned if no owners are found.

#### Retrieve Owner Details by ID

#### GET /api/owners/{id}/
- **Description**: Retrieve details of a specific owner by their unique ID.
- **Parameters**:
  - `id` (uuid): The unique identifier of the owner.
- **Response**:
  - `200 OK`: Returns a JSON object representing the owner.
    ```json
    {
        "id": "1e56c59d-1c2e-4a9b-869d-34123c9a8b6e",
        "full_name": "John Doe",
        "nationality": "US",
        "email": "johndoe@example.com",
        "address": "123 Main St",
        "town": "Anytown",
        "officer": "John Smith"
    }
    ```
  - `404 Not Found`: Returned if the owner with the specified ID is not found.

## Owner Detail Document API

### Retrieve Owner Detail Documents

#### GET /api/owner-detail-documents/
- **Description**: Retrieve a list of all owner detail documents.
- **Response**:
  - `200 OK`: Returns a JSON array containing owner detail document objects.
    ```json
    [
        {
            "id": "4a7e1c3b-87d9-4f9f-b5ca-5b81b6e972c1",
            "name": "Document 1",
            "file": "document_1.pdf",
            "owner": "John Doe"
        },
        {
            "id": "b9b29411-26cb-4cdd-9887-ef56d03e3a2d",
            "name": "Document 2",
            "file": "document_2.pdf",
            "owner": "Jane Smith"
        }
    ]
    ```
  - `404 Not Found`: Returned if no owner detail documents are found.

#### Retrieve Owner Detail Document by ID

#### GET /api/owner-detail-documents/{id}/
- **Description**: Retrieve details of a specific owner detail document by its unique ID.
- **Parameters**:
  - `id` (uuid): The unique identifier of the owner detail document.
- **Response**:
  - `200 OK`: Returns a JSON object representing the owner detail document.
    ```json
    {
        "id": "4a7e1c3b-87d9-4f9f-b5ca-5b81b6e972c1",
        "name": "Document 1",
        "file": "document_1.pdf",
        "owner": "John Doe"
    }
    ```
  - `404 Not Found`: Returned if the owner detail document with the specified ID is not found.

## Agency API

### Retrieve Agencies

#### GET /api/agencies/
- **Description**: Retrieve a list of all agencies.
- **Response**:
  - `200 OK`: Returns a JSON array containing agency objects.
    ```json
    [
        {
            "id": "3c1c5b9e-98a7-4b6a-8d9c-d8b74e4c691e",
            "agency_name": "ABC Insurance",
            "nature_organization": "Public Limited Company",
            "date_of_registration": "2022-01-15",
            "location_house": "456 Oak St",
            "location_street": "Suite 101",
            "location_ward": "Westward",
            "location_district": "District 1",
            "location_region": "Region 2",
            "contact_address": "789 Elm Rd",
            "contact_telephone": "+123456789",
            "contact_mobile": "+987654321",
            "contact_email": "info@abcinsurance.com",
            "iaat_membership_number": "IAAT12345",
            "tira_registration_number": "TIRA67890"
        },
        {
            "id": "7f1c8d4e-b9f4-4aa2-8e78-2b40f01d8764",
            "agency_name": "XYZ Insurers",
            "nature_organization": "Private Limited Company",
            "date_of_registration": "2021-05-20",
            "location_house": "123 Main St",
            "location_street": "Floor 5",
            "location_ward": "Eastward",
            "location_district": "District 2",
            "location_region": "Region 1",
            "contact_address": "456 Maple Ave",
            "contact_telephone": "+987654321",
            "contact_mobile": "+123456789",
            "contact_email": "info@xyzinsurers.com",
            "iaat_membership_number": "IAAT54321",
            "tira_registration_number": "TIRA98765"
        }
    ]
    ```
  - `404 Not Found`: Returned if no agencies are found.

#### Retrieve Agency Details by ID

#### GET /api/agencies/{id}/
- **Description**: Retrieve details of a specific agency by its unique ID.
- **Parameters**:
  - `id` (uuid): The unique identifier of the agency.
- **Response**:
  - `200 OK`: Returns a JSON object representing the agency.
    ```json
    {
        "id": "3c1c5b9e-98a7-4b6a-8d9c-d8b74e4c691e",
        "agency_name": "ABC Insurance",
        "nature_organization": "Public Limited Company",
        "date_of_registration": "2022-01-15",
        "location_house": "456 Oak St",
        "location_street": "Suite 101",
        "location_ward": "Westward",
        "location_district": "District 1",
        "location_region": "Region 2",
        "contact_address": "789 Elm Rd",
        "contact_telephone": "+123456789",
        "contact_mobile": "+987654321",
        "contact_email": "info@abcinsurance.com",
        "iaat_membership_number": "IAAT12345",
        "tira_registration_number": "TIRA67890"
    }
    ```
  - `404 Not Found`: Returned if the agency with the specified ID is not found.

## Officer API

### Retrieve Officers

#### GET /api/officers/
- **Description**: Retrieve a list of all officers.
- **Response**:
  - `200 OK`: Returns a JSON array containing officer objects.
    ```json
    [
        {
            "id": "1f56c59d-1c2e-4a9b-869d-34123c9a8b6e",
            "first_name": "John",
            "last_name": "Smith",
            "qualification": "MBA",
            "email": "johnsmith@example.com",
            "phone1": "+123456789",
            "phone2": "+987654321",
            "agency": "ABC Insurance"
        },
        {
            "id": "e4d8c7f1-b4fc-4aa2-8e78-2b40f01d8764",
            "first_name": "Jane",
            "last_name": "Johnson",
            "qualification": "PhD",
            "email": "janejohnson@example.com",
            "phone1": "+987654321",
            "phone2": "+123456789",
            "agency": "XYZ Insurers"
        }
    ]
    ```
  - `404 Not Found`: Returned if no officers are found.

#### Retrieve Officer Details by ID

#### GET /api/officers/{id}/
- **Description**: Retrieve details of a specific officer by their unique ID.
- **Parameters**:
  - `id` (uuid): The unique identifier of the officer.
- **Response**:
  - `200 OK`: Returns a JSON object representing the officer.
    ```json
    {
        "id": "1f56c59d-1c2e-4a9b-869d-34123c9a8b6e",
        "first_name": "John",
        "last_name": "Smith",
        "qualification": "MBA",
        "email": "johnsmith@example.com",
        "phone1": "+123456789",
        "phone2": "+987654321",
        "agency": "ABC Insurance"
    }
    ```
  - `404 Not Found`: Returned if the officer with the specified ID is not found.

## Principal Officer Document API

### Retrieve Principal Officer Documents

#### GET /api/principal-officer-documents/
- **Description**: Retrieve a list of all principal officer documents.
- **Response**:
  - `200 OK`: Returns a JSON array containing principal officer document objects.
    ```json
    [
        {
            "id": "4a7e1c3b-87d9-4f9f-b5ca-5b81b6e972c1",
            "name": "Document 1",
            "document": "document_1.pdf",
            "officer": "John Smith"
        },
        {
            "id": "b9b29411-26cb-4cdd-9887-ef56d03e3a2d",
            "name": "Document 2",
            "document": "document_2.pdf",
            "officer": "Jane Johnson"
        }
    ]
    ```
  - `404 Not Found`: Returned if no principal officer documents are found.

#### Retrieve Principal Officer Document by ID

#### GET /api/principal-officer-documents/{id}/
- **Description**: Retrieve details of a specific principal officer document by its unique ID.
- **Parameters**:
  - `id` (uuid): The unique identifier of the principal officer document.
- **Response**:
  - `200 OK`: Returns a JSON object representing the principal officer document.
    ```json
    {
        "id": "4a7e1c3b-87d9-4f9f-b5ca-5b81b6e972c1",
        "name": "Document 1",
        "document": "document_1.pdf",
        "officer": "John Smith"
    }
    ```
  - `404 Not Found`: Returned if the principal officer document with the specified ID is not found.

## Owner Detail Certificate API

### Create Owner Detail Certificate

#### POST /api/owner-detail-certificates/
- **Description**: Create a new owner detail certificate.
- **Request Body**: JSON object containing the following fields:
  - `certificate_id` (string): The certificate ID.
  - `certificate` (file): The certificate file.
  - `comments` (string, optional): Comments about the certificate.
  - `owner` (uuid): The ID of the owner to associate with the certificate.
- **Response**:
  - `201 Created`: Returns a JSON object representing the created owner detail certificate.
    ```json
    {
        "id": "4a7e1c3b-87d9-4f9f-b5ca-5b81b6e972c1",
        "certificate_id": "CERT123456",
        "certificate": "certificate.pdf",
        "comments": "Certificate for John Doe",
        "owner": "John Doe"
    }
    ```
  - `400 Bad Request`: Returned if the request data is invalid.
  - `404 Not Found`: Returned if the specified owner ID is not found.

This API integration documentation outlines the endpoints, their functionalities, and the expected request and response structures. Ensure that your integration conforms to these specifications to interact seamlessly with our Django-based system.
