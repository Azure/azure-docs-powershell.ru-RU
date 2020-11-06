---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: ed50d8e25dca0998e7e3e026783fe4ec78e6ce7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556568"
---
# <span data-ttu-id="f5e48-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="f5e48-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="f5e48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5e48-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e48-103">Добавляет конечные точки и метаданные для экземпляра диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e48-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5e48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5e48-104">SYNTAX</span></span>

### <span data-ttu-id="f5e48-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5e48-105">Name (Default)</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5e48-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5e48-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5e48-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5e48-107">DESCRIPTION</span></span>
<span data-ttu-id="f5e48-108">Командлет Add-AzureRmEnvironment добавляет конечные точки и метаданные, чтобы включить командлеты диспетчера ресурсов Azure для соединения с новым экземпляром диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e48-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="f5e48-109">Встроенные среды AzureCloud и AzureChinaCloud предназначены для существующих открытых экземпляров диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e48-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="f5e48-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5e48-110">EXAMPLES</span></span>

### <span data-ttu-id="f5e48-111">Пример 1: создание и изменение новой среды</span><span class="sxs-lookup"><span data-stu-id="f5e48-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment `
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

In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.
```

## <span data-ttu-id="f5e48-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5e48-112">PARAMETERS</span></span>

### <span data-ttu-id="f5e48-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5e48-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="f5e48-114">Указывает базовый центр проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f5e48-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="f5e48-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f5e48-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="f5e48-116">Указывает аудиторию для маркеров, которые проверяют запросы на конечные точки диспетчера ресурсов Azure или службы управления службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="f5e48-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="f5e48-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="f5e48-117">-AdTenant</span></span>
<span data-ttu-id="f5e48-118">Указывает клиента Active Directory, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f5e48-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="f5e48-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5e48-119">-ARMEndpoint</span></span>
<span data-ttu-id="f5e48-120">Конечная точка диспетчера ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="f5e48-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="f5e48-121">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f5e48-121">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="f5e48-122">DNS-суффикс конечных точек служб Analysis Services для Azure</span><span class="sxs-lookup"><span data-stu-id="f5e48-122">Dns Suffix of Azure Analysis Services service endpoints</span></span>

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


### <span data-ttu-id="f5e48-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f5e48-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="f5e48-124">DNS-суффикс для задания и службы каталогов Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f5e48-124">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="f5e48-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f5e48-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="f5e48-126">DNS-суффикс для файловой системы Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f5e48-126">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="f5e48-127">Пример: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="f5e48-127">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="f5e48-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f5e48-128">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="f5e48-129">Указывает суффикс доменного имени для служб хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f5e48-129">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="f5e48-130">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f5e48-130">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="f5e48-131">Указывает аудиторию для маркеров доступа, которые разрешают запросы служб хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f5e48-131">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="f5e48-132">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5e48-132">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="f5e48-133">Задает конечную точку для доступа к запросу оперативной аналитики.</span><span class="sxs-lookup"><span data-stu-id="f5e48-133">Specifies the endpoint for the Operational Insights query access.</span></span> 

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

### <span data-ttu-id="f5e48-134">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f5e48-134">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="f5e48-135">Указывает аудиторию для маркеров доступа, которые разрешают запросы для служб оперативной аналитики.</span><span class="sxs-lookup"><span data-stu-id="f5e48-135">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

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

### <span data-ttu-id="f5e48-136">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f5e48-136">-BatchEndpointResourceId</span></span>
<span data-ttu-id="f5e48-137">Идентификатор ресурса пакетной службы Azure, которая является получателем запрашиваемого маркера.</span><span class="sxs-lookup"><span data-stu-id="f5e48-137">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="f5e48-138">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="f5e48-138">-DataLakeAudience</span></span>
<span data-ttu-id="f5e48-139">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="f5e48-139">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="f5e48-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e48-140">-DefaultProfile</span></span>
<span data-ttu-id="f5e48-141">Credeetnails, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f5e48-141">The credeetnails, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e48-142">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="f5e48-142">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="f5e48-143">Указывает, что локальная проверка подлинности служб федерации Active Directory (ADFS) разрешена.</span><span class="sxs-lookup"><span data-stu-id="f5e48-143">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="f5e48-144">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5e48-144">-GalleryEndpoint</span></span>
<span data-ttu-id="f5e48-145">Задает конечную точку для коллекции шаблонов развертывания диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e48-145">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="f5e48-146">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="f5e48-146">-GraphAudience</span></span>
<span data-ttu-id="f5e48-147">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Graph.</span><span class="sxs-lookup"><span data-stu-id="f5e48-147">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="f5e48-148">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5e48-148">-GraphEndpoint</span></span>
<span data-ttu-id="f5e48-149">Указывает URL-адрес для запросов Graph (для метаданных Active Directory).</span><span class="sxs-lookup"><span data-stu-id="f5e48-149">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="f5e48-150">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="f5e48-150">-ManagementPortalUrl</span></span>
<span data-ttu-id="f5e48-151">Указывает URL-адрес портала управления.</span><span class="sxs-lookup"><span data-stu-id="f5e48-151">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="f5e48-152">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f5e48-152">-Name</span></span>
<span data-ttu-id="f5e48-153">Указывает имя среды, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="f5e48-153">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="f5e48-154">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="f5e48-154">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="f5e48-155">Указывает URL-адрес, с которого можно загрузить файлы publishsettings.</span><span class="sxs-lookup"><span data-stu-id="f5e48-155">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="f5e48-156">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5e48-156">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="f5e48-157">Указывает URL-адрес для запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e48-157">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="f5e48-158">-Scope</span><span class="sxs-lookup"><span data-stu-id="f5e48-158">-Scope</span></span>
<span data-ttu-id="f5e48-159">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="f5e48-159">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f5e48-160">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5e48-160">-ServiceEndpoint</span></span>
<span data-ttu-id="f5e48-161">Задает конечную точку для запросов на управление службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="f5e48-161">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="f5e48-162">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f5e48-162">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="f5e48-163">Указывает суффикс доменных имен для серверов баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f5e48-163">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="f5e48-164">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="f5e48-164">-StorageEndpoint</span></span>
<span data-ttu-id="f5e48-165">Задает конечную точку для хранилища (BLOB-объектов, таблицы, очереди и файла).</span><span class="sxs-lookup"><span data-stu-id="f5e48-165">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="f5e48-166">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f5e48-166">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="f5e48-167">Задает суффикс доменных имен для служб диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="f5e48-167">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="f5e48-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5e48-168">-Confirm</span></span>
<span data-ttu-id="f5e48-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f5e48-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5e48-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5e48-170">-WhatIf</span></span>
<span data-ttu-id="f5e48-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f5e48-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5e48-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f5e48-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5e48-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e48-173">CommonParameters</span></span>
<span data-ttu-id="f5e48-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5e48-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e48-175">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e48-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e48-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5e48-176">INPUTS</span></span>

### <span data-ttu-id="f5e48-177">System. String</span><span class="sxs-lookup"><span data-stu-id="f5e48-177">System.String</span></span>

### <span data-ttu-id="f5e48-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f5e48-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f5e48-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5e48-179">OUTPUTS</span></span>

### <span data-ttu-id="f5e48-180">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f5e48-180">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="f5e48-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5e48-181">NOTES</span></span>

## <span data-ttu-id="f5e48-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5e48-182">RELATED LINKS</span></span>

[<span data-ttu-id="f5e48-183">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f5e48-183">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="f5e48-184">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f5e48-184">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="f5e48-185">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f5e48-185">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

