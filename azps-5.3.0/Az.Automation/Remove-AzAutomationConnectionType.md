---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 5eb31abcc632f06402b4196be8be4c5e32cdacf0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509922"
---
# <span data-ttu-id="9e870-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="9e870-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="9e870-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e870-102">SYNOPSIS</span></span>
<span data-ttu-id="9e870-103">Удаляет тип соединения автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9e870-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="9e870-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9e870-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e870-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e870-105">DESCRIPTION</span></span>
<span data-ttu-id="9e870-106">Для **этого из автоматизации** Azure удаляется тип подключения.</span><span class="sxs-lookup"><span data-stu-id="9e870-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="9e870-107">Все подключения, связанные с удаляемым типом подключения, становятся недоступными.</span><span class="sxs-lookup"><span data-stu-id="9e870-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="9e870-108">Удалите их, если только вы не создайте новый тип подключения, который соответствует следующим условиям:</span><span class="sxs-lookup"><span data-stu-id="9e870-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="9e870-109">Этот тип имеет то же имя, что и исходный тип подключения.</span><span class="sxs-lookup"><span data-stu-id="9e870-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="9e870-110">Этот тип имеет те же определения полей, что и исходный тип подключения.</span><span class="sxs-lookup"><span data-stu-id="9e870-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="9e870-111">Оно может иметь дополнительные поля.</span><span class="sxs-lookup"><span data-stu-id="9e870-111">It can have additional fields.</span></span>

## <span data-ttu-id="9e870-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9e870-112">EXAMPLES</span></span>

### <span data-ttu-id="9e870-113">Пример 1. Удаление типа подключения</span><span class="sxs-lookup"><span data-stu-id="9e870-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9e870-114">Эта команда удаляет тип подключения ContosoConnectionType в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9e870-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9e870-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e870-115">PARAMETERS</span></span>

### <span data-ttu-id="9e870-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e870-116">-AutomationAccountName</span></span>
<span data-ttu-id="9e870-117">Указывает имя учетной записи автоматизации, для которой этот cmdlet удаляет тип подключения.</span><span class="sxs-lookup"><span data-stu-id="9e870-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="9e870-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e870-118">-DefaultProfile</span></span>
<span data-ttu-id="9e870-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9e870-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e870-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9e870-120">-Force</span></span>
<span data-ttu-id="9e870-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="9e870-121">ps_force</span></span>

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

### <span data-ttu-id="9e870-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9e870-122">-Name</span></span>
<span data-ttu-id="9e870-123">Указывает имя типа подключения автоматизации, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e870-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9e870-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e870-124">-ResourceGroupName</span></span>
<span data-ttu-id="9e870-125">Имя группы ресурсов, из которой этот cmdlet удаляет тип подключения автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9e870-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="9e870-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e870-126">-Confirm</span></span>
<span data-ttu-id="9e870-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9e870-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e870-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e870-128">-WhatIf</span></span>
<span data-ttu-id="9e870-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e870-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e870-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9e870-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e870-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e870-131">CommonParameters</span></span>
<span data-ttu-id="9e870-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e870-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e870-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e870-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e870-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9e870-134">INPUTS</span></span>

### <span data-ttu-id="9e870-135">System.String</span><span class="sxs-lookup"><span data-stu-id="9e870-135">System.String</span></span>

## <span data-ttu-id="9e870-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9e870-136">OUTPUTS</span></span>

### <span data-ttu-id="9e870-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="9e870-137">System.Void</span></span>

## <span data-ttu-id="9e870-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9e870-138">NOTES</span></span>

## <span data-ttu-id="9e870-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e870-139">RELATED LINKS</span></span>

[<span data-ttu-id="9e870-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9e870-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


