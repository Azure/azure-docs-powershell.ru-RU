---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 502a15c4d102932e32fb103a80f55c8b3acfee3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967112"
---
# <span data-ttu-id="ac4eb-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="ac4eb-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="ac4eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ac4eb-103">Задает свойства среды Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="ac4eb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac4eb-104">SYNTAX</span></span>

### <span data-ttu-id="ac4eb-105">Имя (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac4eb-105">Name (Default)</span></span>
```
Set-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
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
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac4eb-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac4eb-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac4eb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac4eb-107">DESCRIPTION</span></span>
<span data-ttu-id="ac4eb-108">Этот Set-AzEnvironment задает конечные точки и метаданные для подключения к экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="ac4eb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac4eb-109">EXAMPLES</span></span>

### <span data-ttu-id="ac4eb-110">Пример 1. Создание и изменение новой среды</span><span class="sxs-lookup"><span data-stu-id="ac4eb-110">Example 1: Creating and modifying a new environment</span></span>
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

PS C:\> Set-AzEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint | Format-List

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
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
```

<span data-ttu-id="ac4eb-111">В этом примере мы создаем новую среду Azure с образцами конечных точек с помощью Add-AzEnvironment, а затем изменяем значение атрибутов ActiveDirectoryEndpoint и GraphEndpoint созданной среды с помощью cmdlet Set-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="ac4eb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac4eb-112">PARAMETERS</span></span>

### <span data-ttu-id="ac4eb-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac4eb-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="ac4eb-114">Указывает базовый орган проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="ac4eb-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ac4eb-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="ac4eb-116">Определяет аудиторию для токенов, которые запрашивают проверку подлинности в конечных точках Диспетчера ресурсов Azure или служб управления службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="ac4eb-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="ac4eb-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="ac4eb-117">-AdTenant</span></span>
<span data-ttu-id="ac4eb-118">Определяет клиент Active Directory по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="ac4eb-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac4eb-119">-ARMEndpoint</span></span>
<span data-ttu-id="ac4eb-120">Конечная точка Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="ac4eb-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ac4eb-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="ac4eb-122">Идентификатор ресурса служб Azure Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="ac4eb-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ac4eb-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="ac4eb-124">Конечная точка, используемая при общении с Azure Log Analytics API.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="ac4eb-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ac4eb-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="ac4eb-126">Идентификатор ресурса службы Azure Attestation, который является получателем запрашиваемого маркера.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="ac4eb-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ac4eb-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="ac4eb-128">DNS-суффикс службы Azure Attestation.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="ac4eb-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ac4eb-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="ac4eb-130">DNS-суффикс служб Azure Data Lake Analytics и служб каталога</span><span class="sxs-lookup"><span data-stu-id="ac4eb-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="ac4eb-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ac4eb-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="ac4eb-132">Суффикс DNS для Azure Data Lake Store FileSystem.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="ac4eb-133">Пример: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="ac4eb-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="ac4eb-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="ac4eb-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="ac4eb-135">DNS-суффикс службы хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="ac4eb-136">Пример: vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="ac4eb-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="ac4eb-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ac4eb-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="ac4eb-138">Идентификатор ресурса службы данных хранилища ключа Azure, который является получателем запрашиваемого маркера.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="ac4eb-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac4eb-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="ac4eb-140">Конечная точка, используемая при общении с Azure Log Analytics API.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="ac4eb-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ac4eb-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="ac4eb-142">Аудитория для проверки подлинности токенов с помощью API Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="ac4eb-143">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ac4eb-143">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="ac4eb-144">Идентификатор ресурса средства аналитики Azure SynapseAnalytics, который является получателем запрашиваемого маркера.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-144">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="ac4eb-145">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ac4eb-145">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="ac4eb-146">DNS-суффикс службы Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-146">Dns suffix of Azure Synapse Analytics.</span></span>

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

### <span data-ttu-id="ac4eb-147">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ac4eb-147">-BatchEndpointResourceId</span></span>
<span data-ttu-id="ac4eb-148">Идентификатор ресурса службы Azure Batch, который является получателем запрашиваемого маркера.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-148">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="ac4eb-149">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ac4eb-149">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="ac4eb-150">Суффикс реестра контейнеров Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-150">Suffix of Azure Container Registry.</span></span>

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

