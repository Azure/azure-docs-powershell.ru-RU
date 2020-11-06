---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationVariable.md
ms.openlocfilehash: dea9f62583cca8f3a5ee9ce05b6b7e60e8bf4755
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565000"
---
# <span data-ttu-id="7fe1e-101">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="7fe1e-101">Remove-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="7fe1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fe1e-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe1e-103">Удаляет переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-103">Removes an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fe1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fe1e-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7fe1e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fe1e-105">DESCRIPTION</span></span>
<span data-ttu-id="7fe1e-106">Командлет **Remove-AzureRmAutomationVariable** удаляет переменную из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-106">The **Remove-AzureRmAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="7fe1e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fe1e-107">EXAMPLES</span></span>

### <span data-ttu-id="7fe1e-108">Пример 1: Удаление переменной</span><span class="sxs-lookup"><span data-stu-id="7fe1e-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7fe1e-109">Эта команда удаляет переменную с именем StringVariable22 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="7fe1e-110">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="7fe1e-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="7fe1e-111">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7fe1e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fe1e-112">PARAMETERS</span></span>

### <span data-ttu-id="7fe1e-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7fe1e-113">-AutomationAccountName</span></span>
<span data-ttu-id="7fe1e-114">Указывает имя учетной записи автоматизации, которая содержит переменную, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe1e-115">-DefaultProfile</span></span>
<span data-ttu-id="7fe1e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7fe1e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fe1e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7fe1e-117">-Name</span></span>
<span data-ttu-id="7fe1e-118">Указывает имя переменной, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe1e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fe1e-119">-ResourceGroupName</span></span>
<span data-ttu-id="7fe1e-120">Указывает группу ресурсов, для которой этот командлет удаляет переменную.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe1e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fe1e-121">-Confirm</span></span>
<span data-ttu-id="7fe1e-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fe1e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fe1e-123">-WhatIf</span></span>
<span data-ttu-id="7fe1e-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fe1e-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fe1e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe1e-126">CommonParameters</span></span>
<span data-ttu-id="7fe1e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe1e-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fe1e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe1e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fe1e-129">INPUTS</span></span>

### <span data-ttu-id="7fe1e-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="7fe1e-130">None</span></span>
<span data-ttu-id="7fe1e-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7fe1e-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7fe1e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fe1e-132">OUTPUTS</span></span>

### <span data-ttu-id="7fe1e-133">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="7fe1e-133">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="7fe1e-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fe1e-134">NOTES</span></span>

## <span data-ttu-id="7fe1e-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fe1e-135">RELATED LINKS</span></span>

[<span data-ttu-id="7fe1e-136">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="7fe1e-136">Get-AzureRmAutomationVariable</span></span>](./Get-AzureRMAutomationVariable.md)

[<span data-ttu-id="7fe1e-137">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="7fe1e-137">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="7fe1e-138">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="7fe1e-138">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


