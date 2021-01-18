---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: c8eb7c58300e3252422d8b599422a3a14eb5c1fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507238"
---
# <span data-ttu-id="be3dd-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="be3dd-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="be3dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be3dd-102">SYNOPSIS</span></span>
<span data-ttu-id="be3dd-103">Обновляет существующую службу healthcareApis fhir.</span><span class="sxs-lookup"><span data-stu-id="be3dd-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="be3dd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="be3dd-104">SYNTAX</span></span>

### <span data-ttu-id="be3dd-105">ServiceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be3dd-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-CosmosKeyVaultKeyUri <String>] [-Authority <String>] [-Audience <String>] [-EnableSmartProxy]
 [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>] [-CorsMethod <String[]>]
 [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential] [-ExportStorageAccountName <String>]
 [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>]
 [-AsJob] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be3dd-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be3dd-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be3dd-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be3dd-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be3dd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be3dd-108">DESCRIPTION</span></span>
<span data-ttu-id="be3dd-109">Обновляет существующую службу healthcareApis fhir.</span><span class="sxs-lookup"><span data-stu-id="be3dd-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="be3dd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="be3dd-110">EXAMPLES</span></span>

### <span data-ttu-id="be3dd-111">Пример 1. Обновляет существующую службу healthcareapis с именем MyService в группе ресурсов MyResourceGroup, задав значение 500 (500) для службы "1" (1).</span><span class="sxs-lookup"><span data-stu-id="be3dd-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> Set-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : 
CosmosDbOfferThroughput : 500
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="be3dd-112">Пример 2. Обновляет существующую службу healthcareapis с именем MyService в группе ресурсов MyResourceGroup с помощью uri ключа URI хранилища 500 и uri ключа хранилища uri "https:// \<my-keyvault> \<my-key> .vault.azure.net/keys/"</span><span class="sxs-lookup"><span data-stu-id="be3dd-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : https://<my-keyvault>.vault.azure.net/keys/<my-key>
CosmosDbOfferThroughput : 500
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="be3dd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be3dd-113">PARAMETERS</span></span>

