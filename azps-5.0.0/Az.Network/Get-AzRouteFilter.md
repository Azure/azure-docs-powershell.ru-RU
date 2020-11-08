---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 88b755a8865a5ce07a5dc86c94958de0c0e72485
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249696"
---
# <span data-ttu-id="64d85-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="64d85-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="64d85-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64d85-102">SYNOPSIS</span></span>
<span data-ttu-id="64d85-103">Получает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="64d85-103">Gets a route filter.</span></span>

## <span data-ttu-id="64d85-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64d85-104">SYNTAX</span></span>

### <span data-ttu-id="64d85-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="64d85-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64d85-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="64d85-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64d85-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64d85-107">DESCRIPTION</span></span>
<span data-ttu-id="64d85-108">Командлет **Get-AzRouteFilter** получает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="64d85-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="64d85-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64d85-109">EXAMPLES</span></span>

### <span data-ttu-id="64d85-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="64d85-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="64d85-111">Эта команда получает фильтр маршрутов с именем RouteFilter01, который принадлежит группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="64d85-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="64d85-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="64d85-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter*"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []

Name              : RouteFilter02
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter02
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="64d85-113">Эта команда получает все фильтры маршрутов, которые начинаются с "RouteFilter".</span><span class="sxs-lookup"><span data-stu-id="64d85-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="64d85-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64d85-114">PARAMETERS</span></span>

### <span data-ttu-id="64d85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d85-115">-DefaultProfile</span></span>
<span data-ttu-id="64d85-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64d85-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64d85-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="64d85-117">-ExpandResource</span></span>
<span data-ttu-id="64d85-118">Развернутая ссылка на ресурс.</span><span class="sxs-lookup"><span data-stu-id="64d85-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d85-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="64d85-119">-Name</span></span>
<span data-ttu-id="64d85-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="64d85-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="64d85-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d85-121">-ResourceGroupName</span></span>
<span data-ttu-id="64d85-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64d85-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="64d85-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d85-123">CommonParameters</span></span>
<span data-ttu-id="64d85-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64d85-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d85-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64d85-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d85-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64d85-126">INPUTS</span></span>

### <span data-ttu-id="64d85-127">System. String</span><span class="sxs-lookup"><span data-stu-id="64d85-127">System.String</span></span>

## <span data-ttu-id="64d85-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64d85-128">OUTPUTS</span></span>

### <span data-ttu-id="64d85-129">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="64d85-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="64d85-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="64d85-130">NOTES</span></span>

## <span data-ttu-id="64d85-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64d85-131">RELATED LINKS</span></span>

[<span data-ttu-id="64d85-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="64d85-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="64d85-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="64d85-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="64d85-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="64d85-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="64d85-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64d85-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="64d85-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64d85-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="64d85-137">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64d85-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="64d85-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64d85-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="64d85-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64d85-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
