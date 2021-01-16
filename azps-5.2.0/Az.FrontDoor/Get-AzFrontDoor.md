---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 8c378d7f0b1ac7a753f7f270fd3969eb881c7aec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407367"
---
# <span data-ttu-id="7eadb-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="7eadb-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="7eadb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eadb-102">SYNOPSIS</span></span>
<span data-ttu-id="7eadb-103">Получить балансировку загрузки переднего входа</span><span class="sxs-lookup"><span data-stu-id="7eadb-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="7eadb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7eadb-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7eadb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7eadb-105">DESCRIPTION</span></span>
<span data-ttu-id="7eadb-106">На **основе cmdletGet для Get-AzFrontDoor** в текущей подписке будут предоставляются все существующие двери переднего плану, которые совпадают с предоставленными сведениями.</span><span class="sxs-lookup"><span data-stu-id="7eadb-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="7eadb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7eadb-107">EXAMPLES</span></span>

### <span data-ttu-id="7eadb-108">Пример 1. Получить все FrontDoors в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="7eadb-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid1}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid2}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="7eadb-109">Получить все frontDoors в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="7eadb-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="7eadb-110">Пример 2. Получить все FrontDoors в группе ресурсов "rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="7eadb-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1

FriendlyName          : frontdoor2
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="7eadb-111">Получить все frontDoors в группе ресурсов "rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="7eadb-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="7eadb-112">Пример 3. Получить FrontDoors в группе ресурсов "rg1" с именем frontDoor1 в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="7eadb-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="7eadb-113">Получите frontDoors в группе ресурсов "rg1" с именем frontDoor1 в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="7eadb-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="7eadb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7eadb-114">PARAMETERS</span></span>

### <span data-ttu-id="7eadb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eadb-115">-DefaultProfile</span></span>
<span data-ttu-id="7eadb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7eadb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eadb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7eadb-117">-Name</span></span>
<span data-ttu-id="7eadb-118">Имя передней двери.</span><span class="sxs-lookup"><span data-stu-id="7eadb-118">Front Door name.</span></span>

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

### <span data-ttu-id="7eadb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eadb-119">-ResourceGroupName</span></span>
<span data-ttu-id="7eadb-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7eadb-120">The resource group name.</span></span>

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

### <span data-ttu-id="7eadb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eadb-121">CommonParameters</span></span>
<span data-ttu-id="7eadb-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eadb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eadb-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7eadb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eadb-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7eadb-124">INPUTS</span></span>

### <span data-ttu-id="7eadb-125">Нет</span><span class="sxs-lookup"><span data-stu-id="7eadb-125">None</span></span>

## <span data-ttu-id="7eadb-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7eadb-126">OUTPUTS</span></span>

### <span data-ttu-id="7eadb-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="7eadb-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="7eadb-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7eadb-128">NOTES</span></span>

## <span data-ttu-id="7eadb-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7eadb-129">RELATED LINKS</span></span>

<span data-ttu-id="7eadb-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="7eadb-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
