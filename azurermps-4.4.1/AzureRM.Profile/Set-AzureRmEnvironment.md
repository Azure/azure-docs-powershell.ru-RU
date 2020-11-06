---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
ms.openlocfilehash: c39b61ab51296231b0952d1f12bd18e6d3aa13d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569267"
---
# <span data-ttu-id="3dc93-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="3dc93-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="3dc93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3dc93-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc93-103">Задает свойства среды Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc93-103">Sets properties for an Azure environment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dc93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3dc93-104">SYNTAX</span></span>

### <span data-ttu-id="3dc93-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3dc93-105">Name (Default)</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
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

### <span data-ttu-id="3dc93-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc93-106">ARMEndpoint</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-DataLakeAudience] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dc93-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dc93-107">DESCRIPTION</span></span>
<span data-ttu-id="3dc93-108">Командлет Set-AzureRMEnvironment задает конечные точки и метаданные для подключения к экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc93-108">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="3dc93-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3dc93-109">EXAMPLES</span></span>

### <span data-ttu-id="3dc93-110">Пример 1: создание и изменение новой среды</span><span class="sxs-lookup"><span data-stu-id="3dc93-110">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="3dc93-111">В этом примере мы создаем новую среду Azure с примерами конечных точек с помощью Add-AzureRmEnvironment, а затем изменили значения атрибутов ActiveDirectoryEndpoint и GraphEndpoint для созданной среды с помощью командлета Set-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="3dc93-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="3dc93-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3dc93-112">PARAMETERS</span></span>

### <span data-ttu-id="3dc93-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc93-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="3dc93-114">Указывает базовый центр проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3dc93-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="3dc93-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3dc93-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="3dc93-116">Указывает аудиторию для маркеров, которые проверяют запросы на конечные точки диспетчера ресурсов Azure или службы управления службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="3dc93-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="3dc93-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="3dc93-117">-AdTenant</span></span>
<span data-ttu-id="3dc93-118">Указывает клиента Active Directory, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3dc93-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="3dc93-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc93-119">-ARMEndpoint</span></span>
<span data-ttu-id="3dc93-120">Конечная точка диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc93-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="3dc93-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3dc93-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="3dc93-122">DNS-суффикс для задания и службы каталогов Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="3dc93-122">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="3dc93-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3dc93-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="3dc93-124">DNS-суффикс для файловой системы Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3dc93-124">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="3dc93-125">Пример: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="3dc93-125">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="3dc93-126">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3dc93-126">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="3dc93-127">Указывает суффикс доменного имени для служб хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3dc93-127">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="3dc93-128">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3dc93-128">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="3dc93-129">Указывает аудиторию для маркеров доступа, которые разрешают запросы служб хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="3dc93-129">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="3dc93-130">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="3dc93-130">-DataLakeAudience</span></span>
<span data-ttu-id="3dc93-131">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="3dc93-131">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="3dc93-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc93-132">-DefaultProfile</span></span>
<span data-ttu-id="3dc93-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc93-133">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dc93-134">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="3dc93-134">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="3dc93-135">Указывает, что локальная проверка подлинности служб федерации Active Directory (ADFS) разрешена.</span><span class="sxs-lookup"><span data-stu-id="3dc93-135">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="3dc93-136">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc93-136">-GalleryEndpoint</span></span>
<span data-ttu-id="3dc93-137">Задает конечную точку для коллекции шаблонов развертывания диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc93-137">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="3dc93-138">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="3dc93-138">-GraphAudience</span></span>
<span data-ttu-id="3dc93-139">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Graph.</span><span class="sxs-lookup"><span data-stu-id="3dc93-139">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="3dc93-140">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc93-140">-GraphEndpoint</span></span>
<span data-ttu-id="3dc93-141">Указывает URL-адрес для запросов Graph (для метаданных Active Directory).</span><span class="sxs-lookup"><span data-stu-id="3dc93-141">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="3dc93-142">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="3dc93-142">-ManagementPortalUrl</span></span>
<span data-ttu-id="3dc93-143">Указывает URL-адрес портала управления.</span><span class="sxs-lookup"><span data-stu-id="3dc93-143">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="3dc93-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3dc93-144">-Name</span></span>
<span data-ttu-id="3dc93-145">Указывает имя среды, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="3dc93-145">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="3dc93-146">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="3dc93-146">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="3dc93-147">Указывает URL-адрес, с которого можно загрузить файлы publishsettings.</span><span class="sxs-lookup"><span data-stu-id="3dc93-147">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="3dc93-148">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc93-148">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="3dc93-149">Указывает URL-адрес для запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc93-149">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="3dc93-150">-Scope</span><span class="sxs-lookup"><span data-stu-id="3dc93-150">-Scope</span></span>
<span data-ttu-id="3dc93-151">Определяет область изменений контекста, например wheher изменения применяются только к процессу cusrrent или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="3dc93-151">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3dc93-152">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc93-152">-ServiceEndpoint</span></span>
<span data-ttu-id="3dc93-153">Задает конечную точку для запросов на управление службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="3dc93-153">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="3dc93-154">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3dc93-154">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="3dc93-155">Указывает суффикс доменных имен для серверов баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3dc93-155">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="3dc93-156">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="3dc93-156">-StorageEndpoint</span></span>
<span data-ttu-id="3dc93-157">Задает конечную точку для хранилища (BLOB-объектов, таблицы, очереди и файла).</span><span class="sxs-lookup"><span data-stu-id="3dc93-157">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="3dc93-158">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3dc93-158">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="3dc93-159">Задает суффикс доменных имен для служб диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc93-159">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="3dc93-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dc93-160">-Confirm</span></span>
<span data-ttu-id="3dc93-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3dc93-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dc93-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc93-162">-WhatIf</span></span>
<span data-ttu-id="3dc93-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3dc93-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dc93-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3dc93-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dc93-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc93-165">CommonParameters</span></span>
<span data-ttu-id="3dc93-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3dc93-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc93-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dc93-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc93-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3dc93-168">INPUTS</span></span>

## <span data-ttu-id="3dc93-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dc93-169">OUTPUTS</span></span>

### <span data-ttu-id="3dc93-170">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3dc93-170">PSAzureEnvironment</span></span>

## <span data-ttu-id="3dc93-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="3dc93-171">NOTES</span></span>

## <span data-ttu-id="3dc93-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3dc93-172">RELATED LINKS</span></span>

[<span data-ttu-id="3dc93-173">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3dc93-173">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="3dc93-174">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3dc93-174">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="3dc93-175">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="3dc93-175">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

