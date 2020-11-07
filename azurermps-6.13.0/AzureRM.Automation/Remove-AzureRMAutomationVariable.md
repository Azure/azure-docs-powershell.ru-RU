---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: b336104fea097b0f5adf0993853dd6fff7bba1f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733183"
---
# <span data-ttu-id="c0a92-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c0a92-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="c0a92-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0a92-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a92-103">Удаляет переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c0a92-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0a92-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0a92-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0a92-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0a92-105">DESCRIPTION</span></span>
<span data-ttu-id="c0a92-106">Командлет **Remove-AzureRmAutomationVariable** удаляет переменную из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c0a92-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="c0a92-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0a92-107">EXAMPLES</span></span>

### <span data-ttu-id="c0a92-108">Пример 1: Удаление переменной</span><span class="sxs-lookup"><span data-stu-id="c0a92-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c0a92-109">Эта команда удаляет переменную с именем StringVariable22 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c0a92-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="c0a92-110">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="c0a92-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c0a92-111">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c0a92-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c0a92-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0a92-112">PARAMETERS</span></span>

### <span data-ttu-id="c0a92-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0a92-113">-AutomationAccountName</span></span>
<span data-ttu-id="c0a92-114">Указывает имя учетной записи автоматизации, которая содержит переменную, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c0a92-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c0a92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a92-115">-DefaultProfile</span></span>
<span data-ttu-id="c0a92-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c0a92-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0a92-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0a92-117">-Name</span></span>
<span data-ttu-id="c0a92-118">Указывает имя переменной, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c0a92-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c0a92-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0a92-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0a92-120">Указывает группу ресурсов, для которой этот командлет удаляет переменную.</span><span class="sxs-lookup"><span data-stu-id="c0a92-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="c0a92-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0a92-121">-Confirm</span></span>
<span data-ttu-id="c0a92-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c0a92-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0a92-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0a92-123">-WhatIf</span></span>
<span data-ttu-id="c0a92-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c0a92-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0a92-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c0a92-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0a92-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a92-126">CommonParameters</span></span>
<span data-ttu-id="c0a92-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0a92-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a92-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0a92-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a92-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0a92-129">INPUTS</span></span>

### <span data-ttu-id="c0a92-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c0a92-130">System.String</span></span>

## <span data-ttu-id="c0a92-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0a92-131">OUTPUTS</span></span>

### <span data-ttu-id="c0a92-132">System. void</span><span class="sxs-lookup"><span data-stu-id="c0a92-132">System.Void</span></span>

## <span data-ttu-id="c0a92-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0a92-133">NOTES</span></span>

## <span data-ttu-id="c0a92-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0a92-134">RELATED LINKS</span></span>

[<span data-ttu-id="c0a92-135">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c0a92-135">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="c0a92-136">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c0a92-136">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="c0a92-137">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c0a92-137">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


