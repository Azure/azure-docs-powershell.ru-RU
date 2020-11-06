---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 28c6bf4d463331755121e8a1ea14bf7f93407017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566108"
---
# <span data-ttu-id="5fb17-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="5fb17-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="5fb17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5fb17-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb17-103">Удаляет очередь из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="5fb17-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fb17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5fb17-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fb17-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fb17-105">DESCRIPTION</span></span>
<span data-ttu-id="5fb17-106">Командлет **Remove-AzureRmServiceBusQueue** Удаляет очередь из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="5fb17-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="5fb17-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5fb17-107">EXAMPLES</span></span>

### <span data-ttu-id="5fb17-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5fb17-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="5fb17-109">Удаляет очередь `SB-Queue_exampl1` из пространства имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="5fb17-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="5fb17-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5fb17-110">PARAMETERS</span></span>

### <span data-ttu-id="5fb17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb17-111">-DefaultProfile</span></span>
<span data-ttu-id="5fb17-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5fb17-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fb17-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5fb17-113">-Name</span></span>
<span data-ttu-id="5fb17-114">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="5fb17-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb17-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5fb17-115">-Namespace</span></span>
<span data-ttu-id="5fb17-116">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="5fb17-116">Namespace Name.</span></span>

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

### <span data-ttu-id="5fb17-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb17-117">-ResourceGroupName</span></span>
<span data-ttu-id="5fb17-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5fb17-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb17-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fb17-119">-Confirm</span></span>
<span data-ttu-id="5fb17-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5fb17-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fb17-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fb17-121">-WhatIf</span></span>
<span data-ttu-id="5fb17-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5fb17-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fb17-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5fb17-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fb17-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb17-124">CommonParameters</span></span>
<span data-ttu-id="5fb17-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5fb17-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb17-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb17-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb17-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5fb17-127">INPUTS</span></span>

### <span data-ttu-id="5fb17-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5fb17-128">-ResourceGroup</span></span>
 <span data-ttu-id="5fb17-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5fb17-129">System.String</span></span>

### <span data-ttu-id="5fb17-130">-+ +</span><span class="sxs-lookup"><span data-stu-id="5fb17-130">-NamespaceName</span></span>
 <span data-ttu-id="5fb17-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5fb17-131">System.String</span></span>

### <span data-ttu-id="5fb17-132">-QueueName</span><span class="sxs-lookup"><span data-stu-id="5fb17-132">-QueueName</span></span>
 <span data-ttu-id="5fb17-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5fb17-133">System.String</span></span>

## <span data-ttu-id="5fb17-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fb17-134">OUTPUTS</span></span>

### <span data-ttu-id="5fb17-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="5fb17-135">System.Object</span></span>

## <span data-ttu-id="5fb17-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="5fb17-136">NOTES</span></span>

## <span data-ttu-id="5fb17-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fb17-137">RELATED LINKS</span></span>

