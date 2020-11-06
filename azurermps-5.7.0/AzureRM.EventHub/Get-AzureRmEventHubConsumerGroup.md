---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 445d20453b9f3d99e4ff5c72e118b287f0a83898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567998"
---
# <span data-ttu-id="aed35-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="aed35-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="aed35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aed35-102">SYNOPSIS</span></span>
<span data-ttu-id="aed35-103">Получает сведения о группе потребителей указанных концентраторов событий или получает список групп потребителей в концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="aed35-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aed35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aed35-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aed35-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aed35-105">DESCRIPTION</span></span>
<span data-ttu-id="aed35-106">Командлет Get-AzureRmEventHubConsumerGroup возвращает либо сведения о указанной группе потребителей для концентратора событий, либо список групп потребителей в заданном концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="aed35-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="aed35-107">Если указано имя группы потребителей, возвращаются сведения о одной группе потребителей.</span><span class="sxs-lookup"><span data-stu-id="aed35-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="aed35-108">Если имя группы потребителей не задано, возвращается список групп потребителей в указанном концентраторе событий.</span><span class="sxs-lookup"><span data-stu-id="aed35-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="aed35-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aed35-109">EXAMPLES</span></span>

### <span data-ttu-id="aed35-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aed35-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="aed35-111">Получает группу потребителей \` MyConsumerGroupName \` в центре событий \` MyEventHubName \` , который существует в пространстве имен \` MyNamespaceName \` с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="aed35-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="aed35-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="aed35-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="aed35-113">Получает список групп потребителей в центре событий \` MyEventHubName \` , который существует в пространстве имен \` MyNamespaceName \` с группой ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="aed35-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="aed35-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aed35-114">PARAMETERS</span></span>

### <span data-ttu-id="aed35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aed35-115">-DefaultProfile</span></span>
<span data-ttu-id="aed35-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aed35-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aed35-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="aed35-117">-EventHub</span></span>
<span data-ttu-id="aed35-118">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="aed35-118">EventHub Name</span></span>

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

### <span data-ttu-id="aed35-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aed35-119">-Name</span></span>
<span data-ttu-id="aed35-120">Имя ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="aed35-120">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aed35-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="aed35-121">-Namespace</span></span>
<span data-ttu-id="aed35-122">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="aed35-122">Namespace Name</span></span>

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

### <span data-ttu-id="aed35-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aed35-123">-ResourceGroupName</span></span>
<span data-ttu-id="aed35-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="aed35-124">Resource Group Name</span></span>

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

### <span data-ttu-id="aed35-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aed35-125">CommonParameters</span></span>
<span data-ttu-id="aed35-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aed35-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="aed35-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aed35-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aed35-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aed35-128">INPUTS</span></span>

### <span data-ttu-id="aed35-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aed35-129">System.String</span></span>


## <span data-ttu-id="aed35-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aed35-130">OUTPUTS</span></span>

### <span data-ttu-id="aed35-131">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. eventhub, версия = 0.5.0.0, культура = нейтраль, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="aed35-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="aed35-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="aed35-132">NOTES</span></span>

## <span data-ttu-id="aed35-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aed35-133">RELATED LINKS</span></span>
