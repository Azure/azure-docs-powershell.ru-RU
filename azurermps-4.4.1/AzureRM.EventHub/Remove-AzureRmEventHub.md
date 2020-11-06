---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 22904260488c716ffb702f47442dc8f4678ebe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569468"
---
# <span data-ttu-id="e4705-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="e4705-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="e4705-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4705-102">SYNOPSIS</span></span>
<span data-ttu-id="e4705-103">Удаляет указанный центр событий.</span><span class="sxs-lookup"><span data-stu-id="e4705-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4705-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4705-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e4705-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4705-105">DESCRIPTION</span></span>
<span data-ttu-id="e4705-106">Командлет Remove-AzureRmEventHub удаляет и удаляет указанный концентратор событий из заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e4705-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="e4705-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4705-107">EXAMPLES</span></span>

### <span data-ttu-id="e4705-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e4705-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="e4705-109">Удаляет MyEventHubName концентратора \` событий \` .</span><span class="sxs-lookup"><span data-stu-id="e4705-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="e4705-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4705-110">PARAMETERS</span></span>

### <span data-ttu-id="e4705-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4705-111">-ResourceGroupName</span></span>
<span data-ttu-id="e4705-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e4705-112">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4705-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4705-113">-Confirm</span></span>
<span data-ttu-id="e4705-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e4705-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4705-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4705-115">-WhatIf</span></span>
<span data-ttu-id="e4705-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e4705-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4705-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e4705-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4705-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e4705-118">-Name</span></span>
<span data-ttu-id="e4705-119">Имя EventHub.</span><span class="sxs-lookup"><span data-stu-id="e4705-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4705-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e4705-120">-Namespace</span></span>
<span data-ttu-id="e4705-121">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e4705-121">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="e4705-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4705-122">INPUTS</span></span>

### <span data-ttu-id="e4705-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e4705-123">System.String</span></span>

## <span data-ttu-id="e4705-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4705-124">OUTPUTS</span></span>

### <span data-ttu-id="e4705-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="e4705-125">System.Object</span></span>

## <span data-ttu-id="e4705-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4705-126">NOTES</span></span>

## <span data-ttu-id="e4705-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4705-127">RELATED LINKS</span></span>

