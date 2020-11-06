---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 743928771fdba7ed17fe2643cf9e92ae7c2d9860
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557360"
---
# <span data-ttu-id="ba495-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ba495-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="ba495-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba495-102">SYNOPSIS</span></span>
<span data-ttu-id="ba495-103">Обновляет указанную группу потребителей концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="ba495-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba495-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba495-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba495-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba495-105">DESCRIPTION</span></span>
<span data-ttu-id="ba495-106">Командлет Set-AzureRmEventHubConsumerGroup обновляет указанную группу потребителей концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="ba495-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="ba495-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba495-107">EXAMPLES</span></span>

### <span data-ttu-id="ba495-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ba495-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="ba495-109">Задает пользовательские метаданные группы потребителей \` MyConsumerGroupName \` для "тестирование".</span><span class="sxs-lookup"><span data-stu-id="ba495-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="ba495-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba495-110">PARAMETERS</span></span>

### <span data-ttu-id="ba495-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba495-111">-DefaultProfile</span></span>
<span data-ttu-id="ba495-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba495-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba495-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ba495-113">-EventHub</span></span>
<span data-ttu-id="ba495-114">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="ba495-114">EventHub Name</span></span>

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

### <span data-ttu-id="ba495-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba495-115">-Name</span></span>
<span data-ttu-id="ba495-116">Имя ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ba495-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="ba495-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ba495-117">-Namespace</span></span>
<span data-ttu-id="ba495-118">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="ba495-118">Namespace Name</span></span>

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

### <span data-ttu-id="ba495-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba495-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba495-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ba495-120">Resource Group Name</span></span>

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

### <span data-ttu-id="ba495-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="ba495-121">-UserMetadata</span></span>
<span data-ttu-id="ba495-122">Метаданные пользователей для ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="ba495-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba495-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba495-123">-Confirm</span></span>
<span data-ttu-id="ba495-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba495-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba495-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba495-125">-WhatIf</span></span>
<span data-ttu-id="ba495-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba495-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba495-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba495-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba495-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba495-128">CommonParameters</span></span>
<span data-ttu-id="ba495-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba495-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ba495-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba495-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba495-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba495-131">INPUTS</span></span>

### <span data-ttu-id="ba495-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ba495-132">System.String</span></span>


## <span data-ttu-id="ba495-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba495-133">OUTPUTS</span></span>

### <span data-ttu-id="ba495-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="ba495-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="ba495-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba495-135">NOTES</span></span>

## <span data-ttu-id="ba495-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba495-136">RELATED LINKS</span></span>
