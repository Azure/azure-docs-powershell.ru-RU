---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
ms.openlocfilehash: 13b28d236e1c6e758c4f7883285c55017ce5a727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732932"
---
# <span data-ttu-id="c59f7-101">New-AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="c59f7-101">New-AzureRmFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="c59f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c59f7-102">SYNOPSIS</span></span>
<span data-ttu-id="c59f7-103">Создание объекта PSBackendPool для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="c59f7-103">Create a PSBackendPool object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c59f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c59f7-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c59f7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c59f7-105">DESCRIPTION</span></span>
<span data-ttu-id="c59f7-106">Создание объекта PSBackendPool для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="c59f7-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="c59f7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c59f7-107">EXAMPLES</span></span>

### <span data-ttu-id="c59f7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c59f7-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
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

<span data-ttu-id="c59f7-109">Создание объекта PSBackendPool для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="c59f7-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="c59f7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c59f7-110">PARAMETERS</span></span>

### <span data-ttu-id="c59f7-111">-Внутренний</span><span class="sxs-lookup"><span data-stu-id="c59f7-111">-Backend</span></span>
<span data-ttu-id="c59f7-112">Набор незавершенных элементов для этого пула.</span><span class="sxs-lookup"><span data-stu-id="c59f7-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="c59f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59f7-113">-DefaultProfile</span></span>
<span data-ttu-id="c59f7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c59f7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c59f7-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="c59f7-115">-FrontDoorName</span></span>
<span data-ttu-id="c59f7-116">Имя передней дверцы, к которой относится данное правило маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="c59f7-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="c59f7-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="c59f7-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="c59f7-118">Имя параметров проверки работоспособности для этого пула серверной базы данных</span><span class="sxs-lookup"><span data-stu-id="c59f7-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="c59f7-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="c59f7-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="c59f7-120">Имя параметров балансировки нагрузки для этого пула баз данных.</span><span class="sxs-lookup"><span data-stu-id="c59f7-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="c59f7-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c59f7-121">-Name</span></span>
<span data-ttu-id="c59f7-122">BackendPool имя.</span><span class="sxs-lookup"><span data-stu-id="c59f7-122">BackendPool name.</span></span>

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

### <span data-ttu-id="c59f7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c59f7-123">-ResourceGroupName</span></span>
<span data-ttu-id="c59f7-124">Имя группы ресурсов, в которой будет создано RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="c59f7-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="c59f7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59f7-125">CommonParameters</span></span>
<span data-ttu-id="c59f7-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c59f7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59f7-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c59f7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59f7-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c59f7-128">INPUTS</span></span>

### <span data-ttu-id="c59f7-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="c59f7-129">None</span></span>

## <span data-ttu-id="c59f7-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c59f7-130">OUTPUTS</span></span>

### <span data-ttu-id="c59f7-131">Microsoft. Azure. Commands. FrontDoor. Models. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="c59f7-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="c59f7-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="c59f7-132">NOTES</span></span>

## <span data-ttu-id="c59f7-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c59f7-133">RELATED LINKS</span></span>

<span data-ttu-id="c59f7-134">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="c59f7-134">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span></span>
