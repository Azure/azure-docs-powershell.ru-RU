---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: 510e191f29936b04e1d3e49b71ca1a6dfa160d20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734538"
---
# <span data-ttu-id="f8ccf-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="f8ccf-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="f8ccf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ccf-103">Добавляет конечные точки и метаданные для экземпляра диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8ccf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8ccf-104">SYNTAX</span></span>

### <span data-ttu-id="f8ccf-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f8ccf-105">Name (Default)</span></span>
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
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8ccf-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8ccf-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-DataLakeAudience] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8ccf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8ccf-107">DESCRIPTION</span></span>
<span data-ttu-id="f8ccf-108">Командлет Add-AzureRmEnvironment добавляет конечные точки и метаданные, чтобы включить командлеты диспетчера ресурсов Azure для соединения с новым экземпляром диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="f8ccf-109">Встроенные среды AzureCloud и AzureChinaCloud предназначены для существующих открытых экземпляров диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="f8ccf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8ccf-110">EXAMPLES</span></span>

### <span data-ttu-id="f8ccf-111">Пример 1: создание и изменение новой среды</span><span class="sxs-lookup"><span data-stu-id="f8ccf-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
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
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
```

<span data-ttu-id="f8ccf-112">В этом примере мы создаем новую среду Azure с примерами конечных точек с помощью Add-AzureRmEnvironment, а затем изменили значения атрибутов ActiveDirectoryEndpoint и GraphEndpoint для созданной среды с помощью командлета Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-112">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="f8ccf-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8ccf-113">PARAMETERS</span></span>

### <span data-ttu-id="f8ccf-114">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8ccf-114">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="f8ccf-115">Указывает базовый центр проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-115">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="f8ccf-116">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f8ccf-116">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="f8ccf-117">Указывает аудиторию для маркеров, которые проверяют запросы на конечные точки диспетчера ресурсов Azure или службы управления службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="f8ccf-117">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="f8ccf-118">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="f8ccf-118">-AdTenant</span></span>
<span data-ttu-id="f8ccf-119">Указывает клиента Active Directory, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-119">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="f8ccf-120">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8ccf-120">-ARMEndpoint</span></span>
<span data-ttu-id="f8ccf-121">Конечная точка диспетчера ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="f8ccf-121">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="f8ccf-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f8ccf-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="f8ccf-123">DNS-суффикс для задания и службы каталогов Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="f8ccf-123">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="f8ccf-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f8ccf-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="f8ccf-125">DNS-суффикс для файловой системы Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-125">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="f8ccf-126">Пример: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="f8ccf-126">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="f8ccf-127">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f8ccf-127">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="f8ccf-128">Указывает суффикс доменного имени для служб хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-128">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="f8ccf-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="f8ccf-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="f8ccf-130">Указывает аудиторию для маркеров доступа, которые разрешают запросы служб хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-130">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ccf-131">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="f8ccf-131">-DataLakeAudience</span></span>
<span data-ttu-id="f8ccf-132">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-132">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="f8ccf-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ccf-133">-DefaultProfile</span></span>
<span data-ttu-id="f8ccf-134">Credeetnails, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f8ccf-134">The credeetnails, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8ccf-135">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="f8ccf-135">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="f8ccf-136">Указывает, что локальная проверка подлинности служб федерации Active Directory (ADFS) разрешена.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-136">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="f8ccf-137">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8ccf-137">-GalleryEndpoint</span></span>
<span data-ttu-id="f8ccf-138">Задает конечную точку для коллекции шаблонов развертывания диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-138">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="f8ccf-139">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="f8ccf-139">-GraphAudience</span></span>
<span data-ttu-id="f8ccf-140">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Graph.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-140">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="f8ccf-141">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8ccf-141">-GraphEndpoint</span></span>
<span data-ttu-id="f8ccf-142">Указывает URL-адрес для запросов Graph (для метаданных Active Directory).</span><span class="sxs-lookup"><span data-stu-id="f8ccf-142">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="f8ccf-143">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="f8ccf-143">-ManagementPortalUrl</span></span>
<span data-ttu-id="f8ccf-144">Указывает URL-адрес портала управления.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-144">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="f8ccf-145">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f8ccf-145">-Name</span></span>
<span data-ttu-id="f8ccf-146">Указывает имя среды, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-146">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="f8ccf-147">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="f8ccf-147">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="f8ccf-148">Указывает URL-адрес, с которого можно загрузить файлы publishsettings.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-148">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="f8ccf-149">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8ccf-149">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="f8ccf-150">Указывает URL-адрес для запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-150">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="f8ccf-151">-Scope</span><span class="sxs-lookup"><span data-stu-id="f8ccf-151">-Scope</span></span>
<span data-ttu-id="f8ccf-152">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-152">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f8ccf-153">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8ccf-153">-ServiceEndpoint</span></span>
<span data-ttu-id="f8ccf-154">Задает конечную точку для запросов на управление службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="f8ccf-154">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="f8ccf-155">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f8ccf-155">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="f8ccf-156">Указывает суффикс доменных имен для серверов баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-156">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="f8ccf-157">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8ccf-157">-StorageEndpoint</span></span>
<span data-ttu-id="f8ccf-158">Задает конечную точку для хранилища (BLOB-объектов, таблицы, очереди и файла).</span><span class="sxs-lookup"><span data-stu-id="f8ccf-158">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="f8ccf-159">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="f8ccf-159">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="f8ccf-160">Задает суффикс доменных имен для служб диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-160">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="f8ccf-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8ccf-161">-Confirm</span></span>
<span data-ttu-id="f8ccf-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8ccf-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8ccf-163">-WhatIf</span></span>
<span data-ttu-id="f8ccf-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8ccf-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8ccf-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ccf-166">CommonParameters</span></span>
<span data-ttu-id="f8ccf-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ccf-168">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ccf-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ccf-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8ccf-169">INPUTS</span></span>

## <span data-ttu-id="f8ccf-170">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8ccf-170">OUTPUTS</span></span>

### <span data-ttu-id="f8ccf-171">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f8ccf-171">PSAzureEnvironment</span></span>
<span data-ttu-id="f8ccf-172">Этот командлет возвращает набор конечных точек и метаданных, необходимых для связи с экземпляром Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ccf-172">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="f8ccf-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8ccf-173">NOTES</span></span>

## <span data-ttu-id="f8ccf-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8ccf-174">RELATED LINKS</span></span>

[<span data-ttu-id="f8ccf-175">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f8ccf-175">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="f8ccf-176">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f8ccf-176">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="f8ccf-177">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="f8ccf-177">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

