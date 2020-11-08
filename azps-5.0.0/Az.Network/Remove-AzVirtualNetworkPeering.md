---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248299"
---
# <span data-ttu-id="ef7f8-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ef7f8-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="ef7f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef7f8-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7f8-103">Удаление пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ef7f8-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="ef7f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef7f8-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef7f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef7f8-105">DESCRIPTION</span></span>
<span data-ttu-id="ef7f8-106">Удаление пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ef7f8-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="ef7f8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef7f8-107">EXAMPLES</span></span>

### <span data-ttu-id="ef7f8-108">Пример 1: удаление пиринга виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ef7f8-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="ef7f8-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef7f8-109">PARAMETERS</span></span>

### <span data-ttu-id="ef7f8-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef7f8-110">-AsJob</span></span>
<span data-ttu-id="ef7f8-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ef7f8-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef7f8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7f8-112">-DefaultProfile</span></span>
<span data-ttu-id="ef7f8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef7f8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef7f8-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ef7f8-114">-Force</span></span>
<span data-ttu-id="ef7f8-115">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef7f8-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ef7f8-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef7f8-116">-Name</span></span>
<span data-ttu-id="ef7f8-117">Имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ef7f8-117">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7f8-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef7f8-118">-PassThru</span></span>
<span data-ttu-id="ef7f8-119">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ef7f8-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ef7f8-120">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ef7f8-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef7f8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef7f8-121">-ResourceGroupName</span></span>
<span data-ttu-id="ef7f8-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ef7f8-122">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7f8-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ef7f8-123">-VirtualNetworkName</span></span>
<span data-ttu-id="ef7f8-124">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ef7f8-124">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef7f8-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef7f8-125">-Confirm</span></span>
<span data-ttu-id="ef7f8-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef7f8-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7f8-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef7f8-127">-WhatIf</span></span>
<span data-ttu-id="ef7f8-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef7f8-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef7f8-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef7f8-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7f8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7f8-130">CommonParameters</span></span>
<span data-ttu-id="ef7f8-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef7f8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7f8-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef7f8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7f8-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef7f8-133">INPUTS</span></span>

### <span data-ttu-id="ef7f8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ef7f8-134">System.String</span></span>

## <span data-ttu-id="ef7f8-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef7f8-135">OUTPUTS</span></span>

### <span data-ttu-id="ef7f8-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef7f8-136">System.Boolean</span></span>

## <span data-ttu-id="ef7f8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef7f8-137">NOTES</span></span>

## <span data-ttu-id="ef7f8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef7f8-138">RELATED LINKS</span></span>

[<span data-ttu-id="ef7f8-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ef7f8-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="ef7f8-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ef7f8-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="ef7f8-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ef7f8-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
