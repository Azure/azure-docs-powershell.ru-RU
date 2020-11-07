---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoor.md
ms.openlocfilehash: 8c378d7f0b1ac7a753f7f270fd3969eb881c7aec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911998"
---
# <span data-ttu-id="8741f-101">Get-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="8741f-101">Get-AzFrontDoor</span></span>

## <span data-ttu-id="8741f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8741f-102">SYNOPSIS</span></span>
<span data-ttu-id="8741f-103">Получение подсистемы балансировки нагрузки для передней дверцы</span><span class="sxs-lookup"><span data-stu-id="8741f-103">Get Front Door load balancer</span></span>

## <span data-ttu-id="8741f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8741f-104">SYNTAX</span></span>

```
Get-AzFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8741f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8741f-105">DESCRIPTION</span></span>
<span data-ttu-id="8741f-106">CmdletGet **Get-AzFrontDoor** возвращает все существующие передние двери в текущей подписке, соответствующие указанным сведениям.</span><span class="sxs-lookup"><span data-stu-id="8741f-106">The **Get-AzFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="8741f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8741f-107">EXAMPLES</span></span>

### <span data-ttu-id="8741f-108">Пример 1: получение всех FrontDoors в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="8741f-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
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

<span data-ttu-id="8741f-109">Получение всех FrontDoors в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="8741f-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="8741f-110">Пример 2: получение всех FrontDoors в группе ресурсов "Rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="8741f-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
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

<span data-ttu-id="8741f-111">Получить все FrontDoors в группе ресурсов "Rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="8741f-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="8741f-112">Пример 3: получение FrontDoors в группе ресурсов "Rg1" с именем "frontDoor1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="8741f-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
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

<span data-ttu-id="8741f-113">Получить FrontDoors в группе ресурсов "Rg1" с именем "frontDoor1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="8741f-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="8741f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8741f-114">PARAMETERS</span></span>

### <span data-ttu-id="8741f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8741f-115">-DefaultProfile</span></span>
<span data-ttu-id="8741f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8741f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8741f-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8741f-117">-Name</span></span>
<span data-ttu-id="8741f-118">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="8741f-118">Front Door name.</span></span>

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

### <span data-ttu-id="8741f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8741f-119">-ResourceGroupName</span></span>
<span data-ttu-id="8741f-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8741f-120">The resource group name.</span></span>

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

### <span data-ttu-id="8741f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8741f-121">CommonParameters</span></span>
<span data-ttu-id="8741f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8741f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8741f-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8741f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8741f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8741f-124">INPUTS</span></span>

### <span data-ttu-id="8741f-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="8741f-125">None</span></span>

## <span data-ttu-id="8741f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8741f-126">OUTPUTS</span></span>

### <span data-ttu-id="8741f-127">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="8741f-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="8741f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8741f-128">NOTES</span></span>

## <span data-ttu-id="8741f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8741f-129">RELATED LINKS</span></span>

<span data-ttu-id="8741f-130">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="8741f-130">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)</span></span>
