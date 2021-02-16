---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 75da2231dae7ea0dc587d48ca832b7631fc24986
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235673"
---
# <span data-ttu-id="3ade4-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="3ade4-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="3ade4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ade4-102">SYNOPSIS</span></span>
<span data-ttu-id="3ade4-103">Удаляет тему из указанного пространства имен автобусов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="3ade4-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="3ade4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3ade4-104">SYNTAX</span></span>

### <span data-ttu-id="3ade4-105">Набор свойств темы (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ade4-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ade4-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3ade4-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ade4-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3ade4-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ade4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ade4-108">DESCRIPTION</span></span>
<span data-ttu-id="3ade4-109">Для удаления темы из указанного пространства имен служинного автобусы будет удаляется ее из области имен **AzServiceBusTopic.**</span><span class="sxs-lookup"><span data-stu-id="3ade4-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="3ade4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3ade4-110">EXAMPLES</span></span>

### <span data-ttu-id="3ade4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ade4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="3ade4-112">Удаляет тему `SB-Topic_exampl1` из пространства `SB-Example1` имен.</span><span class="sxs-lookup"><span data-stu-id="3ade4-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="3ade4-113">Пример 2. InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="3ade4-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="3ade4-114">Пример 3. InputObject — использование piping:</span><span class="sxs-lookup"><span data-stu-id="3ade4-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="3ade4-115">Пример 4. ResourceId с переменной:</span><span class="sxs-lookup"><span data-stu-id="3ade4-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="3ade4-116">Пример 5. ResourceId с строкой</span><span class="sxs-lookup"><span data-stu-id="3ade4-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="3ade4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ade4-117">PARAMETERS</span></span>

### <span data-ttu-id="3ade4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ade4-118">-AsJob</span></span>
<span data-ttu-id="3ade4-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3ade4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ade4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ade4-120">-DefaultProfile</span></span>
<span data-ttu-id="3ade4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ade4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ade4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ade4-122">-InputObject</span></span>
<span data-ttu-id="3ade4-123">Service Bus Topic Object</span><span class="sxs-lookup"><span data-stu-id="3ade4-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="3ade4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3ade4-124">-Name</span></span>
<span data-ttu-id="3ade4-125">Название темы</span><span class="sxs-lookup"><span data-stu-id="3ade4-125">Topic Name</span></span>

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

### <span data-ttu-id="3ade4-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3ade4-126">-Namespace</span></span>
<span data-ttu-id="3ade4-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="3ade4-127">Namespace Name</span></span>

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

### <span data-ttu-id="3ade4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ade4-128">-PassThru</span></span>
<span data-ttu-id="3ade4-129">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="3ade4-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3ade4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ade4-130">-ResourceGroupName</span></span>
<span data-ttu-id="3ade4-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3ade4-131">The name of the resource group</span></span>

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

### <span data-ttu-id="3ade4-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ade4-132">-ResourceId</span></span>
<span data-ttu-id="3ade4-133">Service Bus Topic Resource Id</span><span class="sxs-lookup"><span data-stu-id="3ade4-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="3ade4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ade4-134">-Confirm</span></span>
<span data-ttu-id="3ade4-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ade4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ade4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ade4-136">-WhatIf</span></span>
<span data-ttu-id="3ade4-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ade4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ade4-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3ade4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ade4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ade4-139">CommonParameters</span></span>
<span data-ttu-id="3ade4-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ade4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ade4-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ade4-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ade4-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ade4-142">INPUTS</span></span>

### <span data-ttu-id="3ade4-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3ade4-143">System.String</span></span>

### <span data-ttu-id="3ade4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="3ade4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="3ade4-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3ade4-145">OUTPUTS</span></span>

### <span data-ttu-id="3ade4-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3ade4-146">System.Boolean</span></span>

## <span data-ttu-id="3ade4-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3ade4-147">NOTES</span></span>

## <span data-ttu-id="3ade4-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ade4-148">RELATED LINKS</span></span>