### <span data-ttu-id="ac4eb-151">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="ac4eb-151">-DataLakeAudience</span></span>
<span data-ttu-id="ac4eb-152">Аудитория маркеров для проверки подлинности с помощью конечной точки служб AD Data Lake services.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-152">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="ac4eb-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac4eb-153">-DefaultProfile</span></span>
<span data-ttu-id="ac4eb-154">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-154">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac4eb-155">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="ac4eb-155">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="ac4eb-156">Указывает на то, что разрешена проверка локальной проверки подлинности в службах федерации Active Directory (ADFS).</span><span class="sxs-lookup"><span data-stu-id="ac4eb-156">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="ac4eb-157">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac4eb-157">-GalleryEndpoint</span></span>
<span data-ttu-id="ac4eb-158">Указывает конечную точку для коллекции шаблонов развертывания Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-158">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="ac4eb-159">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="ac4eb-159">-GraphAudience</span></span>
<span data-ttu-id="ac4eb-160">Аудитория маркеров для проверки подлинности с помощью конечной точки AD Graph.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-160">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="ac4eb-161">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac4eb-161">-GraphEndpoint</span></span>
<span data-ttu-id="ac4eb-162">Url-адрес запросов Graph (метаданных Active Directory).</span><span class="sxs-lookup"><span data-stu-id="ac4eb-162">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="ac4eb-163">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="ac4eb-163">-ManagementPortalUrl</span></span>
<span data-ttu-id="ac4eb-164">Url-адрес портала управления.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-164">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="ac4eb-165">-Name</span><span class="sxs-lookup"><span data-stu-id="ac4eb-165">-Name</span></span>
<span data-ttu-id="ac4eb-166">Указывает имя среды, которая будет изменяться.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-166">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="ac4eb-167">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="ac4eb-167">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="ac4eb-168">Url-адрес, с которого можно скачать файлы Publishsettings.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-168">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="ac4eb-169">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac4eb-169">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="ac4eb-170">URL-адрес запросов Диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-170">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="ac4eb-171">-Scope</span><span class="sxs-lookup"><span data-stu-id="ac4eb-171">-Scope</span></span>
<span data-ttu-id="ac4eb-172">Определяет область изменения контекста, например, применяются ли изменения только к текущему процессу или же к всем сеансам, на которые начал пользователь.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-172">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="ac4eb-173">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac4eb-173">-ServiceEndpoint</span></span>
<span data-ttu-id="ac4eb-174">Указывает конечную точку для запросов на управление службами (RDFE).</span><span class="sxs-lookup"><span data-stu-id="ac4eb-174">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="ac4eb-175">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="ac4eb-175">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="ac4eb-176">Определяет суффикс доменного имени для серверов баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-176">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="ac4eb-177">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="ac4eb-177">-StorageEndpoint</span></span>
<span data-ttu-id="ac4eb-178">Указывает конечную точку доступа к хранилищу (BLOB-файлы, таблицы, очереди и файла).</span><span class="sxs-lookup"><span data-stu-id="ac4eb-178">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="ac4eb-179">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="ac4eb-179">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="ac4eb-180">Определяет суффикс доменного имени для служб Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-180">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="ac4eb-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac4eb-181">-Confirm</span></span>
<span data-ttu-id="ac4eb-182">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac4eb-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac4eb-183">-WhatIf</span></span>
<span data-ttu-id="ac4eb-184">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac4eb-185">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac4eb-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac4eb-186">CommonParameters</span></span>
<span data-ttu-id="ac4eb-187">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac4eb-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac4eb-188">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac4eb-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac4eb-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac4eb-189">INPUTS</span></span>

### <span data-ttu-id="ac4eb-190">System.String</span><span class="sxs-lookup"><span data-stu-id="ac4eb-190">System.String</span></span>

### <span data-ttu-id="ac4eb-191">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ac4eb-191">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ac4eb-192">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac4eb-192">OUTPUTS</span></span>

### <span data-ttu-id="ac4eb-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="ac4eb-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="ac4eb-194">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac4eb-194">NOTES</span></span>

## <span data-ttu-id="ac4eb-195">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac4eb-195">RELATED LINKS</span></span>

[<span data-ttu-id="ac4eb-196">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="ac4eb-196">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="ac4eb-197">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="ac4eb-197">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="ac4eb-198">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="ac4eb-198">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

