---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 33f1af70b0fef7e89ccb584ed3b69f32e2810690
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426108"
---
# <span data-ttu-id="93689-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="93689-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="93689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93689-102">SYNOPSIS</span></span>
<span data-ttu-id="93689-103">Создание метаданных экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="93689-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="93689-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="93689-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93689-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93689-105">DESCRIPTION</span></span>
<span data-ttu-id="93689-106">Создание или обновление метаданных экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="93689-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="93689-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="93689-107">EXAMPLES</span></span>

### <span data-ttu-id="93689-108">Пример 1. Создание новой службы Azure healthcareapis fhir с именем MyService в группе ресурсов MyResourceGroup в расположении westus2 с пропускной способностью предложения "1sdb" = 400</span><span class="sxs-lookup"><span data-stu-id="93689-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : 
CosmosDbOfferThroughput : 400
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

### <span data-ttu-id="93689-109">Пример 2. Создание новой службы Azure healthcareapis fhir с именем MyService в группе ресурсов MyResourceGroup в расположении westus2 с пропускной способностью предложения "400" и ключом ключа хранилища "https:// \<my-keyvault> \<my-key> .vault.azure.net/keys/"</span><span class="sxs-lookup"><span data-stu-id="93689-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : https://<my-keyvault>.vault.azure.net/keys/<my-key>
CosmosDbOfferThroughput : 400
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

## <span data-ttu-id="93689-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93689-110">PARAMETERS</span></span>

### <span data-ttu-id="93689-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="93689-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="93689-112">Список ИД объектов политики Access.</span><span class="sxs-lookup"><span data-stu-id="93689-112">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93689-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="93689-113">-AllowCorsCredential</span></span>
<span data-ttu-id="93689-114">HealthcareApis Fhir Service AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="93689-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="93689-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93689-115">-AsJob</span></span>
<span data-ttu-id="93689-116">Запуск cmdlet в качестве задания в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="93689-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="93689-117">-Audience</span><span class="sxs-lookup"><span data-stu-id="93689-117">-Audience</span></span>
<span data-ttu-id="93689-118">HealthcareApis Fhir Service Audience.</span><span class="sxs-lookup"><span data-stu-id="93689-118">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="93689-119">-Authority</span><span class="sxs-lookup"><span data-stu-id="93689-119">-Authority</span></span>
<span data-ttu-id="93689-120">HealthcareApis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="93689-120">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="93689-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="93689-121">-CorsHeader</span></span>
<span data-ttu-id="93689-122">HealthcareApis Fhir Service List of Cors Header.</span><span class="sxs-lookup"><span data-stu-id="93689-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="93689-123">Укажите заглавные протоколы HTTP, которые можно использовать во время запроса.</span><span class="sxs-lookup"><span data-stu-id="93689-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="93689-124">Используйте \* для любого заглавия.</span><span class="sxs-lookup"><span data-stu-id="93689-124">Use " \* " for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93689-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="93689-125">-CorsMaxAge</span></span>
<span data-ttu-id="93689-126">HealthcareApis Fhir Service Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="93689-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="93689-127">Укажите, как долго результат запроса можно кэшизировать в секундах.</span><span class="sxs-lookup"><span data-stu-id="93689-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="93689-128">Пример: 600 означает 10 минут.</span><span class="sxs-lookup"><span data-stu-id="93689-128">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93689-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="93689-129">-CorsMethod</span></span>
<span data-ttu-id="93689-130">HealthcareApis Fhir Service List of Cors Method.</span><span class="sxs-lookup"><span data-stu-id="93689-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93689-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="93689-131">-CorsOrigin</span></span>
<span data-ttu-id="93689-132">HealthcareApis Fhir Service List of Cors Origin.</span><span class="sxs-lookup"><span data-stu-id="93689-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="93689-133">Укажите URL-адреса сайтов-источников, которые могут получать доступ к этому API, или используйте " \*", чтобы разрешить доступ с любого сайта.</span><span class="sxs-lookup"><span data-stu-id="93689-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93689-134">-АsKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="93689-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="93689-135">HealthcareApis Fhir ServiceHirsKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="93689-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="93689-136">URI управляемого клиентом ключа базы данных.</span><span class="sxs-lookup"><span data-stu-id="93689-136">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="93689-137">-ThsOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="93689-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="93689-138">HealthcareApis Fhir ServiceHirsOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="93689-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93689-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93689-139">-DefaultProfile</span></span>
<span data-ttu-id="93689-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93689-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93689-141">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="93689-141">-EnableSmartProxy</span></span>
<span data-ttu-id="93689-142">HealthcareApis Fhir Service EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="93689-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="93689-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="93689-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="93689-144">Имя учетной записи службы экспорта службы HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="93689-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="93689-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="93689-145">-FhirVersion</span></span>
<span data-ttu-id="93689-146">Версия Fhir.</span><span class="sxs-lookup"><span data-stu-id="93689-146">Fhir Version.</span></span>

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

### <span data-ttu-id="93689-147">-Kind</span><span class="sxs-lookup"><span data-stu-id="93689-147">-Kind</span></span>
<span data-ttu-id="93689-148">Тип службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="93689-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="93689-149">Значение по умолчанию — Fhir</span><span class="sxs-lookup"><span data-stu-id="93689-149">The default value is Fhir</span></span>

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

### <span data-ttu-id="93689-150">-Location</span><span class="sxs-lookup"><span data-stu-id="93689-150">-Location</span></span>
<span data-ttu-id="93689-151">Расположение службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="93689-151">HealthcareApis Service Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93689-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="93689-152">-ManagedIdentity</span></span>
<span data-ttu-id="93689-153">Используете управляемое удостоверение?</span><span class="sxs-lookup"><span data-stu-id="93689-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="93689-154">-Name</span><span class="sxs-lookup"><span data-stu-id="93689-154">-Name</span></span>
<span data-ttu-id="93689-155">Имя службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="93689-155">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93689-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="93689-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="93689-157">Тип доступа к сети для службы FHIR.</span><span class="sxs-lookup"><span data-stu-id="93689-157">The network access type for Fhir service.</span></span> <span data-ttu-id="93689-158">Обычно или `Enabled` `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="93689-158">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93689-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93689-159">-ResourceGroupName</span></span>
<span data-ttu-id="93689-160">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93689-160">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93689-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="93689-161">-Tag</span></span>
<span data-ttu-id="93689-162">HealthcareApis Fhir Service Account Tags.</span><span class="sxs-lookup"><span data-stu-id="93689-162">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93689-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93689-163">-Confirm</span></span>
<span data-ttu-id="93689-164">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93689-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93689-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93689-165">-WhatIf</span></span>
<span data-ttu-id="93689-166">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93689-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93689-167">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="93689-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93689-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93689-168">CommonParameters</span></span>
<span data-ttu-id="93689-169">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93689-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93689-170">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93689-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93689-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93689-171">INPUTS</span></span>

### <span data-ttu-id="93689-172">System.String</span><span class="sxs-lookup"><span data-stu-id="93689-172">System.String</span></span>

## <span data-ttu-id="93689-173">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93689-173">OUTPUTS</span></span>

### <span data-ttu-id="93689-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="93689-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="93689-175">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="93689-175">NOTES</span></span>

## <span data-ttu-id="93689-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93689-176">RELATED LINKS</span></span>
