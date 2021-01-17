---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405388"
---
# <span data-ttu-id="b0b6e-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="b0b6e-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="b0b6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b6e-103">Сбрасывает routingState ресурса VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="b0b6e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0b6e-104">SYNTAX</span></span>

### <span data-ttu-id="b0b6e-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b0b6e-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0b6e-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="b0b6e-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0b6e-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="b0b6e-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0b6e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0b6e-108">DESCRIPTION</span></span>
<span data-ttu-id="b0b6e-109">Сбрасывает состояние маршрутации для существующего ресурса VirtualHub только в том случае, если состояние маршрутации виртуального концентратора не задано.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="b0b6e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0b6e-110">EXAMPLES</span></span>

### <span data-ttu-id="b0b6e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0b6e-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="b0b6e-112">Сброс состояния маршрутировки виртуального концентратора с помощью его resourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="b0b6e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b0b6e-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="b0b6e-114">Сброс состояния маршрутов виртуального концентратора с помощью его ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="b0b6e-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="b0b6e-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="b0b6e-116">Сброс состояния маршрутов виртуального концентратора с помощью входного объекта.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="b0b6e-117">Входной объект имеет тип PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="b0b6e-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="b0b6e-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="b0b6e-119">Существующий объект виртуального концентратора можно получить, а затем передать в качестве входного объекта для сброса AzHubRouter.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="b0b6e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0b6e-120">PARAMETERS</span></span>

### <span data-ttu-id="b0b6e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0b6e-121">-AsJob</span></span>
<span data-ttu-id="b0b6e-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b0b6e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0b6e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b6e-123">-DefaultProfile</span></span>
<span data-ttu-id="b0b6e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0b6e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b0b6e-125">-Force</span></span>
<span data-ttu-id="b0b6e-126">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="b0b6e-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b0b6e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0b6e-127">-InputObject</span></span>
<span data-ttu-id="b0b6e-128">Объект виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="b0b6e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="b0b6e-129">-Name</span></span>
<span data-ttu-id="b0b6e-130">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-130">The resource name.</span></span>

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

### <span data-ttu-id="b0b6e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b6e-131">-ResourceGroupName</span></span>
<span data-ttu-id="b0b6e-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-132">The resource group name.</span></span>

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

### <span data-ttu-id="b0b6e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0b6e-133">-ResourceId</span></span>
<span data-ttu-id="b0b6e-134">ИД ресурса виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="b0b6e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0b6e-135">-Confirm</span></span>
<span data-ttu-id="b0b6e-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0b6e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0b6e-137">-WhatIf</span></span>
<span data-ttu-id="b0b6e-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0b6e-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0b6e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b6e-140">CommonParameters</span></span>
<span data-ttu-id="b0b6e-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b6e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b6e-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0b6e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b6e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0b6e-143">INPUTS</span></span>

### <span data-ttu-id="b0b6e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b0b6e-144">System.String</span></span>

### <span data-ttu-id="b0b6e-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b0b6e-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="b0b6e-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0b6e-146">OUTPUTS</span></span>

### <span data-ttu-id="b0b6e-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b0b6e-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="b0b6e-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0b6e-148">NOTES</span></span>

## <span data-ttu-id="b0b6e-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0b6e-149">RELATED LINKS</span></span>

[<span data-ttu-id="b0b6e-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="b0b6e-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
