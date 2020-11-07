---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 47f57068af722bd9f34826176d2a31cdfd9843a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720293"
---
# <span data-ttu-id="f99f2-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f99f2-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="f99f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f99f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f99f2-103">Добавляет конечные точки и метаданные для экземпляра диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f99f2-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="f99f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f99f2-104">SYNTAX</span></span>

### <span data-ttu-id="f99f2-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f99f2-105">Name (Default)</span></span>
```
Add-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>]
 [-AzureAnalysisServicesEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f99f2-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f99f2-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f99f2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f99f2-107">DESCRIPTION</span></span>
<span data-ttu-id="f99f2-108">Командлет Add-AzEnvironment добавляет конечные точки и метаданные, чтобы включить командлеты диспетчера ресурсов Azure для соединения с новым экземпляром диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f99f2-108">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="f99f2-109">Встроенные среды AzureCloud и AzureChinaCloud предназначены для существующих открытых экземпляров диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f99f2-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="f99f2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f99f2-110">EXAMPLES</span></span>

### <span data-ttu-id="f99f2-111">Пример 1: создание и изменение новой среды</span><span class="sxs-lookup"><span data-stu-id="f99f2-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint NewTestADEndpoint `
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
OnPremise                                         : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              :
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : NewTestADEndpoint
GraphUrl                                          : NewTestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
DataLakeEndpointResourceId                        :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
AzureOperationalInsightsEndpointResourceId        :
AzureOperationalInsightsEndpoint                  :
AzureAnalysisServicesEndpointSuffix               :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.
```

## <span data-ttu-id="f99f2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f99f2-112">PARAMETERS</span></span>

### <span data-ttu-id="f99f2-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f99f2-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="f99f2-114">Указывает базовый центр проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f99f2-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f99f2-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="f99f2-116">Указывает аудиторию для маркеров, которые проверяют запросы на конечные точки диспетчера ресурсов Azure или службы управления службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="f99f2-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="f99f2-117">-AdTenant</span></span>
<span data-ttu-id="f99f2-118">Указывает клиента Active Directory, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f99f2-118">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f99f2-119">-ARMEndpoint</span></span>
<span data-ttu-id="f99f2-120">Конечная точка диспетчера ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="f99f2-120">The Azure Resource Manager endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f99f2-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="f99f2-122">Идентификатор ресурса для ресурса служб аналитики Azure.</span><span class="sxs-lookup"><span data-stu-id="f99f2-122">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f99f2-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="f99f2-124">Конечная точка, используемая при взаимодействии с API аналитических журналов Azure.</span><span class="sxs-lookup"><span data-stu-id="f99f2-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f99f2-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="f99f2-126">DNS-суффикс для задания и службы каталогов Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f99f2-126">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f99f2-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="f99f2-128">DNS-суффикс для файловой системы Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f99f2-128">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="f99f2-129">Пример: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="f99f2-129">Example: azuredatalake.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-130">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f99f2-130">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="f99f2-131">DNS-суффикс службы хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="f99f2-131">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="f99f2-132">Пример vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="f99f2-132">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-133">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f99f2-133">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="f99f2-134">Идентификатор ресурса службы данных Azure Key Vault, которая является получателем запрошенного маркера.</span><span class="sxs-lookup"><span data-stu-id="f99f2-134">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-135">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="f99f2-135">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="f99f2-136">Конечная точка, используемая при взаимодействии с API аналитических журналов Azure.</span><span class="sxs-lookup"><span data-stu-id="f99f2-136">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-137">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f99f2-137">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="f99f2-138">Аудитория для маркеров, проверяющих подлинность с помощью API аналитических журналов Azure.</span><span class="sxs-lookup"><span data-stu-id="f99f2-138">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-139">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f99f2-139">-BatchEndpointResourceId</span></span>
<span data-ttu-id="f99f2-140">Идентификатор ресурса пакетной службы Azure, которая является получателем запрашиваемого маркера.</span><span class="sxs-lookup"><span data-stu-id="f99f2-140">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-141">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="f99f2-141">-DataLakeAudience</span></span>
<span data-ttu-id="f99f2-142">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="f99f2-142">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f99f2-143">-DefaultProfile</span></span>
<span data-ttu-id="f99f2-144">Credeetnails, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f99f2-144">The credeetnails, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-145">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="f99f2-145">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="f99f2-146">Указывает, что локальная проверка подлинности служб федерации Active Directory (ADFS) разрешена.</span><span class="sxs-lookup"><span data-stu-id="f99f2-146">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-147">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f99f2-147">-GalleryEndpoint</span></span>
<span data-ttu-id="f99f2-148">Задает конечную точку для коллекции шаблонов развертывания диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f99f2-148">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-149">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="f99f2-149">-GraphAudience</span></span>
<span data-ttu-id="f99f2-150">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Graph.</span><span class="sxs-lookup"><span data-stu-id="f99f2-150">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-151">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="f99f2-151">-GraphEndpoint</span></span>
<span data-ttu-id="f99f2-152">Указывает URL-адрес для запросов Graph (для метаданных Active Directory).</span><span class="sxs-lookup"><span data-stu-id="f99f2-152">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-153">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="f99f2-153">-ManagementPortalUrl</span></span>
<span data-ttu-id="f99f2-154">Указывает URL-адрес портала управления.</span><span class="sxs-lookup"><span data-stu-id="f99f2-154">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-155">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f99f2-155">-Name</span></span>
<span data-ttu-id="f99f2-156">Указывает имя среды, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="f99f2-156">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-157">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="f99f2-157">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="f99f2-158">Указывает URL-адрес, с которого можно загрузить файлы publishsettings.</span><span class="sxs-lookup"><span data-stu-id="f99f2-158">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-159">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f99f2-159">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="f99f2-160">Указывает URL-адрес для запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f99f2-160">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-161">-Scope</span><span class="sxs-lookup"><span data-stu-id="f99f2-161">-Scope</span></span>
<span data-ttu-id="f99f2-162">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="f99f2-162">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-163">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f99f2-163">-ServiceEndpoint</span></span>
<span data-ttu-id="f99f2-164">Задает конечную точку для запросов на управление службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="f99f2-164">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-165">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f99f2-165">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="f99f2-166">Указывает суффикс доменных имен для серверов баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f99f2-166">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-167">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="f99f2-167">-StorageEndpoint</span></span>
<span data-ttu-id="f99f2-168">Задает конечную точку для хранилища (BLOB-объектов, таблицы, очереди и файла).</span><span class="sxs-lookup"><span data-stu-id="f99f2-168">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-169">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f99f2-169">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="f99f2-170">Задает суффикс доменных имен для служб диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="f99f2-170">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f99f2-171">-Confirm</span></span>
<span data-ttu-id="f99f2-172">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f99f2-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f99f2-173">-WhatIf</span></span>
<span data-ttu-id="f99f2-174">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f99f2-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f99f2-175">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f99f2-175">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99f2-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f99f2-176">CommonParameters</span></span>
<span data-ttu-id="f99f2-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f99f2-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f99f2-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f99f2-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f99f2-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f99f2-179">INPUTS</span></span>

### <span data-ttu-id="f99f2-180">System. String</span><span class="sxs-lookup"><span data-stu-id="f99f2-180">System.String</span></span>

### <span data-ttu-id="f99f2-181">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f99f2-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f99f2-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f99f2-182">OUTPUTS</span></span>

### <span data-ttu-id="f99f2-183">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f99f2-183">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="f99f2-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="f99f2-184">NOTES</span></span>

## <span data-ttu-id="f99f2-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f99f2-185">RELATED LINKS</span></span>

[<span data-ttu-id="f99f2-186">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f99f2-186">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="f99f2-187">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f99f2-187">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="f99f2-188">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="f99f2-188">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

