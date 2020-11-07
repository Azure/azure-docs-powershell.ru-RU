---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: 2b1e781a65eaa6a43c4f8571caf1850f0b04d6cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735054"
---
# <span data-ttu-id="f865d-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="f865d-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="f865d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f865d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f865d-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f865d-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f865d-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f865d-104">DESCRIPTION</span></span>

## <span data-ttu-id="f865d-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f865d-105">EXAMPLES</span></span>

### <span data-ttu-id="f865d-106">Пример 1: удаление пиринга виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="f865d-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="f865d-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f865d-107">PARAMETERS</span></span>

### <span data-ttu-id="f865d-108">-Force</span><span class="sxs-lookup"><span data-stu-id="f865d-108">-Force</span></span>
<span data-ttu-id="f865d-109">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f865d-109">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f865d-110">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f865d-110">-Name</span></span>
<span data-ttu-id="f865d-111">Имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f865d-111">The virtual network peering name.</span></span>

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

### <span data-ttu-id="f865d-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f865d-112">-PassThru</span></span>
<span data-ttu-id="f865d-113">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f865d-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f865d-114">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f865d-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f865d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f865d-115">-ResourceGroupName</span></span>
<span data-ttu-id="f865d-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f865d-116">The resource group name</span></span>

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

### <span data-ttu-id="f865d-117">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f865d-117">-VirtualNetworkName</span></span>
<span data-ttu-id="f865d-118">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="f865d-118">The virtual network name.</span></span>

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

### <span data-ttu-id="f865d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f865d-119">-Confirm</span></span>
<span data-ttu-id="f865d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f865d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f865d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f865d-121">-WhatIf</span></span>
<span data-ttu-id="f865d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f865d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f865d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f865d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f865d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f865d-124">-DefaultProfile</span></span>
<span data-ttu-id="f865d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f865d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f865d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f865d-126">CommonParameters</span></span>
<span data-ttu-id="f865d-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f865d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f865d-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f865d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f865d-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f865d-129">INPUTS</span></span>

## <span data-ttu-id="f865d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f865d-130">OUTPUTS</span></span>

## <span data-ttu-id="f865d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f865d-131">NOTES</span></span>

## <span data-ttu-id="f865d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f865d-132">RELATED LINKS</span></span>

