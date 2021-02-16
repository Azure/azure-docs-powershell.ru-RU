---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: b10aad8cdf480dd567b0646fb3befa95fb32bf72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226241"
---
# <span data-ttu-id="87406-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="87406-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="87406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87406-102">SYNOPSIS</span></span>
<span data-ttu-id="87406-103">Создает новую или обновляет существующую группу действий.</span><span class="sxs-lookup"><span data-stu-id="87406-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="87406-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="87406-104">SYNTAX</span></span>

### <span data-ttu-id="87406-105">ByPropertyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87406-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87406-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="87406-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87406-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="87406-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87406-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87406-108">DESCRIPTION</span></span>
<span data-ttu-id="87406-109">Для создания или обновления существующей группы действий будет создан новый или обновленный **cmdlet Set-AzActionGroup**</span><span class="sxs-lookup"><span data-stu-id="87406-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="87406-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="87406-110">EXAMPLES</span></span>

### <span data-ttu-id="87406-111">Пример 1. Создание группы действий</span><span class="sxs-lookup"><span data-stu-id="87406-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="87406-112">В первых двух командах создаются два приемника.</span><span class="sxs-lookup"><span data-stu-id="87406-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="87406-113">Конечная команда создает группу действий с двумя приемниками.</span><span class="sxs-lookup"><span data-stu-id="87406-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="87406-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87406-114">PARAMETERS</span></span>

### <span data-ttu-id="87406-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87406-115">-DefaultProfile</span></span>
<span data-ttu-id="87406-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="87406-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87406-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="87406-117">-DisableGroup</span></span>
<span data-ttu-id="87406-118">Отключает группу действий.</span><span class="sxs-lookup"><span data-stu-id="87406-118">Disables the action group.</span></span>

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

### <span data-ttu-id="87406-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87406-119">-InputObject</span></span>
<span data-ttu-id="87406-120">Ресурс группы действий</span><span class="sxs-lookup"><span data-stu-id="87406-120">The action group resource</span></span>

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

### <span data-ttu-id="87406-121">-Name</span><span class="sxs-lookup"><span data-stu-id="87406-121">-Name</span></span>
<span data-ttu-id="87406-122">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="87406-122">The name of the action group.</span></span>

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

### <span data-ttu-id="87406-123">-Receiver</span><span class="sxs-lookup"><span data-stu-id="87406-123">-Receiver</span></span>
<span data-ttu-id="87406-124">Список приемников группы действий.</span><span class="sxs-lookup"><span data-stu-id="87406-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="87406-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87406-125">-ResourceGroupName</span></span>
<span data-ttu-id="87406-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="87406-126">The resource group nam</span></span>

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

### <span data-ttu-id="87406-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87406-127">-ResourceId</span></span>
<span data-ttu-id="87406-128">Ресурс i</span><span class="sxs-lookup"><span data-stu-id="87406-128">The resource i</span></span>

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

### <span data-ttu-id="87406-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="87406-129">-ShortName</span></span>
<span data-ttu-id="87406-130">Краткое имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="87406-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="87406-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="87406-131">-Tag</span></span>
<span data-ttu-id="87406-132">Теги ресурса группы действий</span><span class="sxs-lookup"><span data-stu-id="87406-132">The tags of the action group resource</span></span>

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

### <span data-ttu-id="87406-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87406-133">-Confirm</span></span>
<span data-ttu-id="87406-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="87406-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87406-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87406-135">-WhatIf</span></span>
<span data-ttu-id="87406-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87406-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87406-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="87406-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87406-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87406-138">CommonParameters</span></span>
<span data-ttu-id="87406-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87406-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87406-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87406-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87406-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="87406-141">INPUTS</span></span>

### <span data-ttu-id="87406-142">System.String</span><span class="sxs-lookup"><span data-stu-id="87406-142">System.String</span></span>

### <span data-ttu-id="87406-143">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="87406-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="87406-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87406-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="87406-145">System.Collections.Generic.IDictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="87406-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="87406-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="87406-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="87406-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87406-147">OUTPUTS</span></span>

### <span data-ttu-id="87406-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="87406-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="87406-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="87406-149">NOTES</span></span>

## <span data-ttu-id="87406-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87406-150">RELATED LINKS</span></span>

<span data-ttu-id="87406-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="87406-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
