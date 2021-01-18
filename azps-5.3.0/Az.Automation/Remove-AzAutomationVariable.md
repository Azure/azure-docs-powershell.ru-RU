---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509882"
---
# <span data-ttu-id="142d5-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="142d5-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="142d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="142d5-102">SYNOPSIS</span></span>
<span data-ttu-id="142d5-103">Удаляет переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="142d5-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="142d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="142d5-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="142d5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="142d5-105">DESCRIPTION</span></span>
<span data-ttu-id="142d5-106">При **этом из автоматизации** Azure удаляется переменная.</span><span class="sxs-lookup"><span data-stu-id="142d5-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="142d5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="142d5-107">EXAMPLES</span></span>

### <span data-ttu-id="142d5-108">Пример 1. Удаление переменной</span><span class="sxs-lookup"><span data-stu-id="142d5-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="142d5-109">Эта команда удаляет переменную с именем StringVariable22 в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="142d5-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="142d5-110">Эта команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="142d5-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="142d5-111">Поэтому запрос на подтверждение не будет.</span><span class="sxs-lookup"><span data-stu-id="142d5-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="142d5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="142d5-112">PARAMETERS</span></span>

### <span data-ttu-id="142d5-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="142d5-113">-AutomationAccountName</span></span>
<span data-ttu-id="142d5-114">Указывает имя учетной записи автоматизации, содержаной переменную, удаляемую этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="142d5-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="142d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="142d5-115">-DefaultProfile</span></span>
<span data-ttu-id="142d5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="142d5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="142d5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="142d5-117">-Name</span></span>
<span data-ttu-id="142d5-118">Указывает имя переменной, удаляемой этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="142d5-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="142d5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="142d5-119">-ResourceGroupName</span></span>
<span data-ttu-id="142d5-120">Определяет группу ресурсов, для которой этот cmdlet удаляет переменную.</span><span class="sxs-lookup"><span data-stu-id="142d5-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="142d5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="142d5-121">-Confirm</span></span>
<span data-ttu-id="142d5-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="142d5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="142d5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="142d5-123">-WhatIf</span></span>
<span data-ttu-id="142d5-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="142d5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="142d5-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="142d5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="142d5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="142d5-126">CommonParameters</span></span>
<span data-ttu-id="142d5-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="142d5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="142d5-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="142d5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="142d5-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="142d5-129">INPUTS</span></span>

### <span data-ttu-id="142d5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="142d5-130">System.String</span></span>

## <span data-ttu-id="142d5-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="142d5-131">OUTPUTS</span></span>

### <span data-ttu-id="142d5-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="142d5-132">System.Void</span></span>

## <span data-ttu-id="142d5-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="142d5-133">NOTES</span></span>

## <span data-ttu-id="142d5-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="142d5-134">RELATED LINKS</span></span>

[<span data-ttu-id="142d5-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="142d5-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="142d5-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="142d5-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="142d5-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="142d5-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


