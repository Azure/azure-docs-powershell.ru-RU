---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: ba5a398e21543bc4b19c09309884ceb11fed3197
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243769"
---
# <span data-ttu-id="b6c9d-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6c9d-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="b6c9d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c9d-103">Добавляет конечные точки и метаданные для экземпляра диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="b6c9d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6c9d-104">SYNTAX</span></span>

### <span data-ttu-id="b6c9d-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6c9d-105">Name (Default)</span></span>
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
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6c9d-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6c9d-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6c9d-107">Поиска</span><span class="sxs-lookup"><span data-stu-id="b6c9d-107">Discovery</span></span>
```
Add-AzEnvironment -AutoDiscover [-Uri <Uri>] [-Scope {Process | CurrentUser}]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6c9d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6c9d-108">DESCRIPTION</span></span>
<span data-ttu-id="b6c9d-109">Командлет Add-AzEnvironment добавляет конечные точки и метаданные, чтобы включить командлеты диспетчера ресурсов Azure для соединения с новым экземпляром диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="b6c9d-110">Встроенные среды AzureCloud и AzureChinaCloud предназначены для существующих открытых экземпляров диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="b6c9d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6c9d-111">EXAMPLES</span></span>

### <span data-ttu-id="b6c9d-112">Пример 1: создание и изменение новой среды</span><span class="sxs-lookup"><span data-stu-id="b6c9d-112">Example 1: Creating and modifying a new environment</span></span>
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
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :
```

