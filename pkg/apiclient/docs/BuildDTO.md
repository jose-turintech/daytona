# BuildDTO

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BuildConfig** | Pointer to [**BuildConfig**](BuildConfig.md) |  | [optional] 
**ContainerConfig** | [**ContainerConfig**](ContainerConfig.md) |  | 
**CreatedAt** | **string** |  | 
**EnvVars** | **map[string]string** |  | 
**Id** | **string** |  | 
**Image** | Pointer to **string** |  | [optional] 
**LastJob** | Pointer to [**Job**](Job.md) |  | [optional] 
**LastJobId** | Pointer to **string** |  | [optional] 
**PrebuildId** | Pointer to **string** |  | [optional] 
**Repository** | [**GitRepository**](GitRepository.md) |  | 
**State** | [**ResourceState**](ResourceState.md) |  | 
**UpdatedAt** | **string** |  | 
**User** | Pointer to **string** |  | [optional] 

## Methods

### NewBuildDTO

`func NewBuildDTO(containerConfig ContainerConfig, createdAt string, envVars map[string]string, id string, repository GitRepository, state ResourceState, updatedAt string, ) *BuildDTO`

NewBuildDTO instantiates a new BuildDTO object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBuildDTOWithDefaults

`func NewBuildDTOWithDefaults() *BuildDTO`

NewBuildDTOWithDefaults instantiates a new BuildDTO object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetBuildConfig

`func (o *BuildDTO) GetBuildConfig() BuildConfig`

GetBuildConfig returns the BuildConfig field if non-nil, zero value otherwise.

### GetBuildConfigOk

`func (o *BuildDTO) GetBuildConfigOk() (*BuildConfig, bool)`

GetBuildConfigOk returns a tuple with the BuildConfig field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBuildConfig

`func (o *BuildDTO) SetBuildConfig(v BuildConfig)`

SetBuildConfig sets BuildConfig field to given value.

### HasBuildConfig

`func (o *BuildDTO) HasBuildConfig() bool`

HasBuildConfig returns a boolean if a field has been set.

### GetContainerConfig

`func (o *BuildDTO) GetContainerConfig() ContainerConfig`

GetContainerConfig returns the ContainerConfig field if non-nil, zero value otherwise.

### GetContainerConfigOk

`func (o *BuildDTO) GetContainerConfigOk() (*ContainerConfig, bool)`

GetContainerConfigOk returns a tuple with the ContainerConfig field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetContainerConfig

`func (o *BuildDTO) SetContainerConfig(v ContainerConfig)`

SetContainerConfig sets ContainerConfig field to given value.


### GetCreatedAt

`func (o *BuildDTO) GetCreatedAt() string`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *BuildDTO) GetCreatedAtOk() (*string, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *BuildDTO) SetCreatedAt(v string)`

SetCreatedAt sets CreatedAt field to given value.


### GetEnvVars

`func (o *BuildDTO) GetEnvVars() map[string]string`

GetEnvVars returns the EnvVars field if non-nil, zero value otherwise.

### GetEnvVarsOk

`func (o *BuildDTO) GetEnvVarsOk() (*map[string]string, bool)`

GetEnvVarsOk returns a tuple with the EnvVars field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnvVars

`func (o *BuildDTO) SetEnvVars(v map[string]string)`

SetEnvVars sets EnvVars field to given value.


### GetId

`func (o *BuildDTO) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *BuildDTO) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *BuildDTO) SetId(v string)`

SetId sets Id field to given value.


### GetImage

`func (o *BuildDTO) GetImage() string`

GetImage returns the Image field if non-nil, zero value otherwise.

### GetImageOk

`func (o *BuildDTO) GetImageOk() (*string, bool)`

GetImageOk returns a tuple with the Image field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetImage

`func (o *BuildDTO) SetImage(v string)`

SetImage sets Image field to given value.

### HasImage

`func (o *BuildDTO) HasImage() bool`

HasImage returns a boolean if a field has been set.

### GetLastJob

`func (o *BuildDTO) GetLastJob() Job`

GetLastJob returns the LastJob field if non-nil, zero value otherwise.

### GetLastJobOk

`func (o *BuildDTO) GetLastJobOk() (*Job, bool)`

GetLastJobOk returns a tuple with the LastJob field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLastJob

`func (o *BuildDTO) SetLastJob(v Job)`

SetLastJob sets LastJob field to given value.

### HasLastJob

`func (o *BuildDTO) HasLastJob() bool`

HasLastJob returns a boolean if a field has been set.

### GetLastJobId

`func (o *BuildDTO) GetLastJobId() string`

GetLastJobId returns the LastJobId field if non-nil, zero value otherwise.

### GetLastJobIdOk

`func (o *BuildDTO) GetLastJobIdOk() (*string, bool)`

GetLastJobIdOk returns a tuple with the LastJobId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLastJobId

`func (o *BuildDTO) SetLastJobId(v string)`

SetLastJobId sets LastJobId field to given value.

### HasLastJobId

`func (o *BuildDTO) HasLastJobId() bool`

HasLastJobId returns a boolean if a field has been set.

### GetPrebuildId

`func (o *BuildDTO) GetPrebuildId() string`

GetPrebuildId returns the PrebuildId field if non-nil, zero value otherwise.

### GetPrebuildIdOk

`func (o *BuildDTO) GetPrebuildIdOk() (*string, bool)`

GetPrebuildIdOk returns a tuple with the PrebuildId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrebuildId

`func (o *BuildDTO) SetPrebuildId(v string)`

SetPrebuildId sets PrebuildId field to given value.

### HasPrebuildId

`func (o *BuildDTO) HasPrebuildId() bool`

HasPrebuildId returns a boolean if a field has been set.

### GetRepository

`func (o *BuildDTO) GetRepository() GitRepository`

GetRepository returns the Repository field if non-nil, zero value otherwise.

### GetRepositoryOk

`func (o *BuildDTO) GetRepositoryOk() (*GitRepository, bool)`

GetRepositoryOk returns a tuple with the Repository field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRepository

`func (o *BuildDTO) SetRepository(v GitRepository)`

SetRepository sets Repository field to given value.


### GetState

`func (o *BuildDTO) GetState() ResourceState`

GetState returns the State field if non-nil, zero value otherwise.

### GetStateOk

`func (o *BuildDTO) GetStateOk() (*ResourceState, bool)`

GetStateOk returns a tuple with the State field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetState

`func (o *BuildDTO) SetState(v ResourceState)`

SetState sets State field to given value.


### GetUpdatedAt

`func (o *BuildDTO) GetUpdatedAt() string`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *BuildDTO) GetUpdatedAtOk() (*string, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *BuildDTO) SetUpdatedAt(v string)`

SetUpdatedAt sets UpdatedAt field to given value.


### GetUser

`func (o *BuildDTO) GetUser() string`

GetUser returns the User field if non-nil, zero value otherwise.

### GetUserOk

`func (o *BuildDTO) GetUserOk() (*string, bool)`

GetUserOk returns a tuple with the User field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUser

`func (o *BuildDTO) SetUser(v string)`

SetUser sets User field to given value.

### HasUser

`func (o *BuildDTO) HasUser() bool`

HasUser returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


