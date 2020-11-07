---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: 070ff5ee85687662d11cb30e3e3e7370b29ac251
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911861"
---
# <span data-ttu-id="0612a-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="0612a-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="0612a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0612a-102">SYNOPSIS</span></span>
<span data-ttu-id="0612a-103">Обновляет существующую службу healthcareApis fhir.</span><span class="sxs-lookup"><span data-stu-id="0612a-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="0612a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0612a-104">SYNTAX</span></span>

### <span data-ttu-id="0612a-105">ServiceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0612a-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0612a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0612a-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0612a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0612a-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0612a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0612a-108">DESCRIPTION</span></span>
<span data-ttu-id="0612a-109">Обновляет существующую службу healthcareApis fhir.</span><span class="sxs-lookup"><span data-stu-id="0612a-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="0612a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0612a-110">EXAMPLES</span></span>

### <span data-ttu-id="0612a-111">Например, 1: обновляет существующую службу healthcareapis с именем MyService в группе ресурсов MyResourceGroup с cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="0612a-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

### <span data-ttu-id="0612a-112">Пример 2: обновление существующей службы healthcareapis с именем MyService в группе ресурсов MyResourceGroup с cosmosdb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="0612a-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

## <span data-ttu-id="0612a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0612a-113">PARAMETERS</span></span>

### <span data-ttu-id="0612a-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="0612a-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="0612a-115">Список идентификаторов объектов политики доступа.</span><span class="sxs-lookup"><span data-stu-id="0612a-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="0612a-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="0612a-116">-AllowCorsCredential</span></span>
<span data-ttu-id="0612a-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="0612a-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="0612a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0612a-118">-AsJob</span></span>
<span data-ttu-id="0612a-119">Запустите командлет как задание в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="0612a-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="0612a-120">-Аудитория</span><span class="sxs-lookup"><span data-stu-id="0612a-120">-Audience</span></span>
<span data-ttu-id="0612a-121">HealthcareApis FhirService аудитория.</span><span class="sxs-lookup"><span data-stu-id="0612a-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="0612a-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="0612a-122">-Authority</span></span>
<span data-ttu-id="0612a-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="0612a-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="0612a-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="0612a-124">-CorsHeader</span></span>
<span data-ttu-id="0612a-125">HealthcareApis Fhir Service List (Заголовок CORS).</span><span class="sxs-lookup"><span data-stu-id="0612a-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="0612a-126">Укажите HTTP-заголовки, которые можно использовать во время запроса.</span><span class="sxs-lookup"><span data-stu-id="0612a-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="0612a-127">Используйте \* для любого заголовка.</span><span class="sxs-lookup"><span data-stu-id="0612a-127">Use \* for any header.</span></span>

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

### <span data-ttu-id="0612a-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="0612a-128">-CorsMaxAge</span></span>
<span data-ttu-id="0612a-129">Максимальный возраст службы HealthcareApis Fhir Service CORS.</span><span class="sxs-lookup"><span data-stu-id="0612a-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="0612a-130">Укажите, как долго можно кэшировать результаты запроса за считанные секунды.</span><span class="sxs-lookup"><span data-stu-id="0612a-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="0612a-131">Пример: 600 означает 10 минут.</span><span class="sxs-lookup"><span data-stu-id="0612a-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="0612a-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="0612a-132">-CorsMethod</span></span>
<span data-ttu-id="0612a-133">HealthcareApis FhirService список методов CORS.</span><span class="sxs-lookup"><span data-stu-id="0612a-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0612a-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="0612a-134">-CorsOrigin</span></span>
<span data-ttu-id="0612a-135">HealthcareApis FhirService список источников CORS.</span><span class="sxs-lookup"><span data-stu-id="0612a-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="0612a-136">HealthcareApis Fhir список служб в источнике CORS.</span><span class="sxs-lookup"><span data-stu-id="0612a-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="0612a-137">Укажите URL-адреса исходных сайтов, которые могут получать доступ к этому API или используйте \* для разрешения доступа с любого сайта.</span><span class="sxs-lookup"><span data-stu-id="0612a-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="0612a-138">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="0612a-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="0612a-139">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="0612a-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="0612a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0612a-140">-DefaultProfile</span></span>
<span data-ttu-id="0612a-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0612a-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0612a-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="0612a-142">-DisableCorsCredential</span></span>
<span data-ttu-id="0612a-143">HealthcareApis FhirService CorsCredentials не разрешено.</span><span class="sxs-lookup"><span data-stu-id="0612a-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="0612a-144">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="0612a-144">-DisableSmartProxy</span></span>
<span data-ttu-id="0612a-145">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="0612a-145">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="0612a-146">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="0612a-146">-EnableSmartProxy</span></span>
<span data-ttu-id="0612a-147">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="0612a-147">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="0612a-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0612a-148">-InputObject</span></span>
<span data-ttu-id="0612a-149">Служба HealthcareApis fhir, полученная от Get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="0612a-149">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="0612a-150">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0612a-150">-Name</span></span>
<span data-ttu-id="0612a-151">Имя службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="0612a-151">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="0612a-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0612a-152">-ResourceGroupName</span></span>
<span data-ttu-id="0612a-153">Имя группы ресурсов "служба HealthcareApis".</span><span class="sxs-lookup"><span data-stu-id="0612a-153">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="0612a-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0612a-154">-ResourceId</span></span>
<span data-ttu-id="0612a-155">HealthcareApis Fhir Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0612a-155">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="0612a-156">-Тег</span><span class="sxs-lookup"><span data-stu-id="0612a-156">-Tag</span></span>
<span data-ttu-id="0612a-157">HealthcareApis Fhir учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="0612a-157">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="0612a-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0612a-158">-Confirm</span></span>
<span data-ttu-id="0612a-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0612a-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0612a-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0612a-160">-WhatIf</span></span>
<span data-ttu-id="0612a-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0612a-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0612a-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0612a-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0612a-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0612a-163">CommonParameters</span></span>
<span data-ttu-id="0612a-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0612a-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0612a-165">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0612a-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0612a-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0612a-166">INPUTS</span></span>

### <span data-ttu-id="0612a-167">System. String</span><span class="sxs-lookup"><span data-stu-id="0612a-167">System.String</span></span>

### <span data-ttu-id="0612a-168">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="0612a-168">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="0612a-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0612a-169">OUTPUTS</span></span>

### <span data-ttu-id="0612a-170">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="0612a-170">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="0612a-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="0612a-171">NOTES</span></span>

## <span data-ttu-id="0612a-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0612a-172">RELATED LINKS</span></span>
