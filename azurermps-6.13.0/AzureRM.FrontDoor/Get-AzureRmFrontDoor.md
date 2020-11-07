---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/get-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Get-AzureRmFrontDoor.md
ms.openlocfilehash: ca54e2cc86daca89a9872366dea32b375080c63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732934"
---
# <span data-ttu-id="b0019-101">Get-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="b0019-101">Get-AzureRmFrontDoor</span></span>

## <span data-ttu-id="b0019-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0019-102">SYNOPSIS</span></span>
<span data-ttu-id="b0019-103">Получение подсистемы балансировки нагрузки для передней дверцы</span><span class="sxs-lookup"><span data-stu-id="b0019-103">Get Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0019-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0019-104">SYNTAX</span></span>

```
Get-AzureRmFrontDoor [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0019-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0019-105">DESCRIPTION</span></span>
<span data-ttu-id="b0019-106">CmdletGet **Get-AzureRmFrontDoor** возвращает все существующие передние двери в текущей подписке, соответствующие указанным сведениям.</span><span class="sxs-lookup"><span data-stu-id="b0019-106">The **Get-AzureRmFrontDoor** cmdletGet gets all existing Front Doors in the current subscription that matches provided information.</span></span>

## <span data-ttu-id="b0019-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0019-107">EXAMPLES</span></span>

### <span data-ttu-id="b0019-108">Пример 1: получение всех FrontDoors в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="b0019-108">Example 1: Get all FrontDoors in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor

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

<span data-ttu-id="b0019-109">Получение всех FrontDoors в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="b0019-109">Get all FrontDoors in the current subscription.</span></span>

### <span data-ttu-id="b0019-110">Пример 2: получение всех FrontDoors в группе ресурсов "Rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="b0019-110">Example 2: Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1"

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

<span data-ttu-id="b0019-111">Получить все FrontDoors в группе ресурсов "Rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="b0019-111">Get all FrontDoors in resource group "rg1" in the current subscription.</span></span>

### <span data-ttu-id="b0019-112">Пример 3: получение FrontDoors в группе ресурсов "Rg1" с именем "frontDoor1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="b0019-112">Example 3: Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" -Name "frontDoor1"

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

<span data-ttu-id="b0019-113">Получить FrontDoors в группе ресурсов "Rg1" с именем "frontDoor1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="b0019-113">Get the FrontDoors in resource group "rg1" with name "frontDoor1" in the current subscription.</span></span>

## <span data-ttu-id="b0019-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0019-114">PARAMETERS</span></span>

### <span data-ttu-id="b0019-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0019-115">-DefaultProfile</span></span>
<span data-ttu-id="b0019-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0019-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0019-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b0019-117">-Name</span></span>
<span data-ttu-id="b0019-118">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="b0019-118">Front Door name.</span></span>

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

### <span data-ttu-id="b0019-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0019-119">-ResourceGroupName</span></span>
<span data-ttu-id="b0019-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0019-120">The resource group name.</span></span>

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

### <span data-ttu-id="b0019-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0019-121">CommonParameters</span></span>
<span data-ttu-id="b0019-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0019-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0019-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0019-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0019-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0019-124">INPUTS</span></span>

### <span data-ttu-id="b0019-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b0019-125">System.String</span></span>

## <span data-ttu-id="b0019-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0019-126">OUTPUTS</span></span>

### <span data-ttu-id="b0019-127">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="b0019-127">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="b0019-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0019-128">NOTES</span></span>

## <span data-ttu-id="b0019-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0019-129">RELATED LINKS</span></span>

<span data-ttu-id="b0019-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="b0019-130">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)</span></span>
