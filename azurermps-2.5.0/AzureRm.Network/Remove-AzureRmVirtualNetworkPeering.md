---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: de39828183f06f8435078ceffc8c303c376e6186
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915077"
---
# <span data-ttu-id="ebcf6-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ebcf6-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="ebcf6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebcf6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebcf6-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebcf6-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ebcf6-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebcf6-104">DESCRIPTION</span></span>

## <span data-ttu-id="ebcf6-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebcf6-105">EXAMPLES</span></span>

### <span data-ttu-id="ebcf6-106">Пример 1: удаление пиринга виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ebcf6-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="ebcf6-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebcf6-107">PARAMETERS</span></span>

### <span data-ttu-id="ebcf6-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebcf6-108">-AsJob</span></span>
<span data-ttu-id="ebcf6-109">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ebcf6-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebcf6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebcf6-110">-DefaultProfile</span></span>
<span data-ttu-id="ebcf6-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebcf6-112">-Force</span><span class="sxs-lookup"><span data-stu-id="ebcf6-112">-Force</span></span>
<span data-ttu-id="ebcf6-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ebcf6-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ebcf6-114">-Name</span></span>
<span data-ttu-id="ebcf6-115">Имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="ebcf6-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebcf6-116">-PassThru</span></span>
<span data-ttu-id="ebcf6-117">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ebcf6-118">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ebcf6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebcf6-119">-ResourceGroupName</span></span>
<span data-ttu-id="ebcf6-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ebcf6-120">The resource group name</span></span>

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

### <span data-ttu-id="ebcf6-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ebcf6-121">-VirtualNetworkName</span></span>
<span data-ttu-id="ebcf6-122">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-122">The virtual network name.</span></span>

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

### <span data-ttu-id="ebcf6-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebcf6-123">-Confirm</span></span>
<span data-ttu-id="ebcf6-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebcf6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebcf6-125">-WhatIf</span></span>
<span data-ttu-id="ebcf6-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebcf6-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebcf6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebcf6-128">CommonParameters</span></span>
<span data-ttu-id="ebcf6-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebcf6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebcf6-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebcf6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebcf6-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebcf6-131">INPUTS</span></span>

## <span data-ttu-id="ebcf6-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebcf6-132">OUTPUTS</span></span>

## <span data-ttu-id="ebcf6-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebcf6-133">NOTES</span></span>

## <span data-ttu-id="ebcf6-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebcf6-134">RELATED LINKS</span></span>

