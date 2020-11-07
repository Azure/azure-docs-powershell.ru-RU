---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 69f8c633cc87cac5ff2c0dc3226a09bd24e2e94c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909285"
---
# <span data-ttu-id="095b3-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="095b3-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="095b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="095b3-102">SYNOPSIS</span></span>
<span data-ttu-id="095b3-103">Добавляет конечные точки и метаданные для экземпляра диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="095b3-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="095b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="095b3-104">SYNTAX</span></span>

### <span data-ttu-id="095b3-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="095b3-105">Name (Default)</span></span>
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="095b3-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="095b3-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="095b3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="095b3-107">DESCRIPTION</span></span>
<span data-ttu-id="095b3-108">Командлет Add-AzEnvironment добавляет конечные точки и метаданные, чтобы включить командлеты диспетчера ресурсов Azure для соединения с новым экземпляром диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="095b3-108">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="095b3-109">Встроенные среды AzureCloud и AzureChinaCloud предназначены для существующих открытых экземпляров диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="095b3-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="095b3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="095b3-110">EXAMPLES</span></span>

### <span data-ttu-id="095b3-111">Пример 1: создание и изменение новой среды</span><span class="sxs-lookup"><span data-stu-id="095b3-111">Example 1: Creating and modifying a new environment</span></span>
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
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.
```

## <span data-ttu-id="095b3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="095b3-112">PARAMETERS</span></span>

### <span data-ttu-id="095b3-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="095b3-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="095b3-114">Указывает базовый центр проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="095b3-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="095b3-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="095b3-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="095b3-116">Указывает аудиторию для маркеров, которые проверяют запросы на конечные точки диспетчера ресурсов Azure или службы управления службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="095b3-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="095b3-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="095b3-117">-AdTenant</span></span>
<span data-ttu-id="095b3-118">Указывает клиента Active Directory, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="095b3-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="095b3-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="095b3-119">-ARMEndpoint</span></span>
<span data-ttu-id="095b3-120">Конечная точка диспетчера ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="095b3-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="095b3-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="095b3-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="095b3-122">Идентификатор ресурса для ресурса служб аналитики Azure.</span><span class="sxs-lookup"><span data-stu-id="095b3-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="095b3-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="095b3-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="095b3-124">Конечная точка, используемая при взаимодействии с API аналитических журналов Azure.</span><span class="sxs-lookup"><span data-stu-id="095b3-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="095b3-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="095b3-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="095b3-126">Идентификатор ресурса службы аттестации Azure, который является получателем запрошенного маркера.</span><span class="sxs-lookup"><span data-stu-id="095b3-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095b3-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="095b3-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="095b3-128">DNS-суффикс службы аттестации Azure.</span><span class="sxs-lookup"><span data-stu-id="095b3-128">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="095b3-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="095b3-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="095b3-130">DNS-суффикс для задания и службы каталогов Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="095b3-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="095b3-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="095b3-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="095b3-132">DNS-суффикс для файловой системы Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="095b3-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="095b3-133">Пример: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="095b3-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="095b3-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="095b3-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="095b3-135">DNS-суффикс службы хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="095b3-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="095b3-136">Пример vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="095b3-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="095b3-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="095b3-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="095b3-138">Идентификатор ресурса службы данных Azure Key Vault, которая является получателем запрошенного маркера.</span><span class="sxs-lookup"><span data-stu-id="095b3-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="095b3-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="095b3-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="095b3-140">Конечная точка, используемая при взаимодействии с API аналитических журналов Azure.</span><span class="sxs-lookup"><span data-stu-id="095b3-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="095b3-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="095b3-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="095b3-142">Аудитория для маркеров, проверяющих подлинность с помощью API аналитических журналов Azure.</span><span class="sxs-lookup"><span data-stu-id="095b3-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="095b3-143">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="095b3-143">-BatchEndpointResourceId</span></span>
<span data-ttu-id="095b3-144">Идентификатор ресурса пакетной службы Azure, которая является получателем запрашиваемого маркера.</span><span class="sxs-lookup"><span data-stu-id="095b3-144">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="095b3-145">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="095b3-145">-DataLakeAudience</span></span>
<span data-ttu-id="095b3-146">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="095b3-146">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="095b3-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095b3-147">-DefaultProfile</span></span>
<span data-ttu-id="095b3-148">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="095b3-148">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="095b3-149">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="095b3-149">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="095b3-150">Указывает, что локальная проверка подлинности служб федерации Active Directory (ADFS) разрешена.</span><span class="sxs-lookup"><span data-stu-id="095b3-150">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="095b3-151">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="095b3-151">-GalleryEndpoint</span></span>
<span data-ttu-id="095b3-152">Задает конечную точку для коллекции шаблонов развертывания диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="095b3-152">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="095b3-153">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="095b3-153">-GraphAudience</span></span>
<span data-ttu-id="095b3-154">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Graph.</span><span class="sxs-lookup"><span data-stu-id="095b3-154">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="095b3-155">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="095b3-155">-GraphEndpoint</span></span>
<span data-ttu-id="095b3-156">Указывает URL-адрес для запросов Graph (для метаданных Active Directory).</span><span class="sxs-lookup"><span data-stu-id="095b3-156">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="095b3-157">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="095b3-157">-ManagementPortalUrl</span></span>
<span data-ttu-id="095b3-158">Указывает URL-адрес портала управления.</span><span class="sxs-lookup"><span data-stu-id="095b3-158">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="095b3-159">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="095b3-159">-Name</span></span>
<span data-ttu-id="095b3-160">Указывает имя среды, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="095b3-160">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="095b3-161">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="095b3-161">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="095b3-162">Указывает URL-адрес, с которого можно загрузить файлы publishsettings.</span><span class="sxs-lookup"><span data-stu-id="095b3-162">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="095b3-163">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="095b3-163">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="095b3-164">Указывает URL-адрес для запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="095b3-164">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="095b3-165">-Scope</span><span class="sxs-lookup"><span data-stu-id="095b3-165">-Scope</span></span>
<span data-ttu-id="095b3-166">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="095b3-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="095b3-167">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="095b3-167">-ServiceEndpoint</span></span>
<span data-ttu-id="095b3-168">Задает конечную точку для запросов на управление службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="095b3-168">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="095b3-169">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="095b3-169">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="095b3-170">Указывает суффикс доменных имен для серверов баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="095b3-170">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="095b3-171">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="095b3-171">-StorageEndpoint</span></span>
<span data-ttu-id="095b3-172">Задает конечную точку для хранилища (BLOB-объектов, таблицы, очереди и файла).</span><span class="sxs-lookup"><span data-stu-id="095b3-172">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="095b3-173">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="095b3-173">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="095b3-174">Задает суффикс доменных имен для служб диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="095b3-174">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="095b3-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="095b3-175">-Confirm</span></span>
<span data-ttu-id="095b3-176">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="095b3-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="095b3-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="095b3-177">-WhatIf</span></span>
<span data-ttu-id="095b3-178">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="095b3-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="095b3-179">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="095b3-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="095b3-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095b3-180">CommonParameters</span></span>
<span data-ttu-id="095b3-181">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="095b3-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095b3-182">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="095b3-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095b3-183">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="095b3-183">INPUTS</span></span>

### <span data-ttu-id="095b3-184">System. String</span><span class="sxs-lookup"><span data-stu-id="095b3-184">System.String</span></span>

### <span data-ttu-id="095b3-185">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="095b3-185">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="095b3-186">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="095b3-186">OUTPUTS</span></span>

### <span data-ttu-id="095b3-187">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="095b3-187">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="095b3-188">Пуск</span><span class="sxs-lookup"><span data-stu-id="095b3-188">NOTES</span></span>

## <span data-ttu-id="095b3-189">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="095b3-189">RELATED LINKS</span></span>

[<span data-ttu-id="095b3-190">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="095b3-190">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="095b3-191">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="095b3-191">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="095b3-192">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="095b3-192">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

