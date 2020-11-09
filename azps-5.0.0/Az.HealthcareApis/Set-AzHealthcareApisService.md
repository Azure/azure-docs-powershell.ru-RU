---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: a944982688dac8f9a28c10b3d26e71a8331451ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247374"
---
# <span data-ttu-id="49748-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="49748-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="49748-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49748-102">SYNOPSIS</span></span>
<span data-ttu-id="49748-103">Обновляет существующую службу healthcareApis fhir.</span><span class="sxs-lookup"><span data-stu-id="49748-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="49748-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49748-104">SYNTAX</span></span>

### <span data-ttu-id="49748-105">ServiceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49748-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49748-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49748-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity]
 [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49748-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49748-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49748-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49748-108">DESCRIPTION</span></span>
<span data-ttu-id="49748-109">Обновляет существующую службу healthcareApis fhir.</span><span class="sxs-lookup"><span data-stu-id="49748-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="49748-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49748-110">EXAMPLES</span></span>

### <span data-ttu-id="49748-111">Например, 1: обновляет существующую службу healthcareapis с именем MyService в группе ресурсов MyResourceGroup с cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="49748-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

### <span data-ttu-id="49748-112">Пример 2: обновление существующей службы healthcareapis с именем MyService в группе ресурсов MyResourceGroup с cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="49748-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
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

## <span data-ttu-id="49748-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49748-113">PARAMETERS</span></span>

### <span data-ttu-id="49748-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="49748-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="49748-115">Список идентификаторов объектов политики доступа.</span><span class="sxs-lookup"><span data-stu-id="49748-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="49748-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="49748-116">-AllowCorsCredential</span></span>
<span data-ttu-id="49748-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="49748-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="49748-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49748-118">-AsJob</span></span>
<span data-ttu-id="49748-119">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="49748-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="49748-120">-Аудитория</span><span class="sxs-lookup"><span data-stu-id="49748-120">-Audience</span></span>
<span data-ttu-id="49748-121">HealthcareApis FhirService аудитория.</span><span class="sxs-lookup"><span data-stu-id="49748-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="49748-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="49748-122">-Authority</span></span>
<span data-ttu-id="49748-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="49748-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="49748-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="49748-124">-CorsHeader</span></span>
<span data-ttu-id="49748-125">HealthcareApis Fhir Service List (Заголовок CORS).</span><span class="sxs-lookup"><span data-stu-id="49748-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="49748-126">Укажите HTTP-заголовки, которые можно использовать во время запроса.</span><span class="sxs-lookup"><span data-stu-id="49748-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="49748-127">Используйте \* для любого заголовка.</span><span class="sxs-lookup"><span data-stu-id="49748-127">Use \* for any header.</span></span>

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

### <span data-ttu-id="49748-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="49748-128">-CorsMaxAge</span></span>
<span data-ttu-id="49748-129">Максимальный возраст службы HealthcareApis Fhir Service CORS.</span><span class="sxs-lookup"><span data-stu-id="49748-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="49748-130">Укажите, как долго можно кэшировать результаты запроса за считанные секунды.</span><span class="sxs-lookup"><span data-stu-id="49748-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="49748-131">Пример: 600 означает 10 минут.</span><span class="sxs-lookup"><span data-stu-id="49748-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="49748-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="49748-132">-CorsMethod</span></span>
<span data-ttu-id="49748-133">HealthcareApis FhirService список методов CORS.</span><span class="sxs-lookup"><span data-stu-id="49748-133">HealthcareApis FhirService List of Cors Methods.</span></span>

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

### <span data-ttu-id="49748-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="49748-134">-CorsOrigin</span></span>
<span data-ttu-id="49748-135">HealthcareApis FhirService список источников CORS.</span><span class="sxs-lookup"><span data-stu-id="49748-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="49748-136">HealthcareApis Fhir список служб в источнике CORS.</span><span class="sxs-lookup"><span data-stu-id="49748-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="49748-137">Укажите URL-адреса исходных сайтов, которые могут получать доступ к этому API или используйте \* для разрешения доступа с любого сайта.</span><span class="sxs-lookup"><span data-stu-id="49748-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="49748-138">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="49748-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="49748-139">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="49748-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="49748-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49748-140">-DefaultProfile</span></span>
<span data-ttu-id="49748-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49748-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49748-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="49748-142">-DisableCorsCredential</span></span>
<span data-ttu-id="49748-143">HealthcareApis FhirService CorsCredentials не разрешено.</span><span class="sxs-lookup"><span data-stu-id="49748-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="49748-144">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="49748-144">-DisableManagedIdentity</span></span>
<span data-ttu-id="49748-145">Отключение управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="49748-145">Disable Managed Identity.</span></span>

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

### <span data-ttu-id="49748-146">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="49748-146">-DisableSmartProxy</span></span>
<span data-ttu-id="49748-147">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="49748-147">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="49748-148">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="49748-148">-EnableManagedIdentity</span></span>
<span data-ttu-id="49748-149">Включите управляемое удостоверение.</span><span class="sxs-lookup"><span data-stu-id="49748-149">Enable Managed Identity.</span></span>

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

### <span data-ttu-id="49748-150">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="49748-150">-EnableSmartProxy</span></span>
<span data-ttu-id="49748-151">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="49748-151">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="49748-152">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="49748-152">-ExportStorageAccountName</span></span>
<span data-ttu-id="49748-153">Имя учетной записи хранения для экспорта службы HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="49748-153">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="49748-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49748-154">-InputObject</span></span>
<span data-ttu-id="49748-155">Служба HealthcareApis fhir, полученная от Get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="49748-155">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="49748-156">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49748-156">-Name</span></span>
<span data-ttu-id="49748-157">Имя службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="49748-157">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="49748-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49748-158">-ResourceGroupName</span></span>
<span data-ttu-id="49748-159">Имя группы ресурсов "служба HealthcareApis".</span><span class="sxs-lookup"><span data-stu-id="49748-159">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="49748-160">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49748-160">-ResourceId</span></span>
<span data-ttu-id="49748-161">HealthcareApis Fhir Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="49748-161">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="49748-162">-Тег</span><span class="sxs-lookup"><span data-stu-id="49748-162">-Tag</span></span>
<span data-ttu-id="49748-163">HealthcareApis Fhir учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="49748-163">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="49748-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49748-164">-Confirm</span></span>
<span data-ttu-id="49748-165">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49748-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49748-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49748-166">-WhatIf</span></span>
<span data-ttu-id="49748-167">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49748-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49748-168">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49748-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49748-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49748-169">CommonParameters</span></span>
<span data-ttu-id="49748-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49748-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49748-171">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49748-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49748-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49748-172">INPUTS</span></span>

### <span data-ttu-id="49748-173">System. String</span><span class="sxs-lookup"><span data-stu-id="49748-173">System.String</span></span>

### <span data-ttu-id="49748-174">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="49748-174">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="49748-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49748-175">OUTPUTS</span></span>

### <span data-ttu-id="49748-176">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="49748-176">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="49748-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="49748-177">NOTES</span></span>

## <span data-ttu-id="49748-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49748-178">RELATED LINKS</span></span>