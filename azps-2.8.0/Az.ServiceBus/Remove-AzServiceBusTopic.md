---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 27d35f0c5b0e947624827d01d1182a09912cb9fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905342"
---
# <span data-ttu-id="f4291-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="f4291-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="f4291-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4291-102">SYNOPSIS</span></span>
<span data-ttu-id="f4291-103">Удаляет раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="f4291-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f4291-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4291-104">SYNTAX</span></span>

### <span data-ttu-id="f4291-105">TopicPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4291-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4291-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f4291-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4291-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f4291-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4291-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4291-108">DESCRIPTION</span></span>
<span data-ttu-id="f4291-109">Командлет **Remove-AzServiceBusTopic** удаляет раздел из указанного пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="f4291-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f4291-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4291-110">EXAMPLES</span></span>

### <span data-ttu-id="f4291-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4291-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="f4291-112">Удаляет раздел `SB-Topic_exampl1` из пространства имен `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="f4291-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="f4291-113">Пример 2,1-InputObject: использование переменной</span><span class="sxs-lookup"><span data-stu-id="f4291-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="f4291-114">Пример 2,2-InputObject-использование конвейера:</span><span class="sxs-lookup"><span data-stu-id="f4291-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="f4291-115">Пример 3,1-ResourceId с использованием переменной:</span><span class="sxs-lookup"><span data-stu-id="f4291-115">Example 3.1 - ResourceId Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="f4291-116">Пример 3,2-ResourceId с использованием строкового значения</span><span class="sxs-lookup"><span data-stu-id="f4291-116">Example 3.2 - ResourceId Using String value</span></span>
```
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="f4291-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4291-117">PARAMETERS</span></span>

### <span data-ttu-id="f4291-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4291-118">-AsJob</span></span>
<span data-ttu-id="f4291-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f4291-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4291-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4291-120">-DefaultProfile</span></span>
<span data-ttu-id="f4291-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4291-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4291-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4291-122">-InputObject</span></span>
<span data-ttu-id="f4291-123">Объект темы служебной шины</span><span class="sxs-lookup"><span data-stu-id="f4291-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="f4291-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4291-124">-Name</span></span>
<span data-ttu-id="f4291-125">Название раздела</span><span class="sxs-lookup"><span data-stu-id="f4291-125">Topic Name</span></span>

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

### <span data-ttu-id="f4291-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f4291-126">-Namespace</span></span>
<span data-ttu-id="f4291-127">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="f4291-127">Namespace Name</span></span>

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

### <span data-ttu-id="f4291-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4291-128">-PassThru</span></span>
<span data-ttu-id="f4291-129">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f4291-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f4291-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4291-130">-ResourceGroupName</span></span>
<span data-ttu-id="f4291-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4291-131">The name of the resource group</span></span>

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

### <span data-ttu-id="f4291-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4291-132">-ResourceId</span></span>
<span data-ttu-id="f4291-133">Идентификатор ресурса для темы служебной шины</span><span class="sxs-lookup"><span data-stu-id="f4291-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="f4291-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4291-134">-Confirm</span></span>
<span data-ttu-id="f4291-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4291-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4291-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4291-136">-WhatIf</span></span>
<span data-ttu-id="f4291-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4291-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4291-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4291-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4291-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4291-139">CommonParameters</span></span>
<span data-ttu-id="f4291-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4291-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4291-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4291-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4291-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4291-142">INPUTS</span></span>

### <span data-ttu-id="f4291-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f4291-143">System.String</span></span>

### <span data-ttu-id="f4291-144">Microsoft. Azure. Commands. ServiceBus. Models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="f4291-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="f4291-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4291-145">OUTPUTS</span></span>

### <span data-ttu-id="f4291-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4291-146">System.Boolean</span></span>

## <span data-ttu-id="f4291-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4291-147">NOTES</span></span>

## <span data-ttu-id="f4291-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4291-148">RELATED LINKS</span></span>
