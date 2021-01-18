---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: c93f0d8a44a67195d2c901dd581505276b7ae2f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517385"
---
# <span data-ttu-id="6403b-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="6403b-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="6403b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6403b-102">SYNOPSIS</span></span>
<span data-ttu-id="6403b-103">Удаляет очередь из указанного пространства имен автобусов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="6403b-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6403b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6403b-104">SYNTAX</span></span>

### <span data-ttu-id="6403b-105">QueuePropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6403b-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6403b-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6403b-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6403b-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6403b-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6403b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6403b-108">DESCRIPTION</span></span>
<span data-ttu-id="6403b-109">Для удаления очереди из указанного пространства имен "Служни" удаляется **cmdlet Remove-AzServiceBusQueue.**</span><span class="sxs-lookup"><span data-stu-id="6403b-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6403b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6403b-110">EXAMPLES</span></span>

### <span data-ttu-id="6403b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6403b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="6403b-112">Удаляет очередь "Автобус `SB-Queue_exampl1` обслуживания" из пространства `SB-Example1` имен.</span><span class="sxs-lookup"><span data-stu-id="6403b-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="6403b-113">Пример 2. InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="6403b-113">Example 2: InputObject - Using variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="6403b-114">Удаляет очередь "Обслуживание" в параметре $inputobject -InputObject.</span><span class="sxs-lookup"><span data-stu-id="6403b-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="6403b-115">Пример 3. InputObject — использование piping:</span><span class="sxs-lookup"><span data-stu-id="6403b-115">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="6403b-116">Пример 4. ResourceId — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="6403b-116">Example 4: ResourceId - Using variable:</span></span>
```powershell
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="6403b-117">Удаляет очередь "Автобус обслуживания", предоставленную в ARM в параметре $resourceid/string для -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6403b-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="6403b-118">Пример 5. ResourceId — передача в качестве строки:</span><span class="sxs-lookup"><span data-stu-id="6403b-118">Example 5: ResourceId - passing as string:</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="6403b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6403b-119">PARAMETERS</span></span>

### <span data-ttu-id="6403b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6403b-120">-AsJob</span></span>
<span data-ttu-id="6403b-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6403b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6403b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6403b-122">-DefaultProfile</span></span>
<span data-ttu-id="6403b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6403b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6403b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6403b-124">-InputObject</span></span>
<span data-ttu-id="6403b-125">Объект очереди "Автобусы обслуживания"</span><span class="sxs-lookup"><span data-stu-id="6403b-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="6403b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6403b-126">-Name</span></span>
<span data-ttu-id="6403b-127">Имя очереди</span><span class="sxs-lookup"><span data-stu-id="6403b-127">Queue Name</span></span>

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

### <span data-ttu-id="6403b-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6403b-128">-Namespace</span></span>
<span data-ttu-id="6403b-129">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="6403b-129">Namespace Name</span></span>

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

### <span data-ttu-id="6403b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6403b-130">-PassThru</span></span>
<span data-ttu-id="6403b-131">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="6403b-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6403b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6403b-132">-ResourceGroupName</span></span>
<span data-ttu-id="6403b-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6403b-133">The name of the resource group</span></span>

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

### <span data-ttu-id="6403b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6403b-134">-ResourceId</span></span>
<span data-ttu-id="6403b-135">Service Bus Queue Resource Id</span><span class="sxs-lookup"><span data-stu-id="6403b-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="6403b-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6403b-136">-Confirm</span></span>
<span data-ttu-id="6403b-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6403b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6403b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6403b-138">-WhatIf</span></span>
<span data-ttu-id="6403b-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6403b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6403b-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6403b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6403b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6403b-141">CommonParameters</span></span>
<span data-ttu-id="6403b-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6403b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6403b-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6403b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6403b-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6403b-144">INPUTS</span></span>

### <span data-ttu-id="6403b-145">System.String</span><span class="sxs-lookup"><span data-stu-id="6403b-145">System.String</span></span>

### <span data-ttu-id="6403b-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="6403b-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="6403b-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6403b-147">OUTPUTS</span></span>

### <span data-ttu-id="6403b-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6403b-148">System.Boolean</span></span>

## <span data-ttu-id="6403b-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6403b-149">NOTES</span></span>

## <span data-ttu-id="6403b-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6403b-150">RELATED LINKS</span></span>
