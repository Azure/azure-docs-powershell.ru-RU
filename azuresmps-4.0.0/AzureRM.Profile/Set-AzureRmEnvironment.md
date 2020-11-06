---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37e8952ab7337ae69e5c23ed4ab09e651acfac8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555403"
---
# <span data-ttu-id="158b6-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="158b6-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="158b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="158b6-102">SYNOPSIS</span></span>
<span data-ttu-id="158b6-103">Задает свойства среды Azure.</span><span class="sxs-lookup"><span data-stu-id="158b6-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="158b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="158b6-104">SYNTAX</span></span>

```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="158b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="158b6-105">DESCRIPTION</span></span>
<span data-ttu-id="158b6-106">Командлет Set-AzureRMEnvironment задает конечные точки и метаданные для подключения к экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="158b6-106">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="158b6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="158b6-107">EXAMPLES</span></span>

### <span data-ttu-id="158b6-108">Пример 1: создание и изменение новой среды</span><span class="sxs-lookup"><span data-stu-id="158b6-108">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="158b6-109">В этом примере мы создаем новую среду Azure с примерами конечных точек с помощью Add-AzureRmEnvironment, а затем изменили значения атрибутов ActiveDirectoryEndpoint и GraphEndpoint для созданной среды с помощью командлета Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="158b6-109">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="158b6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="158b6-110">PARAMETERS</span></span>

### <span data-ttu-id="158b6-111">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="158b6-111">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="158b6-112">Указывает базовый центр проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="158b6-112">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-113">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="158b6-113">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="158b6-114">Указывает аудиторию для маркеров, которые проверяют запросы на конечные точки диспетчера ресурсов Azure или службы управления службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="158b6-114">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-115">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="158b6-115">-AdTenant</span></span>
<span data-ttu-id="158b6-116">Указывает клиента Active Directory, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="158b6-116">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="158b6-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="158b6-118">DNS-суффикс для задания и службы каталогов Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="158b6-118">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="158b6-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="158b6-120">DNS-суффикс для файловой системы Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="158b6-120">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="158b6-121">Пример: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="158b6-121">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-122">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="158b6-122">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="158b6-123">Указывает суффикс доменного имени для служб хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="158b6-123">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-124">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="158b6-124">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="158b6-125">Указывает аудиторию для маркеров доступа, которые разрешают запросы служб хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="158b6-125">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="158b6-126">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="158b6-127">Указывает, что локальная проверка подлинности служб федерации Active Directory (ADFS) разрешена.</span><span class="sxs-lookup"><span data-stu-id="158b6-127">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-128">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="158b6-128">-GalleryEndpoint</span></span>
<span data-ttu-id="158b6-129">Задает конечную точку для коллекции шаблонов развертывания диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="158b6-129">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-130">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="158b6-130">-GraphAudience</span></span>
<span data-ttu-id="158b6-131">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Graph.</span><span class="sxs-lookup"><span data-stu-id="158b6-131">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-132">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="158b6-132">-GraphEndpoint</span></span>
<span data-ttu-id="158b6-133">Указывает URL-адрес для запросов Graph (для метаданных Active Directory).</span><span class="sxs-lookup"><span data-stu-id="158b6-133">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-134">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="158b6-134">-ManagementPortalUrl</span></span>
<span data-ttu-id="158b6-135">Указывает URL-адрес портала управления.</span><span class="sxs-lookup"><span data-stu-id="158b6-135">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="158b6-136">-Name</span></span>
<span data-ttu-id="158b6-137">Указывает имя среды, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="158b6-137">Specifies the name of the environment to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-138">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="158b6-138">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="158b6-139">Указывает URL-адрес, с которого можно загрузить файлы publishsettings.</span><span class="sxs-lookup"><span data-stu-id="158b6-139">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-140">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="158b6-140">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="158b6-141">Указывает URL-адрес для запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="158b6-141">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="158b6-142">-ServiceEndpoint</span></span>
<span data-ttu-id="158b6-143">Задает конечную точку для запросов на управление службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="158b6-143">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-144">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="158b6-144">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="158b6-145">Указывает суффикс доменных имен для серверов баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="158b6-145">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-146">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="158b6-146">-StorageEndpoint</span></span>
<span data-ttu-id="158b6-147">Задает конечную точку для хранилища (BLOB-объектов, таблицы, очереди и файла).</span><span class="sxs-lookup"><span data-stu-id="158b6-147">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-148">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="158b6-148">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="158b6-149">Задает суффикс доменных имен для служб диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="158b6-149">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="158b6-150">-Confirm</span></span>
<span data-ttu-id="158b6-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="158b6-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="158b6-152">-WhatIf</span></span>
<span data-ttu-id="158b6-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="158b6-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="158b6-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="158b6-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="158b6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158b6-155">CommonParameters</span></span>
<span data-ttu-id="158b6-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="158b6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158b6-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="158b6-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158b6-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="158b6-158">INPUTS</span></span>

## <span data-ttu-id="158b6-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="158b6-159">OUTPUTS</span></span>

### <span data-ttu-id="158b6-160">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="158b6-160">PSAzureEnvironment</span></span>

## <span data-ttu-id="158b6-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="158b6-161">NOTES</span></span>

## <span data-ttu-id="158b6-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="158b6-162">RELATED LINKS</span></span>

[<span data-ttu-id="158b6-163">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="158b6-163">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="158b6-164">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="158b6-164">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="158b6-165">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="158b6-165">Remove-AzureRMEnvironment</span></span>]()

