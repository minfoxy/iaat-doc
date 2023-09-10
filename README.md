# API Integration Documentation

This comprehensive documentation is intended for partners who are integrating their systems with our Django-based system. It provides a detailed overview of available API endpoints, request methods, and data descriptions.

## Introduction

Our Django system exposes a RESTful API to facilitate seamless integration with external systems. This documentation outlines the API endpoints, their functionalities, request methods, and response structures for each specified model. Properly integrating with these endpoints will enable you to access and manipulate data within your system.

### Authentication

Before accessing the API, Clients should include an `Authorization` header with a valid token to authenticate their requests.

## Owner API

### Retrieve Owners

#### GET /api/owners/
- **Description**: Retrieve a list of all owners.
- **Response**:
  - `200 OK`: Returns a JSON array containing owner objects.
  - `404 Not Found`: Returned if no owners are found.

#### Retrieve Owner Details by ID

#### GET /api/owners/{id}/
- **Description**: Retrieve details of a specific owner by their unique ID.
- **Parameters**:
  - `id` (int): The unique identifier of the owner.
- **Response**:
  - `200 OK`: Returns a JSON object representing the owner.
  - `404 Not Found`: Returned if the owner with the specified ID is not found.

## Owner Detail Document API

### Retrieve Owner Detail Documents

#### GET /api/owner-detail-documents/
- **Description**: Retrieve a list of all owner detail documents.
- **Response**:
  - `200 OK`: Returns a JSON array containing owner detail document objects.
  - `404 Not Found`: Returned if no owner detail documents are found.

#### Retrieve Owner Detail Document by ID

#### GET /api/owner-detail-documents/{id}/
- **Description**: Retrieve details of a specific owner detail document by its unique ID.
- **Parameters**:
  - `id` (int): The unique identifier of the owner detail document.
- **Response**:
  - `200 OK`: Returns a JSON object representing the owner detail document.
  - `404 Not Found`: Returned if the owner detail document with the specified ID is not found.

## Agency API

### Retrieve Agencies

#### GET /api/agencies/
- **Description**: Retrieve a list of all agencies.
- **Response**:
  - `200 OK`: Returns a JSON array containing agency objects.
  - `404 Not Found`: Returned if no agencies are found.

#### Retrieve Agency Details by ID

#### GET /api/agencies/{id}/
- **Description**: Retrieve details of a specific agency by its unique ID.
- **Parameters**:
  - `id` (int): The unique identifier of the agency.
- **Response**:
  - `200 OK`: Returns a JSON object representing the agency.
  - `404 Not Found`: Returned if the agency with the specified ID is not found.

## Officer API

### Retrieve Officers

#### GET /api/officers/
- **Description**: Retrieve a list of all officers.
- **Response**:
  - `200 OK`: Returns a JSON array containing officer objects.
  - `404 Not Found`: Returned if no officers are found.

#### Retrieve Officer Details by ID

#### GET /api/officers/{id}/
- **Description**: Retrieve details of a specific officer by their unique ID.
- **Parameters**:
  - `id` (int): The unique identifier of the officer.
- **Response**:
  - `200 OK`: Returns a JSON object representing the officer.
  - `404 Not Found`: Returned if the officer with the specified ID is not found.

## Principal Officer Document API

### Retrieve Principal Officer Documents

#### GET /api/principal-officer-documents/
- **Description**: Retrieve a list of all principal officer documents.
- **Response**:
  - `200 OK`: Returns a JSON array containing principal officer document objects.
  - `404 Not Found`: Returned if no principal officer documents are found.

#### Retrieve Principal Officer Document by ID

#### GET /api/principal-officer-documents/{id}/
- **Description**: Retrieve details of a specific principal officer document by its unique ID.
- **Parameters**:
  - `id` (int): The unique identifier of the principal officer document.
- **Response**:
  - `200 OK`: Returns a JSON object representing the principal officer document.
  - `404 Not Found`: Returned if the principal officer document with the specified ID is not found.

## Owner Detail Certificate API

### Create Owner Detail Certificate

#### POST /api/owner-detail-certificates/
- **Description**: Create a new owner detail certificate.
- **Request Body**: JSON object containing the following fields:
  - `certificate_id` (string): The certificate ID.
  - `certificate` (file): The certificate file.
  - `comments` (string, optional): Comments about the certificate.
  - `owner` (int): The ID of the owner to associate with the certificate.
- **Response**:
  - `201 Created`: Returns a JSON object representing the created owner detail certificate.
  - `400 Bad Request`: Returned if the request data is invalid.
  - `404 Not Found`: Returned if the specified owner ID is not found.

This API integration documentation outlines the endpoints, their functionalities, and the expected request and response structures. Ensure that your integration conforms to these specifications to interact seamlessly with our Django-based system.
