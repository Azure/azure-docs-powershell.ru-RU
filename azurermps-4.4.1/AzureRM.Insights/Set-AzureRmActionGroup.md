---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: 29ef822e61c13d3ea976002c465a7c114296da9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567124"
---
# <span data-ttu-id="2596d-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="2596d-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="2596d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2596d-102">SYNOPSIS</span></span>
<span data-ttu-id="2596d-103">Создает новую или обновляет существующую группу действий.</span><span class="sxs-lookup"><span data-stu-id="2596d-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2596d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2596d-104">SYNTAX</span></span>

### <span data-ttu-id="2596d-105">ByPropertyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2596d-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2596d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2596d-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2596d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2596d-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2596d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2596d-108">DESCRIPTION</span></span>
<span data-ttu-id="2596d-109">Командлет **Set-AzureRmActionGroup** создает новый или обновляет существующую группу действий</span><span class="sxs-lookup"><span data-stu-id="2596d-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="2596d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2596d-110">EXAMPLES</span></span>

### <span data-ttu-id="2596d-111">Пример 1: создание группы действий</span><span class="sxs-lookup"><span data-stu-id="2596d-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="2596d-112">Первые две команды создают два получателя.</span><span class="sxs-lookup"><span data-stu-id="2596d-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="2596d-113">В последней команде создается группа действий, в том числе два получателя.</span><span class="sxs-lookup"><span data-stu-id="2596d-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="2596d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2596d-114">PARAMETERS</span></span>

### <span data-ttu-id="2596d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2596d-115">-Name</span></span>
<span data-ttu-id="2596d-116">Имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="2596d-116">The name of the action group.</span></span>

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

### <span data-ttu-id="2596d-117">-ShortName</span><span class="sxs-lookup"><span data-stu-id="2596d-117">-ShortName</span></span>
<span data-ttu-id="2596d-118">Краткое имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="2596d-118">The short name of the action group.</span></span>

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

### <span data-ttu-id="2596d-119">-Получатель</span><span class="sxs-lookup"><span data-stu-id="2596d-119">-Receiver</span></span>
<span data-ttu-id="2596d-120">Список получателей группы действий.</span><span class="sxs-lookup"><span data-stu-id="2596d-120">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="2596d-121">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="2596d-121">-DisableGroup</span></span>
<span data-ttu-id="2596d-122">Отключение группы действий.</span><span class="sxs-lookup"><span data-stu-id="2596d-122">Disables the action group.</span></span>

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

### <span data-ttu-id="2596d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2596d-123">-Confirm</span></span>
<span data-ttu-id="2596d-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2596d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2596d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2596d-125">-DefaultProfile</span></span>
<span data-ttu-id="2596d-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2596d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2596d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2596d-127">-InputObject</span></span>
<span data-ttu-id="2596d-128">Ресурс группы действий</span><span class="sxs-lookup"><span data-stu-id="2596d-128">The action group resource</span></span>

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

### <span data-ttu-id="2596d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2596d-129">-ResourceGroupName</span></span>
<span data-ttu-id="2596d-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2596d-130">The resource group name</span></span>

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

### <span data-ttu-id="2596d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2596d-131">-ResourceId</span></span>
<span data-ttu-id="2596d-132">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="2596d-132">The resource id</span></span>

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

### <span data-ttu-id="2596d-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="2596d-133">-Tag</span></span>
<span data-ttu-id="2596d-134">Теги ресурса группы действий</span><span class="sxs-lookup"><span data-stu-id="2596d-134">The tags of the action group resource</span></span>

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

### <span data-ttu-id="2596d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2596d-135">-WhatIf</span></span>
<span data-ttu-id="2596d-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2596d-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2596d-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2596d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2596d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2596d-138">CommonParameters</span></span>
<span data-ttu-id="2596d-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2596d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2596d-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2596d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2596d-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2596d-141">INPUTS</span></span>

## <span data-ttu-id="2596d-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2596d-142">OUTPUTS</span></span>

### <span data-ttu-id="2596d-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="2596d-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="2596d-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="2596d-144">NOTES</span></span>

## <span data-ttu-id="2596d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2596d-145">RELATED LINKS</span></span>

<span data-ttu-id="2596d-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="2596d-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
