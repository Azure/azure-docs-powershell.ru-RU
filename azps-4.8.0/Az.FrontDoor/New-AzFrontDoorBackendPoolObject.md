---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 6dba24ae79d051668e88a718402c5e01e81a7461
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077763"
---
# <span data-ttu-id="225ba-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="225ba-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="225ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="225ba-102">SYNOPSIS</span></span>
<span data-ttu-id="225ba-103">Создание объекта PSBackendPool для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="225ba-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="225ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="225ba-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="225ba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="225ba-105">DESCRIPTION</span></span>
<span data-ttu-id="225ba-106">Создание объекта PSBackendPool для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="225ba-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="225ba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="225ba-107">EXAMPLES</span></span>

### <span data-ttu-id="225ba-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="225ba-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
althProbeSettingsName "healthProbeSetting1" -LoadBalancingSettingsName "loadBalancingSetting1"


Backends                : {Microsoft.Azure.Commands.FrontDoor.Models.PSBackend}
LoadBalancingSettingRef : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/LoadBalancingSettings/loadBalancingSetting1
HealthProbeSettingRef   : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/HealthProbeSettings/healthProbeSetting1
EnabledState            : Enabled
ResourceState           :
Id                      :
Name                    : backendpool1
Type                    :
```

<span data-ttu-id="225ba-109">Создание объекта PSBackendPool для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="225ba-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="225ba-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="225ba-110">PARAMETERS</span></span>

### <span data-ttu-id="225ba-111">-Внутренний</span><span class="sxs-lookup"><span data-stu-id="225ba-111">-Backend</span></span>
<span data-ttu-id="225ba-112">Набор незавершенных элементов для этого пула.</span><span class="sxs-lookup"><span data-stu-id="225ba-112">The set of backends for this pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackend[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225ba-113">-DefaultProfile</span></span>
<span data-ttu-id="225ba-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="225ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="225ba-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="225ba-115">-FrontDoorName</span></span>
<span data-ttu-id="225ba-116">Имя передней дверцы, к которой относится данное правило маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="225ba-116">The name of the Front Door to which this routing rule belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225ba-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="225ba-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="225ba-118">Имя параметров проверки работоспособности для этого пула серверной базы данных</span><span class="sxs-lookup"><span data-stu-id="225ba-118">The name of the health probe settings for this backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225ba-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="225ba-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="225ba-120">Имя параметров балансировки нагрузки для этого пула баз данных.</span><span class="sxs-lookup"><span data-stu-id="225ba-120">The name of the load balancing settings for this backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225ba-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="225ba-121">-Name</span></span>
<span data-ttu-id="225ba-122">BackendPool имя.</span><span class="sxs-lookup"><span data-stu-id="225ba-122">BackendPool name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225ba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="225ba-123">-ResourceGroupName</span></span>
<span data-ttu-id="225ba-124">Имя группы ресурсов, в которой будет создано RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="225ba-124">The resource group name that the RoutingRule will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225ba-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225ba-125">CommonParameters</span></span>
<span data-ttu-id="225ba-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="225ba-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225ba-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="225ba-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225ba-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="225ba-128">INPUTS</span></span>

### <span data-ttu-id="225ba-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="225ba-129">None</span></span>

## <span data-ttu-id="225ba-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="225ba-130">OUTPUTS</span></span>

### <span data-ttu-id="225ba-131">Microsoft. Azure. Commands. FrontDoor. Models. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="225ba-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="225ba-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="225ba-132">NOTES</span></span>

## <span data-ttu-id="225ba-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="225ba-133">RELATED LINKS</span></span>

<span data-ttu-id="225ba-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="225ba-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>