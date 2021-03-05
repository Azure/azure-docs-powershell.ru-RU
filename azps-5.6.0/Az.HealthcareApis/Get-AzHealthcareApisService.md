---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: ca41e87c0f17ef62033cab0966296a307f90a457
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013192"
---
# <span data-ttu-id="76f70-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="76f70-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="76f70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76f70-102">SYNOPSIS</span></span>
<span data-ttu-id="76f70-103">Получите метаданные экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="76f70-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="76f70-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76f70-104">SYNTAX</span></span>

### <span data-ttu-id="76f70-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76f70-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76f70-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="76f70-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76f70-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76f70-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76f70-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76f70-108">DESCRIPTION</span></span>
<span data-ttu-id="76f70-109">Получает существующие учетные записи службы healthcareApis, созданные в рамках указанной подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76f70-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="76f70-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76f70-110">EXAMPLES</span></span>

### <span data-ttu-id="76f70-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76f70-111">Example 1</span></span>
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

### <span data-ttu-id="76f70-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="76f70-112">Example 2</span></span>

<span data-ttu-id="76f70-113">Возвращает метаданные для всех служб HealthcareApis в предоставленной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76f70-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

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

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
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

### <span data-ttu-id="76f70-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="76f70-114">Example 3</span></span>

<span data-ttu-id="76f70-115">Получает метаданные для всех служб HealthcareApis в данной подписке</span><span class="sxs-lookup"><span data-stu-id="76f70-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

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

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
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

## <span data-ttu-id="76f70-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76f70-116">PARAMETERS</span></span>

### <span data-ttu-id="76f70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f70-117">-DefaultProfile</span></span>
<span data-ttu-id="76f70-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76f70-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76f70-119">-Name</span><span class="sxs-lookup"><span data-stu-id="76f70-119">-Name</span></span>
<span data-ttu-id="76f70-120">Имя службы HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="76f70-120">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="76f70-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f70-121">-ResourceGroupName</span></span>
<span data-ttu-id="76f70-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76f70-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="76f70-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76f70-123">-ResourceId</span></span>
<span data-ttu-id="76f70-124">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="76f70-124">Resource Id Name.</span></span>

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

### <span data-ttu-id="76f70-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f70-125">CommonParameters</span></span>
<span data-ttu-id="76f70-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f70-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f70-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76f70-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f70-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76f70-128">INPUTS</span></span>

### <span data-ttu-id="76f70-129">System.String</span><span class="sxs-lookup"><span data-stu-id="76f70-129">System.String</span></span>

## <span data-ttu-id="76f70-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76f70-130">OUTPUTS</span></span>

### <span data-ttu-id="76f70-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="76f70-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="76f70-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76f70-132">NOTES</span></span>

## <span data-ttu-id="76f70-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76f70-133">RELATED LINKS</span></span>
