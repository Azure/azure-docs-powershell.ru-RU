---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418351"
---
# <span data-ttu-id="1f103-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1f103-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="1f103-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f103-102">SYNOPSIS</span></span>
<span data-ttu-id="1f103-103">Модуль удаляется из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1f103-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="1f103-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1f103-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f103-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f103-105">DESCRIPTION</span></span>
<span data-ttu-id="1f103-106">Командлет **Remove-AzAutomationModule** удаляет модуль из учетной записи автоматизации в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1f103-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="1f103-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1f103-107">EXAMPLES</span></span>

### <span data-ttu-id="1f103-108">Пример 1. Удаление модуля</span><span class="sxs-lookup"><span data-stu-id="1f103-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1f103-109">Эта команда удаляет модуль ContosoModule из учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1f103-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1f103-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f103-110">PARAMETERS</span></span>

### <span data-ttu-id="1f103-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1f103-111">-AutomationAccountName</span></span>
<span data-ttu-id="1f103-112">Указывает имя учетной записи автоматизации, из которой этот командлет удаляет модуль.</span><span class="sxs-lookup"><span data-stu-id="1f103-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="1f103-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f103-113">-DefaultProfile</span></span>
<span data-ttu-id="1f103-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1f103-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f103-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1f103-115">-Force</span></span>
<span data-ttu-id="1f103-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="1f103-116">ps_force</span></span>

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

### <span data-ttu-id="1f103-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1f103-117">-Name</span></span>
<span data-ttu-id="1f103-118">Указывает имя модуля, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1f103-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1f103-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f103-119">-ResourceGroupName</span></span>
<span data-ttu-id="1f103-120">Указывает имя группы ресурсов, из которой этот командлет удаляет модуль.</span><span class="sxs-lookup"><span data-stu-id="1f103-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="1f103-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f103-121">-Confirm</span></span>
<span data-ttu-id="1f103-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1f103-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f103-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f103-123">-WhatIf</span></span>
<span data-ttu-id="1f103-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f103-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f103-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1f103-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f103-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f103-126">CommonParameters</span></span>
<span data-ttu-id="1f103-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f103-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f103-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f103-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f103-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f103-129">INPUTS</span></span>

### <span data-ttu-id="1f103-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1f103-130">System.String</span></span>

## <span data-ttu-id="1f103-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f103-131">OUTPUTS</span></span>

### <span data-ttu-id="1f103-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="1f103-132">System.Void</span></span>

## <span data-ttu-id="1f103-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1f103-133">NOTES</span></span>

## <span data-ttu-id="1f103-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f103-134">RELATED LINKS</span></span>

[<span data-ttu-id="1f103-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1f103-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="1f103-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1f103-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="1f103-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1f103-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


