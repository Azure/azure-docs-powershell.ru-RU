---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 73e4fb2dde10739176a1adfe55c22529e8ccdaaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562811"
---
# <span data-ttu-id="695dd-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="695dd-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="695dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="695dd-102">SYNOPSIS</span></span>
<span data-ttu-id="695dd-103">Удаление пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="695dd-103">Removes a virtual network peering.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="695dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="695dd-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="695dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="695dd-105">DESCRIPTION</span></span>
<span data-ttu-id="695dd-106">Удаление пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="695dd-106">Removes a virtual network peering.</span></span>

## <span data-ttu-id="695dd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="695dd-107">EXAMPLES</span></span>

### <span data-ttu-id="695dd-108">Пример 1: удаление пиринга виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="695dd-108">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="695dd-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="695dd-109">PARAMETERS</span></span>

### <span data-ttu-id="695dd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="695dd-110">-AsJob</span></span>
<span data-ttu-id="695dd-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="695dd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="695dd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695dd-112">-DefaultProfile</span></span>
<span data-ttu-id="695dd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="695dd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="695dd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="695dd-114">-Force</span></span>
<span data-ttu-id="695dd-115">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="695dd-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="695dd-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="695dd-116">-Name</span></span>
<span data-ttu-id="695dd-117">Имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="695dd-117">The virtual network peering name.</span></span>

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

### <span data-ttu-id="695dd-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="695dd-118">-PassThru</span></span>
<span data-ttu-id="695dd-119">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="695dd-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="695dd-120">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="695dd-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="695dd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="695dd-121">-ResourceGroupName</span></span>
<span data-ttu-id="695dd-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="695dd-122">The resource group name</span></span>

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

### <span data-ttu-id="695dd-123">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="695dd-123">-VirtualNetworkName</span></span>
<span data-ttu-id="695dd-124">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="695dd-124">The virtual network name.</span></span>

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

### <span data-ttu-id="695dd-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="695dd-125">-Confirm</span></span>
<span data-ttu-id="695dd-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="695dd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="695dd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="695dd-127">-WhatIf</span></span>
<span data-ttu-id="695dd-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="695dd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="695dd-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="695dd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="695dd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695dd-130">CommonParameters</span></span>
<span data-ttu-id="695dd-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="695dd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695dd-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="695dd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695dd-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="695dd-133">INPUTS</span></span>

### <span data-ttu-id="695dd-134">System. String</span><span class="sxs-lookup"><span data-stu-id="695dd-134">System.String</span></span>

## <span data-ttu-id="695dd-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="695dd-135">OUTPUTS</span></span>

### <span data-ttu-id="695dd-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="695dd-136">System.Boolean</span></span>

## <span data-ttu-id="695dd-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="695dd-137">NOTES</span></span>

## <span data-ttu-id="695dd-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="695dd-138">RELATED LINKS</span></span>
