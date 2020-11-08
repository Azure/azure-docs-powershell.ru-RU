---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 5eb31abcc632f06402b4196be8be4c5e32cdacf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074937"
---
# <span data-ttu-id="333f2-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="333f2-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="333f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="333f2-102">SYNOPSIS</span></span>
<span data-ttu-id="333f2-103">Удаляет тип подключения автоматизации.</span><span class="sxs-lookup"><span data-stu-id="333f2-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="333f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="333f2-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="333f2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="333f2-105">DESCRIPTION</span></span>
<span data-ttu-id="333f2-106">Командлет **Remove-AzAutomationConnectionType** удаляет тип подключения из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="333f2-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="333f2-107">Все подключения, связанные с удаленным типом соединения, будут недоступны для использования.</span><span class="sxs-lookup"><span data-stu-id="333f2-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="333f2-108">Удалите их, если не создать новый тип соединения, отвечающий указанным ниже условиям.</span><span class="sxs-lookup"><span data-stu-id="333f2-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="333f2-109">Тип имеет то же имя, что и исходный тип соединения.</span><span class="sxs-lookup"><span data-stu-id="333f2-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="333f2-110">Этот тип имеет те же определения полей, что и исходный тип соединения.</span><span class="sxs-lookup"><span data-stu-id="333f2-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="333f2-111">У него могут быть дополнительные поля.</span><span class="sxs-lookup"><span data-stu-id="333f2-111">It can have additional fields.</span></span>

## <span data-ttu-id="333f2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="333f2-112">EXAMPLES</span></span>

### <span data-ttu-id="333f2-113">Пример 1: Удаление типа подключения</span><span class="sxs-lookup"><span data-stu-id="333f2-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="333f2-114">Эта команда удаляет тип подключения с именем ContosoConnectionType в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="333f2-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="333f2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="333f2-115">PARAMETERS</span></span>

### <span data-ttu-id="333f2-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="333f2-116">-AutomationAccountName</span></span>
<span data-ttu-id="333f2-117">Указывает имя учетной записи автоматизации, для которой этот командлет удаляет тип подключения.</span><span class="sxs-lookup"><span data-stu-id="333f2-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333f2-118">-DefaultProfile</span></span>
<span data-ttu-id="333f2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="333f2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="333f2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="333f2-120">-Force</span></span>
<span data-ttu-id="333f2-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="333f2-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="333f2-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="333f2-122">-Name</span></span>
<span data-ttu-id="333f2-123">Указывает имя типа подключения автоматизации, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="333f2-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333f2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="333f2-124">-ResourceGroupName</span></span>
<span data-ttu-id="333f2-125">Указывает имя группы ресурсов, из которой этот командлет удаляет тип подключения автоматизации.</span><span class="sxs-lookup"><span data-stu-id="333f2-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="333f2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="333f2-126">-Confirm</span></span>
<span data-ttu-id="333f2-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="333f2-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="333f2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="333f2-128">-WhatIf</span></span>
<span data-ttu-id="333f2-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="333f2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="333f2-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="333f2-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="333f2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333f2-131">CommonParameters</span></span>
<span data-ttu-id="333f2-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="333f2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333f2-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="333f2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333f2-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="333f2-134">INPUTS</span></span>

### <span data-ttu-id="333f2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="333f2-135">System.String</span></span>

## <span data-ttu-id="333f2-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="333f2-136">OUTPUTS</span></span>

### <span data-ttu-id="333f2-137">System. void</span><span class="sxs-lookup"><span data-stu-id="333f2-137">System.Void</span></span>

## <span data-ttu-id="333f2-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="333f2-138">NOTES</span></span>

## <span data-ttu-id="333f2-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="333f2-139">RELATED LINKS</span></span>

[<span data-ttu-id="333f2-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="333f2-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


