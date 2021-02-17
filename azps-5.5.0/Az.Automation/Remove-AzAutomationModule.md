---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239549"
---
# <span data-ttu-id="94439-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="94439-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="94439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94439-102">SYNOPSIS</span></span>
<span data-ttu-id="94439-103">Модуль удаляется из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="94439-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="94439-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94439-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94439-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94439-105">DESCRIPTION</span></span>
<span data-ttu-id="94439-106">Командлет **Remove-AzAutomationModule** удаляет модуль из учетной записи автоматизации в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="94439-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="94439-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94439-107">EXAMPLES</span></span>

### <span data-ttu-id="94439-108">Пример 1. Удаление модуля</span><span class="sxs-lookup"><span data-stu-id="94439-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="94439-109">Эта команда удаляет модуль ContosoModule из учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="94439-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="94439-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94439-110">PARAMETERS</span></span>

### <span data-ttu-id="94439-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="94439-111">-AutomationAccountName</span></span>
<span data-ttu-id="94439-112">Указывает имя учетной записи автоматизации, из которой этот командлет удаляет модуль.</span><span class="sxs-lookup"><span data-stu-id="94439-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="94439-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94439-113">-DefaultProfile</span></span>
<span data-ttu-id="94439-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="94439-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94439-115">-Force</span><span class="sxs-lookup"><span data-stu-id="94439-115">-Force</span></span>
<span data-ttu-id="94439-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="94439-116">ps_force</span></span>

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

### <span data-ttu-id="94439-117">-Name</span><span class="sxs-lookup"><span data-stu-id="94439-117">-Name</span></span>
<span data-ttu-id="94439-118">Указывает имя модуля, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="94439-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="94439-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94439-119">-ResourceGroupName</span></span>
<span data-ttu-id="94439-120">Имя группы ресурсов, из которой этот командлет удаляет модуль.</span><span class="sxs-lookup"><span data-stu-id="94439-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="94439-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94439-121">-Confirm</span></span>
<span data-ttu-id="94439-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94439-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94439-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94439-123">-WhatIf</span></span>
<span data-ttu-id="94439-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94439-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94439-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94439-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94439-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94439-126">CommonParameters</span></span>
<span data-ttu-id="94439-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94439-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94439-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94439-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94439-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94439-129">INPUTS</span></span>

### <span data-ttu-id="94439-130">System.String</span><span class="sxs-lookup"><span data-stu-id="94439-130">System.String</span></span>

## <span data-ttu-id="94439-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94439-131">OUTPUTS</span></span>

### <span data-ttu-id="94439-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="94439-132">System.Void</span></span>

## <span data-ttu-id="94439-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94439-133">NOTES</span></span>

## <span data-ttu-id="94439-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94439-134">RELATED LINKS</span></span>

[<span data-ttu-id="94439-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="94439-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="94439-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="94439-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="94439-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="94439-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


