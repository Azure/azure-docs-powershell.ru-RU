---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079853"
---
# <span data-ttu-id="0a5b6-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0a5b6-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="0a5b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a5b6-102">SYNOPSIS</span></span>
<span data-ttu-id="0a5b6-103">Удаляет модуль из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="0a5b6-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="0a5b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a5b6-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a5b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a5b6-105">DESCRIPTION</span></span>
<span data-ttu-id="0a5b6-106">Командлет **Remove-AzAutomationModule** удаляет модуль из учетной записи автоматизации в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5b6-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="0a5b6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a5b6-107">EXAMPLES</span></span>

### <span data-ttu-id="0a5b6-108">Пример 1: Удаление модуля</span><span class="sxs-lookup"><span data-stu-id="0a5b6-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0a5b6-109">Эта команда удаляет модуль с именем ContosoModule из учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0a5b6-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0a5b6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a5b6-110">PARAMETERS</span></span>

### <span data-ttu-id="0a5b6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0a5b6-111">-AutomationAccountName</span></span>
<span data-ttu-id="0a5b6-112">Указывает имя учетной записи автоматизации, из которой этот командлет удаляет модуль.</span><span class="sxs-lookup"><span data-stu-id="0a5b6-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="0a5b6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a5b6-113">-DefaultProfile</span></span>
<span data-ttu-id="0a5b6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0a5b6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a5b6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0a5b6-115">-Force</span></span>
<span data-ttu-id="0a5b6-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="0a5b6-116">ps_force</span></span>

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

### <span data-ttu-id="0a5b6-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a5b6-117">-Name</span></span>
<span data-ttu-id="0a5b6-118">Указывает имя модуля, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0a5b6-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0a5b6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a5b6-119">-ResourceGroupName</span></span>
<span data-ttu-id="0a5b6-120">Указывает имя группы ресурсов, в которой этот командлет удаляет модуль.</span><span class="sxs-lookup"><span data-stu-id="0a5b6-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="0a5b6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a5b6-121">-Confirm</span></span>
<span data-ttu-id="0a5b6-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a5b6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a5b6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a5b6-123">-WhatIf</span></span>
<span data-ttu-id="0a5b6-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a5b6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a5b6-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a5b6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a5b6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a5b6-126">CommonParameters</span></span>
<span data-ttu-id="0a5b6-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a5b6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a5b6-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a5b6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a5b6-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a5b6-129">INPUTS</span></span>

### <span data-ttu-id="0a5b6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0a5b6-130">System.String</span></span>

## <span data-ttu-id="0a5b6-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a5b6-131">OUTPUTS</span></span>

### <span data-ttu-id="0a5b6-132">System. void</span><span class="sxs-lookup"><span data-stu-id="0a5b6-132">System.Void</span></span>

## <span data-ttu-id="0a5b6-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a5b6-133">NOTES</span></span>

## <span data-ttu-id="0a5b6-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a5b6-134">RELATED LINKS</span></span>

[<span data-ttu-id="0a5b6-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0a5b6-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="0a5b6-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0a5b6-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="0a5b6-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="0a5b6-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


