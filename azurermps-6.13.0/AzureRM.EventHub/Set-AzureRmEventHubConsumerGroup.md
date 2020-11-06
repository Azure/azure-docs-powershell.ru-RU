---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 52038de3d0bb8f07fdfe5abf0978e306a1959a94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564540"
---
# <span data-ttu-id="79855-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="79855-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="79855-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79855-102">SYNOPSIS</span></span>
<span data-ttu-id="79855-103">Обновляет указанную группу потребителей концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="79855-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79855-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79855-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79855-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79855-105">DESCRIPTION</span></span>
<span data-ttu-id="79855-106">Командлет Set-AzureRmEventHubConsumerGroup обновляет указанную группу потребителей концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="79855-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="79855-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79855-107">EXAMPLES</span></span>

### <span data-ttu-id="79855-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="79855-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="79855-109">Задает пользовательские метаданные группы потребителей \` MyConsumerGroupName \` для "тестирование".</span><span class="sxs-lookup"><span data-stu-id="79855-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="79855-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79855-110">PARAMETERS</span></span>

### <span data-ttu-id="79855-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79855-111">-DefaultProfile</span></span>
<span data-ttu-id="79855-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79855-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79855-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="79855-113">-EventHub</span></span>
<span data-ttu-id="79855-114">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="79855-114">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79855-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="79855-115">-Name</span></span>
<span data-ttu-id="79855-116">Имя ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="79855-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79855-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="79855-117">-Namespace</span></span>
<span data-ttu-id="79855-118">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="79855-118">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79855-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79855-119">-ResourceGroupName</span></span>
<span data-ttu-id="79855-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="79855-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79855-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="79855-121">-UserMetadata</span></span>
<span data-ttu-id="79855-122">Метаданные пользователей для ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="79855-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79855-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79855-123">-Confirm</span></span>
<span data-ttu-id="79855-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79855-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79855-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79855-125">-WhatIf</span></span>
<span data-ttu-id="79855-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79855-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79855-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79855-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79855-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79855-128">CommonParameters</span></span>
<span data-ttu-id="79855-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79855-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79855-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79855-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79855-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79855-131">INPUTS</span></span>

### <span data-ttu-id="79855-132">System. String</span><span class="sxs-lookup"><span data-stu-id="79855-132">System.String</span></span>

## <span data-ttu-id="79855-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79855-133">OUTPUTS</span></span>

### <span data-ttu-id="79855-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="79855-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="79855-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="79855-135">NOTES</span></span>

## <span data-ttu-id="79855-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79855-136">RELATED LINKS</span></span>
