---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 5cfe83c48950fff7f300b07cf43ba32ff9739606
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965907"
---
# <span data-ttu-id="8b2b0-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="8b2b0-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="8b2b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b2b0-102">SYNOPSIS</span></span>
<span data-ttu-id="8b2b0-103">Создание объекта PSBackendPool для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="8b2b0-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="8b2b0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b2b0-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b2b0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b2b0-105">DESCRIPTION</span></span>
<span data-ttu-id="8b2b0-106">Создание объекта PSBackendPool для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="8b2b0-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="8b2b0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b2b0-107">EXAMPLES</span></span>

### <span data-ttu-id="8b2b0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b2b0-108">Example 1</span></span>
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

<span data-ttu-id="8b2b0-109">Создание объекта PSBackendPool для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="8b2b0-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="8b2b0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b2b0-110">PARAMETERS</span></span>

### <span data-ttu-id="8b2b0-111">-Backend</span><span class="sxs-lookup"><span data-stu-id="8b2b0-111">-Backend</span></span>
<span data-ttu-id="8b2b0-112">Набор резервов для этого пула.</span><span class="sxs-lookup"><span data-stu-id="8b2b0-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="8b2b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2b0-113">-DefaultProfile</span></span>
<span data-ttu-id="8b2b0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b2b0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b2b0-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="8b2b0-115">-FrontDoorName</span></span>
<span data-ttu-id="8b2b0-116">Название переднего входа, к которому относится это правило маршрутинга.</span><span class="sxs-lookup"><span data-stu-id="8b2b0-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="8b2b0-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="8b2b0-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="8b2b0-118">Имя параметров проблемы с состоянием здоровья для этого пула</span><span class="sxs-lookup"><span data-stu-id="8b2b0-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="8b2b0-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="8b2b0-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="8b2b0-120">Имя параметров балансировки нагрузки для этого пула</span><span class="sxs-lookup"><span data-stu-id="8b2b0-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="8b2b0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8b2b0-121">-Name</span></span>
<span data-ttu-id="8b2b0-122">Имя backendPool.</span><span class="sxs-lookup"><span data-stu-id="8b2b0-122">BackendPool name.</span></span>

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

### <span data-ttu-id="8b2b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b2b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b2b0-124">Имя группы ресурсов, в которую будет создано RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="8b2b0-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="8b2b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2b0-125">CommonParameters</span></span>
<span data-ttu-id="8b2b0-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b2b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2b0-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b2b0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2b0-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b2b0-128">INPUTS</span></span>

### <span data-ttu-id="8b2b0-129">Нет</span><span class="sxs-lookup"><span data-stu-id="8b2b0-129">None</span></span>

## <span data-ttu-id="8b2b0-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b2b0-130">OUTPUTS</span></span>

### <span data-ttu-id="8b2b0-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="8b2b0-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="8b2b0-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b2b0-132">NOTES</span></span>

## <span data-ttu-id="8b2b0-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b2b0-133">RELATED LINKS</span></span>

<span data-ttu-id="8b2b0-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="8b2b0-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
