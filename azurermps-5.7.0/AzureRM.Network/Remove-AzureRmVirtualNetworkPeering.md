---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: a128f7c9e9440255ed01b32c4460ffd180655928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568987"
---
# <span data-ttu-id="b90fb-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b90fb-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="b90fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b90fb-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b90fb-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b90fb-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b90fb-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b90fb-104">DESCRIPTION</span></span>

## <span data-ttu-id="b90fb-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b90fb-105">EXAMPLES</span></span>

### <span data-ttu-id="b90fb-106">Пример 1: удаление пиринга виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="b90fb-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="b90fb-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b90fb-107">PARAMETERS</span></span>

### <span data-ttu-id="b90fb-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b90fb-108">-AsJob</span></span>
<span data-ttu-id="b90fb-109">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b90fb-109">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90fb-110">-DefaultProfile</span></span>
<span data-ttu-id="b90fb-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b90fb-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b90fb-112">-Force</span></span>
<span data-ttu-id="b90fb-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b90fb-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b90fb-114">-Name</span></span>
<span data-ttu-id="b90fb-115">Имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b90fb-115">The virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b90fb-116">-PassThru</span></span>
<span data-ttu-id="b90fb-117">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b90fb-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b90fb-118">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b90fb-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b90fb-119">-ResourceGroupName</span></span>
<span data-ttu-id="b90fb-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b90fb-120">The resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b90fb-121">-VirtualNetworkName</span></span>
<span data-ttu-id="b90fb-122">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b90fb-122">The virtual network name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b90fb-123">-Confirm</span></span>
<span data-ttu-id="b90fb-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b90fb-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b90fb-125">-WhatIf</span></span>
<span data-ttu-id="b90fb-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b90fb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b90fb-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b90fb-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90fb-128">CommonParameters</span></span>
<span data-ttu-id="b90fb-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b90fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b90fb-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b90fb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90fb-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b90fb-131">INPUTS</span></span>

### <span data-ttu-id="b90fb-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="b90fb-132">None</span></span>
<span data-ttu-id="b90fb-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b90fb-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b90fb-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b90fb-134">OUTPUTS</span></span>

## <span data-ttu-id="b90fb-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="b90fb-135">NOTES</span></span>

## <span data-ttu-id="b90fb-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b90fb-136">RELATED LINKS</span></span>