<span data-ttu-id="b6c9d-113">В этом примере мы создаем новую среду Azure с примерами конечных точек с помощью Add-AzEnvironment, а затем изменили значения атрибутов ActiveDirectoryEndpoint и GraphEndpoint для созданной среды с помощью командлета Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="b6c9d-114">Пример 2: обнаружение новой среды с помощью URI</span><span class="sxs-lookup"><span data-stu-id="b6c9d-114">Example 2: Discovering a new environment via Uri</span></span>
```
<#
Uri https://configuredmetadata.net returns an array of environment metadata. The following example contains a payload for the AzureCloud default environment.

[
  {
    "portal": "https://portal.azure.com",
    "authentication": {
      "loginEndpoint": "https://login.microsoftonline.com/",
      "audiences": [
        "https://management.core.windows.net/"
      ],
      "tenant": "common",
      "identityProvider": "AAD"
    },
    "media": "https://rest.media.azure.net",
    "graphAudience": "https://graph.windows.net/",
    "graph": "https://graph.windows.net/",
    "name": "AzureCloud",
    "suffixes": {
      "azureDataLakeStoreFileSystem": "azuredatalakestore.net",
      "acrLoginServer": "azurecr.io",
      "sqlServerHostname": ".database.windows.net",
      "azureDataLakeAnalyticsCatalogAndJob": "azuredatalakeanalytics.net",
      "keyVaultDns": "vault.azure.net",
      "storage": "core.windows.net",
      "azureFrontDoorEndpointSuffix": "azurefd.net"
    },
    "batch": "https://batch.core.windows.net/",
    "resourceManager": "https://management.azure.com/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json",
    "activeDirectoryDataLake": "https://datalake.azure.net/",
    "sqlManagement": "https://management.core.windows.net:8443/",
    "gallery": "https://gallery.azure.com/"
  },
……
]
#>

PS C:\> Add-AzEnvironment -AutoDiscover -Uri https://configuredmetadata.net

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="b6c9d-115">В этом примере мы обнаруживаем новую среду Azure из https://configuredmetadata.net универсального кода ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="b6c9d-115">In this example, we are discovering a new Azure environment from the https://configuredmetadata.net Uri.</span></span>

## <span data-ttu-id="b6c9d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6c9d-116">PARAMETERS</span></span>

### <span data-ttu-id="b6c9d-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6c9d-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="b6c9d-118">Указывает базовый центр проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="b6c9d-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c9d-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="b6c9d-120">Указывает аудиторию для маркеров, которые проверяют запросы на конечные точки диспетчера ресурсов Azure или службы управления службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="b6c9d-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="b6c9d-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="b6c9d-121">-AdTenant</span></span>
<span data-ttu-id="b6c9d-122">Указывает клиента Active Directory, используемого по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-122">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="b6c9d-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6c9d-123">-ARMEndpoint</span></span>
<span data-ttu-id="b6c9d-124">Конечная точка диспетчера ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="b6c9d-124">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="b6c9d-125">-Автообнаружения</span><span class="sxs-lookup"><span data-stu-id="b6c9d-125">-AutoDiscover</span></span>
<span data-ttu-id="b6c9d-126">Среды рассматриваются по умолчанию или настроенной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-126">Discovers environments via default or configured endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Discovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c9d-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="b6c9d-128">Идентификатор ресурса для ресурса служб аналитики Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-128">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b6c9d-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="b6c9d-130">Конечная точка, используемая при взаимодействии с API аналитических журналов Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c9d-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="b6c9d-132">Идентификатор ресурса службы аттестации Azure, который является получателем запрошенного маркера.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b6c9d-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="b6c9d-134">DNS-суффикс службы аттестации Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-134">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b6c9d-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="b6c9d-136">DNS-суффикс для задания и службы каталогов Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="b6c9d-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="b6c9d-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b6c9d-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="b6c9d-138">DNS-суффикс для файловой системы Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="b6c9d-139">Пример: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="b6c9d-139">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="b6c9d-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b6c9d-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="b6c9d-141">DNS-суффикс службы хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="b6c9d-142">Пример vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="b6c9d-142">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c9d-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="b6c9d-144">Идентификатор ресурса службы данных Azure Key Vault, которая является получателем запрошенного маркера.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6c9d-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="b6c9d-146">Конечная точка, используемая при взаимодействии с API аналитических журналов Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c9d-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="b6c9d-148">Аудитория для маркеров, проверяющих подлинность с помощью API аналитических журналов Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c9d-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="b6c9d-150">Идентификатор ресурса аналитики Azure Synapse Analytics, которая является получателем запрошенного маркера.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="b6c9d-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="b6c9d-152">DNS-суффикс Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-152">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c9d-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="b6c9d-154">Идентификатор ресурса пакетной службы Azure, которая является получателем запрашиваемого маркера.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-155">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="b6c9d-155">-DataLakeAudience</span></span>
<span data-ttu-id="b6c9d-156">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Data Lake Services.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-156">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c9d-157">-DefaultProfile</span></span>
<span data-ttu-id="b6c9d-158">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b6c9d-158">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6c9d-159">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="b6c9d-159">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="b6c9d-160">Указывает, что локальная проверка подлинности служб федерации Active Directory (ADFS) разрешена.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-160">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="b6c9d-161">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6c9d-161">-GalleryEndpoint</span></span>
<span data-ttu-id="b6c9d-162">Задает конечную точку для коллекции шаблонов развертывания диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-162">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="b6c9d-163">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="b6c9d-163">-GraphAudience</span></span>
<span data-ttu-id="b6c9d-164">Аудитория для маркеров, прошедших проверку подлинности с помощью конечной точки AD Graph.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-164">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="b6c9d-165">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6c9d-165">-GraphEndpoint</span></span>
<span data-ttu-id="b6c9d-166">Указывает URL-адрес для запросов Graph (для метаданных Active Directory).</span><span class="sxs-lookup"><span data-stu-id="b6c9d-166">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="b6c9d-167">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="b6c9d-167">-ManagementPortalUrl</span></span>
<span data-ttu-id="b6c9d-168">Указывает URL-адрес портала управления.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-168">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="b6c9d-169">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b6c9d-169">-Name</span></span>
<span data-ttu-id="b6c9d-170">Указывает имя среды, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-170">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-171">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="b6c9d-171">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="b6c9d-172">Указывает URL-адрес, с которого можно загрузить файлы publishsettings.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-172">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="b6c9d-173">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6c9d-173">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="b6c9d-174">Указывает URL-адрес для запросов диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-174">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="b6c9d-175">-Scope</span><span class="sxs-lookup"><span data-stu-id="b6c9d-175">-Scope</span></span>
<span data-ttu-id="b6c9d-176">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-176">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="b6c9d-177">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6c9d-177">-ServiceEndpoint</span></span>
<span data-ttu-id="b6c9d-178">Задает конечную точку для запросов на управление службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="b6c9d-178">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="b6c9d-179">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b6c9d-179">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="b6c9d-180">Указывает суффикс доменных имен для серверов баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-180">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="b6c9d-181">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="b6c9d-181">-StorageEndpoint</span></span>
<span data-ttu-id="b6c9d-182">Задает конечную точку для хранилища (BLOB-объектов, таблицы, очереди и файла).</span><span class="sxs-lookup"><span data-stu-id="b6c9d-182">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-183">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="b6c9d-183">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="b6c9d-184">Задает суффикс доменных имен для служб диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-184">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="b6c9d-185">-URI</span><span class="sxs-lookup"><span data-stu-id="b6c9d-185">-Uri</span></span>
<span data-ttu-id="b6c9d-186">Указывает URI интернет-ресурса для выборки сред.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-186">Specifies URI of the internet resource to fetch environments.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Discovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6c9d-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6c9d-187">-Confirm</span></span>
<span data-ttu-id="b6c9d-188">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6c9d-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6c9d-189">-WhatIf</span></span>
<span data-ttu-id="b6c9d-190">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6c9d-191">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6c9d-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c9d-192">CommonParameters</span></span>
<span data-ttu-id="b6c9d-193">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6c9d-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c9d-194">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6c9d-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c9d-195">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6c9d-195">INPUTS</span></span>

### <span data-ttu-id="b6c9d-196">System. String</span><span class="sxs-lookup"><span data-stu-id="b6c9d-196">System.String</span></span>

### <span data-ttu-id="b6c9d-197">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b6c9d-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b6c9d-198">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6c9d-198">OUTPUTS</span></span>

### <span data-ttu-id="b6c9d-199">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6c9d-199">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="b6c9d-200">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6c9d-200">NOTES</span></span>

## <span data-ttu-id="b6c9d-201">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6c9d-201">RELATED LINKS</span></span>

[<span data-ttu-id="b6c9d-202">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6c9d-202">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="b6c9d-203">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6c9d-203">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="b6c9d-204">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="b6c9d-204">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)
