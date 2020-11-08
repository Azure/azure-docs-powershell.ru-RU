---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: d1a6edc3365631f93d2bc3b7a0e153ec360c2611
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243378"
---
# <span data-ttu-id="45a59-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="45a59-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="45a59-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45a59-102">SYNOPSIS</span></span>
<span data-ttu-id="45a59-103">Получение метаданных экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="45a59-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="45a59-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45a59-104">SYNTAX</span></span>

### <span data-ttu-id="45a59-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45a59-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45a59-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="45a59-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45a59-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="45a59-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45a59-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45a59-108">DESCRIPTION</span></span>
<span data-ttu-id="45a59-109">Получает существующие учетные записи служб healthcareApis fhir, созданные в указанной подписке или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45a59-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="45a59-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45a59-110">EXAMPLES</span></span>

### <span data-ttu-id="45a59-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45a59-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -Name "MyService" -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
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

### <span data-ttu-id="45a59-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="45a59-112">Example 2</span></span>

<span data-ttu-id="45a59-113">Получает метаданные для всех служб HealthcareApis в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45a59-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
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

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="45a59-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="45a59-114">Example 3</span></span>

<span data-ttu-id="45a59-115">Получает метаданные для всех служб HealthcareApis в данной подписке.</span><span class="sxs-lookup"><span data-stu-id="45a59-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
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

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="45a59-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45a59-116">PARAMETERS</span></span>

### <span data-ttu-id="45a59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a59-117">-DefaultProfile</span></span>
<span data-ttu-id="45a59-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45a59-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45a59-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45a59-119">-Name</span></span>
<span data-ttu-id="45a59-120">Имя службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="45a59-120">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a59-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a59-121">-ResourceGroupName</span></span>
<span data-ttu-id="45a59-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45a59-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="45a59-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45a59-123">-ResourceId</span></span>
<span data-ttu-id="45a59-124">Имя идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="45a59-124">Resource Id Name.</span></span>

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

### <span data-ttu-id="45a59-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a59-125">CommonParameters</span></span>
<span data-ttu-id="45a59-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45a59-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a59-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45a59-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a59-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45a59-128">INPUTS</span></span>

### <span data-ttu-id="45a59-129">System. String</span><span class="sxs-lookup"><span data-stu-id="45a59-129">System.String</span></span>

## <span data-ttu-id="45a59-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45a59-130">OUTPUTS</span></span>

### <span data-ttu-id="45a59-131">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="45a59-131">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="45a59-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="45a59-132">NOTES</span></span>

## <span data-ttu-id="45a59-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45a59-133">RELATED LINKS</span></span>