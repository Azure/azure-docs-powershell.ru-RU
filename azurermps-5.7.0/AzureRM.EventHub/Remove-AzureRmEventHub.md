---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: b546c4f610bb6bc8021547fa5f7f0516ffbc2371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569988"
---
# <span data-ttu-id="00227-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="00227-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="00227-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00227-102">SYNOPSIS</span></span>
<span data-ttu-id="00227-103">Удаляет указанный центр событий.</span><span class="sxs-lookup"><span data-stu-id="00227-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00227-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00227-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00227-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00227-105">DESCRIPTION</span></span>
<span data-ttu-id="00227-106">Командлет Remove-AzureRmEventHub удаляет и удаляет указанный концентратор событий из заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="00227-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="00227-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00227-107">EXAMPLES</span></span>

### <span data-ttu-id="00227-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00227-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="00227-109">Удаляет MyEventHubName концентратора \` событий \` .</span><span class="sxs-lookup"><span data-stu-id="00227-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="00227-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00227-110">PARAMETERS</span></span>

### <span data-ttu-id="00227-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00227-111">-DefaultProfile</span></span>
<span data-ttu-id="00227-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00227-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00227-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00227-113">-Name</span></span>
<span data-ttu-id="00227-114">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="00227-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00227-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="00227-115">-Namespace</span></span>
<span data-ttu-id="00227-116">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="00227-116">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00227-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00227-117">-ResourceGroupName</span></span>
<span data-ttu-id="00227-118">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="00227-118">Resource Group Name</span></span>

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

### <span data-ttu-id="00227-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00227-119">-Confirm</span></span>
<span data-ttu-id="00227-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="00227-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00227-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00227-121">-WhatIf</span></span>
<span data-ttu-id="00227-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="00227-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00227-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="00227-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00227-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00227-124">CommonParameters</span></span>
<span data-ttu-id="00227-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00227-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="00227-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00227-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00227-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00227-127">INPUTS</span></span>

### <span data-ttu-id="00227-128">System. String</span><span class="sxs-lookup"><span data-stu-id="00227-128">System.String</span></span>


## <span data-ttu-id="00227-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00227-129">OUTPUTS</span></span>

### <span data-ttu-id="00227-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="00227-130">System.Object</span></span>

## <span data-ttu-id="00227-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="00227-131">NOTES</span></span>

## <span data-ttu-id="00227-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00227-132">RELATED LINKS</span></span>
