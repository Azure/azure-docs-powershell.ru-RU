---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406492"
---
# <span data-ttu-id="1f09b-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1f09b-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="1f09b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f09b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f09b-103">Обновляет указанную группу "Концентраторы событий".</span><span class="sxs-lookup"><span data-stu-id="1f09b-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="1f09b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1f09b-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f09b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f09b-105">DESCRIPTION</span></span>
<span data-ttu-id="1f09b-106">Этот Set-AzEventHubConsumerGroup обновляет указанную группу "Концентраторы событий".</span><span class="sxs-lookup"><span data-stu-id="1f09b-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="1f09b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1f09b-107">EXAMPLES</span></span>

### <span data-ttu-id="1f09b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f09b-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="1f09b-109">Устанавливает для метаданных пользователя группы \` пользователей MyConsumerGroupName \` "Тестирование".</span><span class="sxs-lookup"><span data-stu-id="1f09b-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="1f09b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f09b-110">PARAMETERS</span></span>

### <span data-ttu-id="1f09b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f09b-111">-DefaultProfile</span></span>
<span data-ttu-id="1f09b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f09b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f09b-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="1f09b-113">-EventHub</span></span>
<span data-ttu-id="1f09b-114">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="1f09b-114">EventHub Name</span></span>

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

### <span data-ttu-id="1f09b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1f09b-115">-Name</span></span>
<span data-ttu-id="1f09b-116">Имя группы потребителей</span><span class="sxs-lookup"><span data-stu-id="1f09b-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="1f09b-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1f09b-117">-Namespace</span></span>
<span data-ttu-id="1f09b-118">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="1f09b-118">Namespace Name</span></span>

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

### <span data-ttu-id="1f09b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f09b-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f09b-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1f09b-120">Resource Group Name</span></span>

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

### <span data-ttu-id="1f09b-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="1f09b-121">-UserMetadata</span></span>
<span data-ttu-id="1f09b-122">Метаданные пользователя для ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="1f09b-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="1f09b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f09b-123">-Confirm</span></span>
<span data-ttu-id="1f09b-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f09b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f09b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f09b-125">-WhatIf</span></span>
<span data-ttu-id="1f09b-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f09b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f09b-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1f09b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f09b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f09b-128">CommonParameters</span></span>
<span data-ttu-id="1f09b-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f09b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f09b-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f09b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f09b-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f09b-131">INPUTS</span></span>

### <span data-ttu-id="1f09b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1f09b-132">System.String</span></span>

## <span data-ttu-id="1f09b-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f09b-133">OUTPUTS</span></span>

### <span data-ttu-id="1f09b-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="1f09b-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="1f09b-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1f09b-135">NOTES</span></span>

## <span data-ttu-id="1f09b-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f09b-136">RELATED LINKS</span></span>