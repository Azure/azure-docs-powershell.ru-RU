---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 75da2231dae7ea0dc587d48ca832b7631fc24986
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249614"
---
# <span data-ttu-id="62e30-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="62e30-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="62e30-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62e30-102">SYNOPSIS</span></span>
<span data-ttu-id="62e30-103">Удаляет раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="62e30-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="62e30-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62e30-104">SYNTAX</span></span>

### <span data-ttu-id="62e30-105">TopicPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62e30-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e30-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62e30-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62e30-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="62e30-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62e30-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62e30-108">DESCRIPTION</span></span>
<span data-ttu-id="62e30-109">Командлет **Remove-AzServiceBusTopic** удаляет раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="62e30-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="62e30-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62e30-110">EXAMPLES</span></span>

### <span data-ttu-id="62e30-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62e30-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="62e30-112">Удаляет раздел `SB-Topic_exampl1` из пространства имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="62e30-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="62e30-113">Пример 2: InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="62e30-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="62e30-114">Пример 3: InputObject — использование трубопроводов:</span><span class="sxs-lookup"><span data-stu-id="62e30-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="62e30-115">Пример 4: ResourceId с помощью переменной:</span><span class="sxs-lookup"><span data-stu-id="62e30-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="62e30-116">Пример 5: ResourceId с помощью строкового значения</span><span class="sxs-lookup"><span data-stu-id="62e30-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="62e30-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62e30-117">PARAMETERS</span></span>

### <span data-ttu-id="62e30-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62e30-118">-AsJob</span></span>
<span data-ttu-id="62e30-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="62e30-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62e30-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e30-120">-DefaultProfile</span></span>
<span data-ttu-id="62e30-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62e30-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62e30-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62e30-122">-InputObject</span></span>
<span data-ttu-id="62e30-123">Объект темы служебной шины</span><span class="sxs-lookup"><span data-stu-id="62e30-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62e30-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62e30-124">-Name</span></span>
<span data-ttu-id="62e30-125">Название раздела</span><span class="sxs-lookup"><span data-stu-id="62e30-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e30-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="62e30-126">-Namespace</span></span>
<span data-ttu-id="62e30-127">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="62e30-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e30-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62e30-128">-PassThru</span></span>
<span data-ttu-id="62e30-129">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="62e30-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="62e30-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e30-130">-ResourceGroupName</span></span>
<span data-ttu-id="62e30-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62e30-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e30-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62e30-132">-ResourceId</span></span>
<span data-ttu-id="62e30-133">Идентификатор ресурса для темы служебной шины</span><span class="sxs-lookup"><span data-stu-id="62e30-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62e30-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62e30-134">-Confirm</span></span>
<span data-ttu-id="62e30-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62e30-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62e30-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62e30-136">-WhatIf</span></span>
<span data-ttu-id="62e30-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62e30-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62e30-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62e30-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62e30-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e30-139">CommonParameters</span></span>
<span data-ttu-id="62e30-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62e30-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e30-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62e30-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e30-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62e30-142">INPUTS</span></span>

### <span data-ttu-id="62e30-143">System. String</span><span class="sxs-lookup"><span data-stu-id="62e30-143">System.String</span></span>

### <span data-ttu-id="62e30-144">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="62e30-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="62e30-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62e30-145">OUTPUTS</span></span>

### <span data-ttu-id="62e30-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62e30-146">System.Boolean</span></span>

## <span data-ttu-id="62e30-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="62e30-147">NOTES</span></span>

## <span data-ttu-id="62e30-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62e30-148">RELATED LINKS</span></span>