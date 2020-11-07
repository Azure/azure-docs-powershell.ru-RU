---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: cfb8aa96da85cbfe1e9c16277c5c1c3539e04ac3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727746"
---
# <span data-ttu-id="31a08-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="31a08-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="31a08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31a08-102">SYNOPSIS</span></span>
<span data-ttu-id="31a08-103">Удаляет переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="31a08-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="31a08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31a08-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31a08-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31a08-105">DESCRIPTION</span></span>
<span data-ttu-id="31a08-106">Командлет **Remove-AzAutomationVariable** удаляет переменную из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="31a08-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="31a08-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31a08-107">EXAMPLES</span></span>

### <span data-ttu-id="31a08-108">Пример 1: Удаление переменной</span><span class="sxs-lookup"><span data-stu-id="31a08-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="31a08-109">Эта команда удаляет переменную с именем StringVariable22 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="31a08-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="31a08-110">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="31a08-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="31a08-111">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="31a08-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="31a08-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31a08-112">PARAMETERS</span></span>

### <span data-ttu-id="31a08-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="31a08-113">-AutomationAccountName</span></span>
<span data-ttu-id="31a08-114">Указывает имя учетной записи автоматизации, которая содержит переменную, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="31a08-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="31a08-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a08-115">-DefaultProfile</span></span>
<span data-ttu-id="31a08-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="31a08-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31a08-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31a08-117">-Name</span></span>
<span data-ttu-id="31a08-118">Указывает имя переменной, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="31a08-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="31a08-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a08-119">-ResourceGroupName</span></span>
<span data-ttu-id="31a08-120">Указывает группу ресурсов, для которой этот командлет удаляет переменную.</span><span class="sxs-lookup"><span data-stu-id="31a08-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="31a08-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31a08-121">-Confirm</span></span>
<span data-ttu-id="31a08-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="31a08-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31a08-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31a08-123">-WhatIf</span></span>
<span data-ttu-id="31a08-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="31a08-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31a08-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="31a08-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31a08-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a08-126">CommonParameters</span></span>
<span data-ttu-id="31a08-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31a08-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a08-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31a08-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a08-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31a08-129">INPUTS</span></span>

### <span data-ttu-id="31a08-130">System. String</span><span class="sxs-lookup"><span data-stu-id="31a08-130">System.String</span></span>

## <span data-ttu-id="31a08-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31a08-131">OUTPUTS</span></span>

### <span data-ttu-id="31a08-132">System. void</span><span class="sxs-lookup"><span data-stu-id="31a08-132">System.Void</span></span>

## <span data-ttu-id="31a08-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="31a08-133">NOTES</span></span>

## <span data-ttu-id="31a08-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31a08-134">RELATED LINKS</span></span>

[<span data-ttu-id="31a08-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="31a08-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="31a08-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="31a08-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="31a08-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="31a08-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


