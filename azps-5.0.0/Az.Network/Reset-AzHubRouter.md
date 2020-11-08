---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azhubrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzHubRouter.md
ms.openlocfilehash: 039d37f9d9dd7b5af026b7ce2a87113513949b67
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248818"
---
# <span data-ttu-id="0a2c7-101">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="0a2c7-101">Reset-AzHubRouter</span></span>

## <span data-ttu-id="0a2c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a2c7-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2c7-103">Сбрасывает RoutingState ресурса VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-103">Resets the RoutingState of a VirtualHub resource.</span></span>

## <span data-ttu-id="0a2c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a2c7-104">SYNTAX</span></span>

### <span data-ttu-id="0a2c7-105">ByVirtualHubName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a2c7-105">ByVirtualHubName (Default)</span></span>
```
Reset-AzHubRouter -ResourceGroupName <String> -Name <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a2c7-106">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2c7-106">ByVirtualHubResourceId</span></span>
```
Reset-AzHubRouter -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a2c7-107">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="0a2c7-107">ByVirtualHubObject</span></span>
```
Reset-AzHubRouter -InputObject <PSVirtualHub> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a2c7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a2c7-108">DESCRIPTION</span></span>
<span data-ttu-id="0a2c7-109">Сбрасывает состояние маршрутизации для существующего ресурса VirtualHub только в том случае, если состояние маршрутизации виртуального концентратора не настроено.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-109">Resets the Routing State of an existing VirtualHub resource only if the Routing State of the virtual hub is not Provisioned.</span></span>

## <span data-ttu-id="0a2c7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a2c7-110">EXAMPLES</span></span>

### <span data-ttu-id="0a2c7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0a2c7-111">Example 1</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceGroupName "testRG" -Name "westushub"
```

<span data-ttu-id="0a2c7-112">Сбросьте состояние маршрутизации виртуального концентратора, используя его ResourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-112">Reset the routing state of the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="0a2c7-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0a2c7-113">Example 2</span></span>

```powershell
PS C:\> Reset-AzHubRouter -ResourceId "/subscriptions/testSub/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub"
```

<span data-ttu-id="0a2c7-114">Сбросьте состояние маршрутизации виртуального концентратора с помощью ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-114">Reset the routing state of the virtual hub using its ResourceId.</span></span>

### <span data-ttu-id="0a2c7-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0a2c7-115">Example 3</span></span>

```powershell
PS C:\> Reset-AzHubRouter -InputObject $virtualHub
```

<span data-ttu-id="0a2c7-116">Сбросьте состояние маршрутизации виртуального концентратора с помощью объекта ввода.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-116">Reset the routing state of the virtual hub using an input object.</span></span> <span data-ttu-id="0a2c7-117">Входной объект имеет тип PSVirtualHub.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-117">The input object is of type PSVirtualHub.</span></span>

### <span data-ttu-id="0a2c7-118">Пример 4</span><span class="sxs-lookup"><span data-stu-id="0a2c7-118">Example 4</span></span>

```powershell
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub" | Reset-AzHubRouter
```

<span data-ttu-id="0a2c7-119">Существующий виртуальный объект-концентратор можно извлечь, а затем передать его в качестве объекта ввода для сброса-AzHubRouter.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-119">An existing virtual hub object can be retrieved and then passed as input object to Reset-AzHubRouter.</span></span>

## <span data-ttu-id="0a2c7-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a2c7-120">PARAMETERS</span></span>

### <span data-ttu-id="0a2c7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a2c7-121">-AsJob</span></span>
<span data-ttu-id="0a2c7-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0a2c7-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a2c7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a2c7-123">-DefaultProfile</span></span>
<span data-ttu-id="0a2c7-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a2c7-125">-Force</span><span class="sxs-lookup"><span data-stu-id="0a2c7-125">-Force</span></span>
<span data-ttu-id="0a2c7-126">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="0a2c7-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0a2c7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a2c7-127">-InputObject</span></span>
<span data-ttu-id="0a2c7-128">Объект виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-128">The Virtual hub object to be modified.</span></span>

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

### <span data-ttu-id="0a2c7-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a2c7-129">-Name</span></span>
<span data-ttu-id="0a2c7-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-130">The resource name.</span></span>

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

### <span data-ttu-id="0a2c7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a2c7-131">-ResourceGroupName</span></span>
<span data-ttu-id="0a2c7-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-132">The resource group name.</span></span>

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

### <span data-ttu-id="0a2c7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a2c7-133">-ResourceId</span></span>
<span data-ttu-id="0a2c7-134">Идентификатор ресурса виртуального концентратора, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-134">The resource id of the Virtual hub to be modified.</span></span>

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

### <span data-ttu-id="0a2c7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a2c7-135">-Confirm</span></span>
<span data-ttu-id="0a2c7-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a2c7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a2c7-137">-WhatIf</span></span>
<span data-ttu-id="0a2c7-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a2c7-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a2c7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2c7-140">CommonParameters</span></span>
<span data-ttu-id="0a2c7-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a2c7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2c7-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a2c7-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2c7-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a2c7-143">INPUTS</span></span>

### <span data-ttu-id="0a2c7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0a2c7-144">System.String</span></span>

### <span data-ttu-id="0a2c7-145">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0a2c7-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="0a2c7-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a2c7-146">OUTPUTS</span></span>

### <span data-ttu-id="0a2c7-147">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0a2c7-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="0a2c7-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a2c7-148">NOTES</span></span>

## <span data-ttu-id="0a2c7-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a2c7-149">RELATED LINKS</span></span>

[<span data-ttu-id="0a2c7-150">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0a2c7-150">Get-AzVirtualHub</span></span>](./Get-AzVirtualHub.md)
