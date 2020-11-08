---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: b10aad8cdf480dd567b0646fb3befa95fb32bf72
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236093"
---
# <span data-ttu-id="2b852-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="2b852-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="2b852-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b852-102">SYNOPSIS</span></span>
<span data-ttu-id="2b852-103">Создает новую или обновляет существующую группу действий.</span><span class="sxs-lookup"><span data-stu-id="2b852-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="2b852-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b852-104">SYNTAX</span></span>

### <span data-ttu-id="2b852-105">ByPropertyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b852-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b852-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b852-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b852-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2b852-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b852-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b852-108">DESCRIPTION</span></span>
<span data-ttu-id="2b852-109">Командлет **Set-AzActionGroup** создает новый или обновляет существующую группу действий</span><span class="sxs-lookup"><span data-stu-id="2b852-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="2b852-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b852-110">EXAMPLES</span></span>

### <span data-ttu-id="2b852-111">Пример 1: создание группы действий</span><span class="sxs-lookup"><span data-stu-id="2b852-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="2b852-112">Первые две команды создают два получателя.</span><span class="sxs-lookup"><span data-stu-id="2b852-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="2b852-113">В последней команде создается группа действий, в том числе два получателя.</span><span class="sxs-lookup"><span data-stu-id="2b852-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="2b852-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b852-114">PARAMETERS</span></span>

### <span data-ttu-id="2b852-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b852-115">-DefaultProfile</span></span>
<span data-ttu-id="2b852-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2b852-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b852-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="2b852-117">-DisableGroup</span></span>
<span data-ttu-id="2b852-118">Отключение группы действий.</span><span class="sxs-lookup"><span data-stu-id="2b852-118">Disables the action group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b852-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b852-119">-InputObject</span></span>
<span data-ttu-id="2b852-120">Ресурс группы действий</span><span class="sxs-lookup"><span data-stu-id="2b852-120">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b852-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2b852-121">-Name</span></span>
<span data-ttu-id="2b852-122">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="2b852-122">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b852-123">-Получатель</span><span class="sxs-lookup"><span data-stu-id="2b852-123">-Receiver</span></span>
<span data-ttu-id="2b852-124">Список получателей группы действий.</span><span class="sxs-lookup"><span data-stu-id="2b852-124">The list of receivers of the action group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b852-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b852-125">-ResourceGroupName</span></span>
<span data-ttu-id="2b852-126">"Группа ресурсов"</span><span class="sxs-lookup"><span data-stu-id="2b852-126">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b852-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b852-127">-ResourceId</span></span>
<span data-ttu-id="2b852-128">Ресурс</span><span class="sxs-lookup"><span data-stu-id="2b852-128">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b852-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="2b852-129">-ShortName</span></span>
<span data-ttu-id="2b852-130">Краткое имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="2b852-130">The short name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b852-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="2b852-131">-Tag</span></span>
<span data-ttu-id="2b852-132">Теги ресурса группы действий</span><span class="sxs-lookup"><span data-stu-id="2b852-132">The tags of the action group resource</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b852-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b852-133">-Confirm</span></span>
<span data-ttu-id="2b852-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2b852-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b852-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b852-135">-WhatIf</span></span>
<span data-ttu-id="2b852-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2b852-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2b852-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2b852-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b852-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b852-138">CommonParameters</span></span>
<span data-ttu-id="2b852-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b852-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b852-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b852-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b852-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b852-141">INPUTS</span></span>

### <span data-ttu-id="2b852-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2b852-142">System.String</span></span>

### <span data-ttu-id="2b852-143">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. PowerShell. командлеты. Monitor, версия = 1.0.0.0, культура = независимая, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="2b852-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2b852-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2b852-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="2b852-145">System. Collections. Generic. IDictionary "2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2b852-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2b852-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="2b852-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="2b852-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b852-147">OUTPUTS</span></span>

### <span data-ttu-id="2b852-148">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="2b852-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="2b852-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b852-149">NOTES</span></span>

## <span data-ttu-id="2b852-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b852-150">RELATED LINKS</span></span>

<span data-ttu-id="2b852-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="2b852-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
