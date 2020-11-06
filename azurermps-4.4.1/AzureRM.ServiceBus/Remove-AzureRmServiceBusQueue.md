---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8c5c614a041ff0e4ab9bc4fdc0aea944901d1efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562155"
---
# <span data-ttu-id="06616-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="06616-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="06616-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="06616-102">SYNOPSIS</span></span>
<span data-ttu-id="06616-103">Удаляет очередь из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="06616-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06616-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="06616-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06616-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06616-105">DESCRIPTION</span></span>
<span data-ttu-id="06616-106">Командлет **Remove-AzureRmServiceBusQueue** Удаляет очередь из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="06616-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="06616-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="06616-107">EXAMPLES</span></span>

### <span data-ttu-id="06616-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="06616-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="06616-109">Удаляет очередь `SB-Queue_exampl1` из пространства имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="06616-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="06616-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="06616-110">PARAMETERS</span></span>

### <span data-ttu-id="06616-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06616-111">-Confirm</span></span>
<span data-ttu-id="06616-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="06616-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06616-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06616-113">-WhatIf</span></span>
<span data-ttu-id="06616-114">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="06616-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06616-115">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="06616-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06616-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06616-116">-DefaultProfile</span></span>
<span data-ttu-id="06616-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06616-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06616-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="06616-118">-Name</span></span>
<span data-ttu-id="06616-119">Имя очереди.</span><span class="sxs-lookup"><span data-stu-id="06616-119">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06616-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="06616-120">-Namespace</span></span>
<span data-ttu-id="06616-121">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="06616-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06616-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06616-122">-ResourceGroupName</span></span>
<span data-ttu-id="06616-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06616-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06616-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06616-124">CommonParameters</span></span>
<span data-ttu-id="06616-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="06616-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06616-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06616-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06616-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="06616-127">INPUTS</span></span>

### <span data-ttu-id="06616-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06616-128">-ResourceGroup</span></span>
 <span data-ttu-id="06616-129">System. String</span><span class="sxs-lookup"><span data-stu-id="06616-129">System.String</span></span>

### <span data-ttu-id="06616-130">-+ +</span><span class="sxs-lookup"><span data-stu-id="06616-130">-NamespaceName</span></span>
 <span data-ttu-id="06616-131">System. String</span><span class="sxs-lookup"><span data-stu-id="06616-131">System.String</span></span>

### <span data-ttu-id="06616-132">-QueueName</span><span class="sxs-lookup"><span data-stu-id="06616-132">-QueueName</span></span>
 <span data-ttu-id="06616-133">System. String</span><span class="sxs-lookup"><span data-stu-id="06616-133">System.String</span></span>

## <span data-ttu-id="06616-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="06616-134">OUTPUTS</span></span>

### <span data-ttu-id="06616-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="06616-135">System.Object</span></span>

## <span data-ttu-id="06616-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="06616-136">NOTES</span></span>

## <span data-ttu-id="06616-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06616-137">RELATED LINKS</span></span>

