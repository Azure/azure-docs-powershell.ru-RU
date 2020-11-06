---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 650b5e2c930577101337c4fe0f33db9c32160e1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555295"
---
# <span data-ttu-id="abe51-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="abe51-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="abe51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="abe51-102">SYNOPSIS</span></span>
<span data-ttu-id="abe51-103">Добавляет конечные точки и метаданные для экземпляра диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="abe51-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="abe51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="abe51-104">SYNTAX</span></span>

```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abe51-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="abe51-105">DESCRIPTION</span></span>
<span data-ttu-id="abe51-106">Командлет Add-AzureRmEnvironment добавляет конечные точки и метаданные, чтобы включить командлеты диспетчера ресурсов Azure для соединения с новым экземпляром диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="abe51-106">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="abe51-107">Встроенные среды AzureCloud и AzureChinaCloud предназначены для существующих открытых экземпляров диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="abe51-107">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="abe51-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="abe51-108">EXAMPLES</span></span>

### <span data-ttu-id="abe51-109">Пример 1: создание и изменение новой среды</span><span class="sxs-lookup"><span data-stu-id="abe51-109">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="abe51-110">В этом примере мы создаем новую среду Azure с примерами конечных точек с помощью Add-AzureRmEnvironment, а затем изменили значения атрибутов ActiveDirectoryEndpoint и GraphEndpoint для созданной среды с помощью командлета Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="abe51-110">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="abe51-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="abe51-111">PARAMETERS</span></span>

### <span data-ttu-id="abe51-112">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="abe51-112">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="abe51-113">Указывает базовый центр проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="abe51-113">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="abe51-114">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="abe51-114">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="abe51-115">Указывает аудиторию для маркеров, которые проверяют запросы на конечные точки диспетчера ресурсов Azure или службы управления службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="abe51-115">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="abe51-116">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="abe51-116">-AdTenant</span></span>
<span data-ttu-id="abe51-117">Указывает клиента Active Directory, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="abe51-117">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="abe51-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="abe51-118">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="abe51-119">DNS-суффикс для задания и службы каталогов Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="abe51-119">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="abe51-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="abe51-120">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="abe51-121">DNS-суффикс для файловой системы Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="abe51-121">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="abe51-122">Пример: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="abe51-122">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="abe51-123">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="abe51-123">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="abe51-124">Указывает суффикс доменного имени для служб хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="abe51-124">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="abe51-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="abe51-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="abe51-126">Указывает аудиторию для маркеров доступа, которые разрешают запросы служб хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="abe51-126">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="abe51-127">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="abe51-127">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="abe51-128">Указывает, что локальная проверка подлинности служб федерации Active Directory (ADFS) разрешена.</span><span class="sxs-lookup"><span data-stu-id="abe51-128">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="abe51-129">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="abe51-129">-GalleryEndpoint</span></span>
<span data-ttu-id="abe51-130">Задает конечную точку для коллекции шаблонов развертывания диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="abe51-130">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="abe51-131">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="abe51-131">-GraphAudience</span></span>
<span data-ttu-id="abe51-132">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Graph.</span><span class="sxs-lookup"><span data-stu-id="abe51-132">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="abe51-133">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="abe51-133">-GraphEndpoint</span></span>
<span data-ttu-id="abe51-134">Указывает URL-адрес для запросов Graph (для метаданных Active Directory).</span><span class="sxs-lookup"><span data-stu-id="abe51-134">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="abe51-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="abe51-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="abe51-136">Указывает URL-адрес портала управления.</span><span class="sxs-lookup"><span data-stu-id="abe51-136">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="abe51-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="abe51-137">-Name</span></span>
<span data-ttu-id="abe51-138">Указывает имя среды, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="abe51-138">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="abe51-139">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="abe51-139">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="abe51-140">Указывает URL-адрес, с которого можно загрузить файлы publishsettings.</span><span class="sxs-lookup"><span data-stu-id="abe51-140">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="abe51-141">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="abe51-141">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="abe51-142">Указывает URL-адрес для запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="abe51-142">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="abe51-143">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="abe51-143">-ServiceEndpoint</span></span>
<span data-ttu-id="abe51-144">Задает конечную точку для запросов на управление службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="abe51-144">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="abe51-145">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="abe51-145">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="abe51-146">Указывает суффикс доменных имен для серверов баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="abe51-146">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="abe51-147">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="abe51-147">-StorageEndpoint</span></span>
<span data-ttu-id="abe51-148">Задает конечную точку для хранилища (BLOB-объектов, таблицы, очереди и файла).</span><span class="sxs-lookup"><span data-stu-id="abe51-148">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="abe51-149">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="abe51-149">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="abe51-150">Задает суффикс доменных имен для служб диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="abe51-150">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="abe51-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abe51-151">-Confirm</span></span>
<span data-ttu-id="abe51-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="abe51-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abe51-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abe51-153">-WhatIf</span></span>
<span data-ttu-id="abe51-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="abe51-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abe51-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="abe51-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abe51-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe51-156">CommonParameters</span></span>
<span data-ttu-id="abe51-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="abe51-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe51-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abe51-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe51-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="abe51-159">INPUTS</span></span>

## <span data-ttu-id="abe51-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="abe51-160">OUTPUTS</span></span>

### <span data-ttu-id="abe51-161">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="abe51-161">PSAzureEnvironment</span></span>
<span data-ttu-id="abe51-162">Этот командлет возвращает набор конечных точек и метаданных, необходимых для связи с экземпляром Azure.</span><span class="sxs-lookup"><span data-stu-id="abe51-162">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="abe51-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="abe51-163">NOTES</span></span>

## <span data-ttu-id="abe51-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="abe51-164">RELATED LINKS</span></span>

[<span data-ttu-id="abe51-165">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="abe51-165">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="abe51-166">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="abe51-166">Remove-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="abe51-167">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="abe51-167">Set-AzureRMEnvironment</span></span>]()

