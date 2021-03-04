---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: 6c0843afa3001299a21f49cec5ed73f74bdcd2a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955816"
---
# <span data-ttu-id="004cf-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="004cf-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="004cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="004cf-102">SYNOPSIS</span></span>
<span data-ttu-id="004cf-103">Создает новую или обновляет существующую группу действий.</span><span class="sxs-lookup"><span data-stu-id="004cf-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="004cf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="004cf-104">SYNTAX</span></span>

### <span data-ttu-id="004cf-105">ByPropertyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="004cf-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="004cf-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="004cf-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="004cf-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="004cf-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="004cf-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="004cf-108">DESCRIPTION</span></span>
<span data-ttu-id="004cf-109">Для создания или обновления **существующей** группы действий будет создан или обновлена существующая группа действий.</span><span class="sxs-lookup"><span data-stu-id="004cf-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="004cf-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="004cf-110">EXAMPLES</span></span>

### <span data-ttu-id="004cf-111">Пример 1. Создание группы действий</span><span class="sxs-lookup"><span data-stu-id="004cf-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="004cf-112">В первых двух командах создаются два приемника.</span><span class="sxs-lookup"><span data-stu-id="004cf-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="004cf-113">Конечная команда создает группу действий, включая два приемника.</span><span class="sxs-lookup"><span data-stu-id="004cf-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="004cf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="004cf-114">PARAMETERS</span></span>

### <span data-ttu-id="004cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004cf-115">-DefaultProfile</span></span>
<span data-ttu-id="004cf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="004cf-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="004cf-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="004cf-117">-DisableGroup</span></span>
<span data-ttu-id="004cf-118">Отключает группу действий.</span><span class="sxs-lookup"><span data-stu-id="004cf-118">Disables the action group.</span></span>

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

### <span data-ttu-id="004cf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="004cf-119">-InputObject</span></span>
<span data-ttu-id="004cf-120">Ресурс группы действий</span><span class="sxs-lookup"><span data-stu-id="004cf-120">The action group resource</span></span>

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

### <span data-ttu-id="004cf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="004cf-121">-Name</span></span>
<span data-ttu-id="004cf-122">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="004cf-122">The name of the action group.</span></span>

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

### <span data-ttu-id="004cf-123">-Receiver</span><span class="sxs-lookup"><span data-stu-id="004cf-123">-Receiver</span></span>
<span data-ttu-id="004cf-124">Список приемников группы действий.</span><span class="sxs-lookup"><span data-stu-id="004cf-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="004cf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="004cf-125">-ResourceGroupName</span></span>
<span data-ttu-id="004cf-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="004cf-126">The resource group nam</span></span>

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

### <span data-ttu-id="004cf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="004cf-127">-ResourceId</span></span>
<span data-ttu-id="004cf-128">Ресурс i</span><span class="sxs-lookup"><span data-stu-id="004cf-128">The resource i</span></span>

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

### <span data-ttu-id="004cf-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="004cf-129">-ShortName</span></span>
<span data-ttu-id="004cf-130">Краткое имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="004cf-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="004cf-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="004cf-131">-Tag</span></span>
<span data-ttu-id="004cf-132">Теги ресурса группы действий</span><span class="sxs-lookup"><span data-stu-id="004cf-132">The tags of the action group resource</span></span>

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

### <span data-ttu-id="004cf-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="004cf-133">-Confirm</span></span>
<span data-ttu-id="004cf-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="004cf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="004cf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="004cf-135">-WhatIf</span></span>
<span data-ttu-id="004cf-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="004cf-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="004cf-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="004cf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="004cf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004cf-138">CommonParameters</span></span>
<span data-ttu-id="004cf-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="004cf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004cf-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="004cf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004cf-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="004cf-141">INPUTS</span></span>

### <span data-ttu-id="004cf-142">System.String</span><span class="sxs-lookup"><span data-stu-id="004cf-142">System.String</span></span>

### <span data-ttu-id="004cf-143">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="004cf-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="004cf-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="004cf-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="004cf-145">System.Collections.Generic.IDictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="004cf-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="004cf-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="004cf-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="004cf-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="004cf-147">OUTPUTS</span></span>

### <span data-ttu-id="004cf-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="004cf-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="004cf-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="004cf-149">NOTES</span></span>

## <span data-ttu-id="004cf-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="004cf-150">RELATED LINKS</span></span>

<span data-ttu-id="004cf-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="004cf-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
