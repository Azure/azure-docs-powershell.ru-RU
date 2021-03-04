---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 2261e3e0f9237985459dc69e06ba4f055dd86427
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962664"
---
# <span data-ttu-id="fd83a-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="fd83a-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="fd83a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd83a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd83a-103">Сбрасывает routingState ресурса VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="fd83a-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="fd83a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fd83a-104">SYNTAX</span></span>

### <span data-ttu-id="fd83a-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd83a-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd83a-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="fd83a-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd83a-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="fd83a-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd83a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd83a-108">DESCRIPTION</span></span>
<span data-ttu-id="fd83a-109">Сбрасывает состояние маршрутации для существующего ресурса VirtualHub только в том случае, если состояние маршрутации виртуального концентратора не задано.</span><span class="sxs-lookup"><span data-stu-id="fd83a-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="fd83a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fd83a-110">EXAMPLES</span></span>

### <span data-ttu-id="fd83a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fd83a-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="fd83a-112">Сброс состояния маршрутировки виртуального концентратора с помощью его resourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="fd83a-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="fd83a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fd83a-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="fd83a-114">Сброс состояния маршрутов виртуального концентратора с помощью его ResourceId.</span><span class="sxs-lookup"><span data-stu-id="fd83a-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="fd83a-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="fd83a-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="fd83a-116">Сброс состояния маршрутов виртуального концентратора с помощью входного объекта.</span><span class="sxs-lookup"><span data-stu-id="fd83a-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="fd83a-117">Входной объект имеет тип PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="fd83a-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="fd83a-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="fd83a-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="fd83a-119">Существующий объект виртуального концентратора можно получить, а затем передать в качестве входного объекта для сброса AzHubRouter.</span><span class="sxs-lookup"><span data-stu-id="fd83a-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="fd83a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd83a-120">PARAMETERS</span></span>

### <span data-ttu-id="fd83a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd83a-121">-AsJob</span></span>
<span data-ttu-id="fd83a-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fd83a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd83a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd83a-123">-DefaultProfile</span></span>
<span data-ttu-id="fd83a-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd83a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd83a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="fd83a-125">-Force</span></span>
<span data-ttu-id="fd83a-126">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="fd83a-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fd83a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd83a-127">-InputObject</span></span>
<span data-ttu-id="fd83a-128">Объект виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="fd83a-128">The Virtual hub object to be modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd83a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="fd83a-129">-Name</span></span>
<span data-ttu-id="fd83a-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="fd83a-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd83a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd83a-131">-ResourceGroupName</span></span>
<span data-ttu-id="fd83a-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd83a-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd83a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd83a-133">-ResourceId</span></span>
<span data-ttu-id="fd83a-134">ИД ресурса виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="fd83a-134">The resource id of the Virtual hub to be modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd83a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd83a-135">-Confirm</span></span>
<span data-ttu-id="fd83a-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd83a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd83a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd83a-137">-WhatIf</span></span>
<span data-ttu-id="fd83a-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd83a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd83a-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fd83a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd83a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd83a-140">CommonParameters</span></span>
<span data-ttu-id="fd83a-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd83a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd83a-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd83a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd83a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd83a-143">INPUTS</span></span>

### <span data-ttu-id="fd83a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="fd83a-144">System.String</span></span>

### <span data-ttu-id="fd83a-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="fd83a-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="fd83a-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd83a-146">OUTPUTS</span></span>

### <span data-ttu-id="fd83a-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="fd83a-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="fd83a-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd83a-148">NOTES</span></span>

## <span data-ttu-id="fd83a-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd83a-149">RELATED LINKS</span></span>

[<span data-ttu-id="fd83a-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="fd83a-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
