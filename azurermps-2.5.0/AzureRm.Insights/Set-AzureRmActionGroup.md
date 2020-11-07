---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 3f8b3ad20e9a80344227a28dd7cd1f2763cbaab4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913471"
---
# <span data-ttu-id="667a2-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="667a2-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="667a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="667a2-102">SYNOPSIS</span></span>
<span data-ttu-id="667a2-103">Создает новую или обновляет существующую группу действий.</span><span class="sxs-lookup"><span data-stu-id="667a2-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="667a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="667a2-104">SYNTAX</span></span>

### <span data-ttu-id="667a2-105">ByPropertyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="667a2-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667a2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="667a2-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="667a2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="667a2-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="667a2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="667a2-108">DESCRIPTION</span></span>
<span data-ttu-id="667a2-109">Командлет **Set-AzureRmActionGroup** создает новый или обновляет существующую группу действий</span><span class="sxs-lookup"><span data-stu-id="667a2-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="667a2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="667a2-110">EXAMPLES</span></span>

### <span data-ttu-id="667a2-111">Пример 1: создание группы действий</span><span class="sxs-lookup"><span data-stu-id="667a2-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="667a2-112">Первые две команды создают два получателя.</span><span class="sxs-lookup"><span data-stu-id="667a2-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="667a2-113">В последней команде создается группа действий, в том числе два получателя.</span><span class="sxs-lookup"><span data-stu-id="667a2-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="667a2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="667a2-114">PARAMETERS</span></span>

### <span data-ttu-id="667a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667a2-115">-DefaultProfile</span></span>
<span data-ttu-id="667a2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="667a2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667a2-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="667a2-117">-DisableGroup</span></span>
<span data-ttu-id="667a2-118">Отключение группы действий.</span><span class="sxs-lookup"><span data-stu-id="667a2-118">Disables the action group.</span></span>

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

### <span data-ttu-id="667a2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="667a2-119">-InputObject</span></span>
<span data-ttu-id="667a2-120">Группа "действия" resourc</span><span class="sxs-lookup"><span data-stu-id="667a2-120">The action group resourc</span></span>

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

### <span data-ttu-id="667a2-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="667a2-121">-Name</span></span>
<span data-ttu-id="667a2-122">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="667a2-122">The name of the action group.</span></span>

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

### <span data-ttu-id="667a2-123">-Получатель</span><span class="sxs-lookup"><span data-stu-id="667a2-123">-Receiver</span></span>
<span data-ttu-id="667a2-124">Список получателей группы действий.</span><span class="sxs-lookup"><span data-stu-id="667a2-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="667a2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667a2-125">-ResourceGroupName</span></span>
<span data-ttu-id="667a2-126">"Группа ресурсов"</span><span class="sxs-lookup"><span data-stu-id="667a2-126">The resource group nam</span></span>

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

### <span data-ttu-id="667a2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="667a2-127">-ResourceId</span></span>
<span data-ttu-id="667a2-128">Ресурс</span><span class="sxs-lookup"><span data-stu-id="667a2-128">The resource i</span></span>

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

### <span data-ttu-id="667a2-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="667a2-129">-ShortName</span></span>
<span data-ttu-id="667a2-130">Краткое имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="667a2-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="667a2-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="667a2-131">-Tag</span></span>
<span data-ttu-id="667a2-132">Теги группы действий resourc</span><span class="sxs-lookup"><span data-stu-id="667a2-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="667a2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="667a2-133">-Confirm</span></span>
<span data-ttu-id="667a2-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="667a2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="667a2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667a2-135">-WhatIf</span></span>
<span data-ttu-id="667a2-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="667a2-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="667a2-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="667a2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="667a2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667a2-138">CommonParameters</span></span>
<span data-ttu-id="667a2-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="667a2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667a2-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="667a2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667a2-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="667a2-141">INPUTS</span></span>

### <span data-ttu-id="667a2-142">System. String</span><span class="sxs-lookup"><span data-stu-id="667a2-142">System.String</span></span>

### <span data-ttu-id="667a2-143">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="667a2-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="667a2-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="667a2-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="667a2-145">System. Collections. Generic. IDictionary "2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="667a2-145">System.Collections.Generic.IDictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="667a2-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="667a2-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="667a2-147">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="667a2-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="667a2-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="667a2-148">OUTPUTS</span></span>

### <span data-ttu-id="667a2-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="667a2-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="667a2-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="667a2-150">NOTES</span></span>

## <span data-ttu-id="667a2-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="667a2-151">RELATED LINKS</span></span>

<span data-ttu-id="667a2-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="667a2-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
