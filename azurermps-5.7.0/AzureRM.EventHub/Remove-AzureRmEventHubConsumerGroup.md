---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 5b88ce6edc92cb6483b8d6df95599fcea854f805
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564936"
---
# <span data-ttu-id="8756b-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="8756b-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="8756b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8756b-102">SYNOPSIS</span></span>
<span data-ttu-id="8756b-103">Удаляет указанную группу потребителей концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="8756b-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8756b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8756b-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8756b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8756b-105">DESCRIPTION</span></span>
<span data-ttu-id="8756b-106">Командлет Remove-AzureRmEventHubConsumerGroup удаляет указанную группу потребителей из заданного концентратора событий и удаляет ее.</span><span class="sxs-lookup"><span data-stu-id="8756b-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="8756b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8756b-107">EXAMPLES</span></span>

### <span data-ttu-id="8756b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8756b-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="8756b-109">Удаляет группу потребителей \` MyConsumerGroupName \` из MyEventHubName концентратора событий \` с \` областью в \` \` пространство имен MyNamespaceName.</span><span class="sxs-lookup"><span data-stu-id="8756b-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="8756b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8756b-110">PARAMETERS</span></span>

### <span data-ttu-id="8756b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8756b-111">-DefaultProfile</span></span>
<span data-ttu-id="8756b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8756b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8756b-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="8756b-113">-EventHub</span></span>
<span data-ttu-id="8756b-114">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="8756b-114">EventHub Name</span></span>

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

### <span data-ttu-id="8756b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8756b-115">-Name</span></span>
<span data-ttu-id="8756b-116">Имя ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="8756b-116">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8756b-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8756b-117">-Namespace</span></span>
<span data-ttu-id="8756b-118">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="8756b-118">Namespace Name</span></span>

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

### <span data-ttu-id="8756b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8756b-119">-ResourceGroupName</span></span>
<span data-ttu-id="8756b-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8756b-120">Resource Group Name</span></span>

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

### <span data-ttu-id="8756b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8756b-121">-Confirm</span></span>
<span data-ttu-id="8756b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8756b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8756b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8756b-123">-WhatIf</span></span>
<span data-ttu-id="8756b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8756b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8756b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8756b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8756b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8756b-126">CommonParameters</span></span>
<span data-ttu-id="8756b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8756b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8756b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8756b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8756b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8756b-129">INPUTS</span></span>

### <span data-ttu-id="8756b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8756b-130">System.String</span></span>


## <span data-ttu-id="8756b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8756b-131">OUTPUTS</span></span>

### <span data-ttu-id="8756b-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="8756b-132">System.Object</span></span>

## <span data-ttu-id="8756b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8756b-133">NOTES</span></span>

## <span data-ttu-id="8756b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8756b-134">RELATED LINKS</span></span>
