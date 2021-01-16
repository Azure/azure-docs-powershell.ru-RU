---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 38530b5e4034286d623c82b841064760fe2e49e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519939"
---
# <span data-ttu-id="fd7ad-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fd7ad-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="fd7ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd7ad-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7ad-103">Удаляет виртуальный сетевой пиринг.</span><span class="sxs-lookup"><span data-stu-id="fd7ad-103">Removes a virtual network peering.</span></span>

## <span data-ttu-id="fd7ad-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fd7ad-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd7ad-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd7ad-105">DESCRIPTION</span></span>
<span data-ttu-id="fd7ad-106">Удаляет виртуальный сетевой пиринг.</span><span class="sxs-lookup"><span data-stu-id="fd7ad-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="fd7ad-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fd7ad-107">EXAMPLES</span></span>

### <span data-ttu-id="fd7ad-108">Пример 1. Удаление виртуального сетевого пиринга</span><span class="sxs-lookup"><span data-stu-id="fd7ad-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="fd7ad-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd7ad-109">PARAMETERS</span></span>

### <span data-ttu-id="fd7ad-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd7ad-110">-AsJob</span></span>
<span data-ttu-id="fd7ad-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fd7ad-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd7ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7ad-112">-DefaultProfile</span></span>
<span data-ttu-id="fd7ad-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd7ad-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd7ad-114">-Force</span><span class="sxs-lookup"><span data-stu-id="fd7ad-114">-Force</span></span>
<span data-ttu-id="fd7ad-115">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="fd7ad-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd7ad-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fd7ad-116">-Name</span></span>
<span data-ttu-id="fd7ad-117">Имя виртуального сетевого пиринга.</span><span class="sxs-lookup"><span data-stu-id="fd7ad-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="fd7ad-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd7ad-118">-PassThru</span></span>
<span data-ttu-id="fd7ad-119">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="fd7ad-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fd7ad-120">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fd7ad-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd7ad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7ad-121">-ResourceGroupName</span></span>
<span data-ttu-id="fd7ad-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fd7ad-122">The resource group name</span></span>

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

### <span data-ttu-id="fd7ad-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fd7ad-123">-VirtualNetworkName</span></span>
<span data-ttu-id="fd7ad-124">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="fd7ad-124">The virtual network name.</span></span>

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

### <span data-ttu-id="fd7ad-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd7ad-125">-Confirm</span></span>
<span data-ttu-id="fd7ad-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd7ad-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd7ad-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd7ad-127">-WhatIf</span></span>
<span data-ttu-id="fd7ad-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd7ad-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd7ad-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fd7ad-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd7ad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7ad-130">CommonParameters</span></span>
<span data-ttu-id="fd7ad-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd7ad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7ad-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7ad-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7ad-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd7ad-133">INPUTS</span></span>

### <span data-ttu-id="fd7ad-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fd7ad-134">System.String</span></span>

## <span data-ttu-id="fd7ad-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd7ad-135">OUTPUTS</span></span>

### <span data-ttu-id="fd7ad-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fd7ad-136">System.Boolean</span></span>

## <span data-ttu-id="fd7ad-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd7ad-137">NOTES</span></span>

## <span data-ttu-id="fd7ad-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd7ad-138">RELATED LINKS</span></span>

[<span data-ttu-id="fd7ad-139">Add-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fd7ad-139">Add-AzVirtualNetworkPeering</span></span>](./Add-AzVirtualNetworkPeering.md)

[<span data-ttu-id="fd7ad-140">Get-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fd7ad-140">Get-AzVirtualNetworkPeering</span></span>](./Get-AzVirtualNetworkPeering.md)

[<span data-ttu-id="fd7ad-141">Set-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="fd7ad-141">Set-AzVirtualNetworkPeering</span></span>](./Set-AzVirtualNetworkPeering.md)
