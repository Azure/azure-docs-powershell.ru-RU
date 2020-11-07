---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: aad8ebb5b78163319ca0c6f56780bd0e336853f7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910181"
---
# <span data-ttu-id="6358a-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="6358a-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="6358a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6358a-102">SYNOPSIS</span></span>
<span data-ttu-id="6358a-103">Создает новую или обновляет существующую группу действий.</span><span class="sxs-lookup"><span data-stu-id="6358a-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="6358a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6358a-104">SYNTAX</span></span>

### <span data-ttu-id="6358a-105">ByPropertyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6358a-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6358a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6358a-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6358a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6358a-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6358a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6358a-108">DESCRIPTION</span></span>
<span data-ttu-id="6358a-109">Командлет **Set-AzActionGroup** создает новый или обновляет существующую группу действий</span><span class="sxs-lookup"><span data-stu-id="6358a-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="6358a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6358a-110">EXAMPLES</span></span>

### <span data-ttu-id="6358a-111">Пример 1: создание группы действий</span><span class="sxs-lookup"><span data-stu-id="6358a-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="6358a-112">Первые две команды создают два получателя.</span><span class="sxs-lookup"><span data-stu-id="6358a-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="6358a-113">В последней команде создается группа действий, в том числе два получателя.</span><span class="sxs-lookup"><span data-stu-id="6358a-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="6358a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6358a-114">PARAMETERS</span></span>

### <span data-ttu-id="6358a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6358a-115">-DefaultProfile</span></span>
<span data-ttu-id="6358a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6358a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6358a-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="6358a-117">-DisableGroup</span></span>
<span data-ttu-id="6358a-118">Отключение группы действий.</span><span class="sxs-lookup"><span data-stu-id="6358a-118">Disables the action group.</span></span>

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

### <span data-ttu-id="6358a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6358a-119">-InputObject</span></span>
<span data-ttu-id="6358a-120">Ресурс группы действий</span><span class="sxs-lookup"><span data-stu-id="6358a-120">The action group resource</span></span>

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

### <span data-ttu-id="6358a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6358a-121">-Name</span></span>
<span data-ttu-id="6358a-122">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="6358a-122">The name of the action group.</span></span>

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

### <span data-ttu-id="6358a-123">-Получатель</span><span class="sxs-lookup"><span data-stu-id="6358a-123">-Receiver</span></span>
<span data-ttu-id="6358a-124">Список получателей группы действий.</span><span class="sxs-lookup"><span data-stu-id="6358a-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="6358a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6358a-125">-ResourceGroupName</span></span>
<span data-ttu-id="6358a-126">"Группа ресурсов"</span><span class="sxs-lookup"><span data-stu-id="6358a-126">The resource group nam</span></span>

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

### <span data-ttu-id="6358a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6358a-127">-ResourceId</span></span>
<span data-ttu-id="6358a-128">Ресурс</span><span class="sxs-lookup"><span data-stu-id="6358a-128">The resource i</span></span>

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

### <span data-ttu-id="6358a-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="6358a-129">-ShortName</span></span>
<span data-ttu-id="6358a-130">Краткое имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="6358a-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="6358a-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="6358a-131">-Tag</span></span>
<span data-ttu-id="6358a-132">Теги ресурса группы действий</span><span class="sxs-lookup"><span data-stu-id="6358a-132">The tags of the action group resource</span></span>

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

### <span data-ttu-id="6358a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6358a-133">-Confirm</span></span>
<span data-ttu-id="6358a-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6358a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6358a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6358a-135">-WhatIf</span></span>
<span data-ttu-id="6358a-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6358a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6358a-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6358a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6358a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6358a-138">CommonParameters</span></span>
<span data-ttu-id="6358a-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6358a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6358a-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6358a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6358a-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6358a-141">INPUTS</span></span>

### <span data-ttu-id="6358a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6358a-142">System.String</span></span>

### <span data-ttu-id="6358a-143">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. PowerShell. командлеты. Monitor, версия = 1.0.0.0, культура = независимая, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="6358a-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6358a-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6358a-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6358a-145">System. Collections. Generic. IDictionary "2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6358a-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6358a-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="6358a-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="6358a-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6358a-147">OUTPUTS</span></span>

### <span data-ttu-id="6358a-148">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="6358a-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="6358a-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="6358a-149">NOTES</span></span>

## <span data-ttu-id="6358a-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6358a-150">RELATED LINKS</span></span>

<span data-ttu-id="6358a-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="6358a-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
