---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 75da2231dae7ea0dc587d48ca832b7631fc24986
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416052"
---
# <span data-ttu-id="733db-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="733db-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="733db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="733db-102">SYNOPSIS</span></span>
<span data-ttu-id="733db-103">Удаляет тему из указанного пространства имен автобусов обслуживания.</span><span class="sxs-lookup"><span data-stu-id="733db-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="733db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="733db-104">SYNTAX</span></span>

### <span data-ttu-id="733db-105">Набор свойств темы (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="733db-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="733db-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="733db-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="733db-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="733db-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="733db-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="733db-108">DESCRIPTION</span></span>
<span data-ttu-id="733db-109">Для удаления этой темы из указанного пространства имен "Служни" удаляется ее cmdlet **AzServiceBusTopic.**</span><span class="sxs-lookup"><span data-stu-id="733db-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="733db-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="733db-110">EXAMPLES</span></span>

### <span data-ttu-id="733db-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="733db-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="733db-112">Удаляет тему `SB-Topic_exampl1` из пространства `SB-Example1` имен.</span><span class="sxs-lookup"><span data-stu-id="733db-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="733db-113">Пример 2. InputObject — использование переменной:</span><span class="sxs-lookup"><span data-stu-id="733db-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="733db-114">Пример 3. InputObject — использование piping:</span><span class="sxs-lookup"><span data-stu-id="733db-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="733db-115">Пример 4. ResourceId с переменной:</span><span class="sxs-lookup"><span data-stu-id="733db-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="733db-116">Пример 5. ResourceId с строкой</span><span class="sxs-lookup"><span data-stu-id="733db-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="733db-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="733db-117">PARAMETERS</span></span>

### <span data-ttu-id="733db-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="733db-118">-AsJob</span></span>
<span data-ttu-id="733db-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="733db-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="733db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="733db-120">-DefaultProfile</span></span>
<span data-ttu-id="733db-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="733db-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="733db-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="733db-122">-InputObject</span></span>
<span data-ttu-id="733db-123">Service Bus Topic Object</span><span class="sxs-lookup"><span data-stu-id="733db-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="733db-124">-Name</span><span class="sxs-lookup"><span data-stu-id="733db-124">-Name</span></span>
<span data-ttu-id="733db-125">Название темы</span><span class="sxs-lookup"><span data-stu-id="733db-125">Topic Name</span></span>

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

### <span data-ttu-id="733db-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="733db-126">-Namespace</span></span>
<span data-ttu-id="733db-127">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="733db-127">Namespace Name</span></span>

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

### <span data-ttu-id="733db-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="733db-128">-PassThru</span></span>
<span data-ttu-id="733db-129">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="733db-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="733db-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="733db-130">-ResourceGroupName</span></span>
<span data-ttu-id="733db-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="733db-131">The name of the resource group</span></span>

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

### <span data-ttu-id="733db-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="733db-132">-ResourceId</span></span>
<span data-ttu-id="733db-133">Service Bus Topic Resource Id</span><span class="sxs-lookup"><span data-stu-id="733db-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="733db-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="733db-134">-Confirm</span></span>
<span data-ttu-id="733db-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="733db-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="733db-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="733db-136">-WhatIf</span></span>
<span data-ttu-id="733db-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="733db-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="733db-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="733db-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="733db-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="733db-139">CommonParameters</span></span>
<span data-ttu-id="733db-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="733db-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="733db-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="733db-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="733db-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="733db-142">INPUTS</span></span>

### <span data-ttu-id="733db-143">System.String</span><span class="sxs-lookup"><span data-stu-id="733db-143">System.String</span></span>

### <span data-ttu-id="733db-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="733db-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="733db-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="733db-145">OUTPUTS</span></span>

### <span data-ttu-id="733db-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="733db-146">System.Boolean</span></span>

## <span data-ttu-id="733db-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="733db-147">NOTES</span></span>

## <span data-ttu-id="733db-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="733db-148">RELATED LINKS</span></span>