### <span data-ttu-id="be3dd-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="be3dd-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="be3dd-115">Список ИД объектов политики Access.</span><span class="sxs-lookup"><span data-stu-id="be3dd-115">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="be3dd-116">-AllowCorsCredential</span></span>
<span data-ttu-id="be3dd-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="be3dd-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be3dd-118">-AsJob</span></span>
<span data-ttu-id="be3dd-119">Запуск cmdlet в качестве задания в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="be3dd-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-120">-Audience</span><span class="sxs-lookup"><span data-stu-id="be3dd-120">-Audience</span></span>
<span data-ttu-id="be3dd-121">HealthcareApis FhirService Audience.</span><span class="sxs-lookup"><span data-stu-id="be3dd-121">HealthcareApis FhirService Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="be3dd-122">-Authority</span></span>
<span data-ttu-id="be3dd-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="be3dd-123">HealthcareApis FhirService Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="be3dd-124">-CorsHeader</span></span>
<span data-ttu-id="be3dd-125">HealthcareApis FhirService List of Cors Headers.</span><span class="sxs-lookup"><span data-stu-id="be3dd-125">HealthcareApis FhirService List of Cors Headers.</span></span>
<span data-ttu-id="be3dd-126">Укажите заглавные протоколы HTTP, которые можно использовать во время запроса.</span><span class="sxs-lookup"><span data-stu-id="be3dd-126">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="be3dd-127">Используйте \* для любого заглавия.</span><span class="sxs-lookup"><span data-stu-id="be3dd-127">Use " \* " for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="be3dd-128">-CorsMaxAge</span></span>
<span data-ttu-id="be3dd-129">HealthcareApis FhirService Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="be3dd-129">HealthcareApis FhirService Cors Max Age.</span></span>
<span data-ttu-id="be3dd-130">Укажите, как долго результат запроса можно кэшизировать в секундах.</span><span class="sxs-lookup"><span data-stu-id="be3dd-130">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="be3dd-131">Пример: 600 означает 10 минут.</span><span class="sxs-lookup"><span data-stu-id="be3dd-131">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="be3dd-132">-CorsMethod</span></span>
<span data-ttu-id="be3dd-133">HealthcareApis FhirService List of Cors Methods.</span><span class="sxs-lookup"><span data-stu-id="be3dd-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="be3dd-134">-CorsOrigin</span></span>
<span data-ttu-id="be3dd-135">HealthcareApis FhirService List of Cors Origins.</span><span class="sxs-lookup"><span data-stu-id="be3dd-135">HealthcareApis FhirService List of Cors Origins.</span></span>
<span data-ttu-id="be3dd-136">Укажите URL-адреса сайтов-источников, которые могут получить доступ к этому API, или используйте \*, чтобы разрешить доступ с любого сайта.</span><span class="sxs-lookup"><span data-stu-id="be3dd-136">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-137">-АsKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="be3dd-137">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="be3dd-138">HealthcareApis Fhir ServiceHirsKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="be3dd-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="be3dd-139">URI управляемого клиентом ключа базы данных.</span><span class="sxs-lookup"><span data-stu-id="be3dd-139">The URI of the customer-managed key for the backing database.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-140">-ThsOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="be3dd-140">-CosmosOfferThroughput</span></span>
<span data-ttu-id="be3dd-141">HealthcareApis FhirServiceOughsOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="be3dd-141">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be3dd-142">-DefaultProfile</span></span>
<span data-ttu-id="be3dd-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be3dd-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be3dd-144">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="be3dd-144">-DisableCorsCredential</span></span>
<span data-ttu-id="be3dd-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span><span class="sxs-lookup"><span data-stu-id="be3dd-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-146">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="be3dd-146">-DisableManagedIdentity</span></span>
<span data-ttu-id="be3dd-147">Отключать управляемые удостоверения.</span><span class="sxs-lookup"><span data-stu-id="be3dd-147">Disable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-148">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="be3dd-148">-DisableSmartProxy</span></span>
<span data-ttu-id="be3dd-149">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="be3dd-149">HealthcareApis FhirService DisableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-150">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="be3dd-150">-EnableManagedIdentity</span></span>
<span data-ttu-id="be3dd-151">Включить управляемые удостоверения.</span><span class="sxs-lookup"><span data-stu-id="be3dd-151">Enable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-152">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="be3dd-152">-EnableSmartProxy</span></span>
<span data-ttu-id="be3dd-153">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="be3dd-153">HealthcareApis FhirService EnableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-154">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="be3dd-154">-ExportStorageAccountName</span></span>
<span data-ttu-id="be3dd-155">Имя учетной записи службы экспорта службы HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="be3dd-155">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be3dd-156">-InputObject</span></span>
<span data-ttu-id="be3dd-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="be3dd-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-158">-Name</span><span class="sxs-lookup"><span data-stu-id="be3dd-158">-Name</span></span>
<span data-ttu-id="be3dd-159">Имя службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="be3dd-159">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-160">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="be3dd-160">-PublicNetworkAccess</span></span>
<span data-ttu-id="be3dd-161">Тип доступа к сети для службы FHIR.</span><span class="sxs-lookup"><span data-stu-id="be3dd-161">The network access type for Fhir service.</span></span> <span data-ttu-id="be3dd-162">Обычно или `Enabled` `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="be3dd-162">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be3dd-163">-ResourceGroupName</span></span>
<span data-ttu-id="be3dd-164">Имя группы ресурсов службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="be3dd-164">HealthcareApis Service Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-165">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be3dd-165">-ResourceId</span></span>
<span data-ttu-id="be3dd-166">HealthcareApis Fhir Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="be3dd-166">HealthcareApis Fhir Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="be3dd-167">-Tag</span></span>
<span data-ttu-id="be3dd-168">HealthcareApis Fhir Service Account Tags.</span><span class="sxs-lookup"><span data-stu-id="be3dd-168">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be3dd-169">-Confirm</span></span>
<span data-ttu-id="be3dd-170">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be3dd-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be3dd-171">-WhatIf</span></span>
<span data-ttu-id="be3dd-172">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be3dd-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be3dd-173">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="be3dd-173">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be3dd-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be3dd-174">CommonParameters</span></span>
<span data-ttu-id="be3dd-175">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be3dd-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be3dd-176">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be3dd-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be3dd-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be3dd-177">INPUTS</span></span>

### <span data-ttu-id="be3dd-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="be3dd-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="be3dd-179">System.String</span><span class="sxs-lookup"><span data-stu-id="be3dd-179">System.String</span></span>

## <span data-ttu-id="be3dd-180">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be3dd-180">OUTPUTS</span></span>

### <span data-ttu-id="be3dd-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="be3dd-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="be3dd-182">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="be3dd-182">NOTES</span></span>

## <span data-ttu-id="be3dd-183">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be3dd-183">RELATED LINKS</span></span>
