---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: c93f0d8a44a67195d2c901dd581505276b7ae2f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077612"
---
# <span data-ttu-id="df900-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="df900-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="df900-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df900-102">SYNOPSIS</span></span>
<span data-ttu-id="df900-103">Удаляет очередь из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="df900-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="df900-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df900-104">SYNTAX</span></span>

### <span data-ttu-id="df900-105">QueuePropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df900-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df900-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="df900-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df900-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="df900-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df900-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df900-108">DESCRIPTION</span></span>
<span data-ttu-id="df900-109">Командлет **Remove-AzServiceBusQueue** Удаляет очередь из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="df900-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="df900-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df900-110">EXAMPLES</span></span>

### <span data-ttu-id="df900-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df900-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="df900-112">Удаляет очередь служебной шины `SB-Queue_exampl1` из пространства имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="df900-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="df900-113">Пример 2: InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="df900-113">Example 2: InputObject - Using variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="df900-114">Удаляет очередь служебной шины, указанную в параметре $inputobject для-InputObject</span><span class="sxs-lookup"><span data-stu-id="df900-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="df900-115">Пример 3: InputObject — использование трубопроводов:</span><span class="sxs-lookup"><span data-stu-id="df900-115">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="df900-116">Пример 4: ResourceId — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="df900-116">Example 4: ResourceId - Using variable:</span></span>
```powershell
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="df900-117">Удаляет очередь служебной шины, указанную в идентификаторе ARM, в $resourceid/String для-ResourceId (параметр)</span><span class="sxs-lookup"><span data-stu-id="df900-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="df900-118">Пример 5: ИД ResourceId — передача строки:</span><span class="sxs-lookup"><span data-stu-id="df900-118">Example 5: ResourceId - passing as string:</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="df900-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df900-119">PARAMETERS</span></span>

### <span data-ttu-id="df900-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df900-120">-AsJob</span></span>
<span data-ttu-id="df900-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="df900-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df900-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df900-122">-DefaultProfile</span></span>
<span data-ttu-id="df900-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df900-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df900-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df900-124">-InputObject</span></span>
<span data-ttu-id="df900-125">Объект очереди служебной шины</span><span class="sxs-lookup"><span data-stu-id="df900-125">Service Bus Queue Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: QueueInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df900-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="df900-126">-Name</span></span>
<span data-ttu-id="df900-127">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="df900-127">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df900-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="df900-128">-Namespace</span></span>
<span data-ttu-id="df900-129">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="df900-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df900-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df900-130">-PassThru</span></span>
<span data-ttu-id="df900-131">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="df900-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="df900-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df900-132">-ResourceGroupName</span></span>
<span data-ttu-id="df900-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="df900-133">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df900-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df900-134">-ResourceId</span></span>
<span data-ttu-id="df900-135">Идентификатор ресурса очереди обслуживания служебной шины</span><span class="sxs-lookup"><span data-stu-id="df900-135">Service Bus Queue Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: QueueResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df900-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df900-136">-Confirm</span></span>
<span data-ttu-id="df900-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="df900-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df900-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df900-138">-WhatIf</span></span>
<span data-ttu-id="df900-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="df900-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df900-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="df900-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df900-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df900-141">CommonParameters</span></span>
<span data-ttu-id="df900-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df900-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df900-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df900-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df900-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df900-144">INPUTS</span></span>

### <span data-ttu-id="df900-145">System. String</span><span class="sxs-lookup"><span data-stu-id="df900-145">System.String</span></span>

### <span data-ttu-id="df900-146">Microsoft. Azure. Commands. ServiceBus. Models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="df900-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="df900-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df900-147">OUTPUTS</span></span>

### <span data-ttu-id="df900-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df900-148">System.Boolean</span></span>

## <span data-ttu-id="df900-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="df900-149">NOTES</span></span>

## <span data-ttu-id="df900-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df900-150">RELATED LINKS</span></span>
