---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationModule.md
ms.openlocfilehash: 2ce97441769c15ed122dc7921554b4fa1c5a144f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570284"
---
# <span data-ttu-id="3a651-101">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="3a651-101">Remove-AzureRmAutomationModule</span></span>

## <span data-ttu-id="3a651-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a651-102">SYNOPSIS</span></span>
<span data-ttu-id="3a651-103">Удаляет модуль из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3a651-103">Removes a module from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a651-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a651-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a651-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a651-105">DESCRIPTION</span></span>
<span data-ttu-id="3a651-106">Командлет **Remove-AzureRmAutomationModule** удаляет модуль из учетной записи автоматизации в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="3a651-106">The **Remove-AzureRmAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="3a651-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a651-107">EXAMPLES</span></span>

### <span data-ttu-id="3a651-108">Пример 1: Удаление модуля</span><span class="sxs-lookup"><span data-stu-id="3a651-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3a651-109">Эта команда удаляет модуль с именем ContosoModule из учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3a651-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3a651-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a651-110">PARAMETERS</span></span>

### <span data-ttu-id="3a651-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3a651-111">-AutomationAccountName</span></span>
<span data-ttu-id="3a651-112">Указывает имя учетной записи автоматизации, из которой этот командлет удаляет модуль.</span><span class="sxs-lookup"><span data-stu-id="3a651-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="3a651-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a651-113">-DefaultProfile</span></span>
<span data-ttu-id="3a651-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3a651-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a651-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3a651-115">-Force</span></span>
<span data-ttu-id="3a651-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="3a651-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a651-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a651-117">-Name</span></span>
<span data-ttu-id="3a651-118">Указывает имя модуля, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3a651-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3a651-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a651-119">-ResourceGroupName</span></span>
<span data-ttu-id="3a651-120">Указывает имя группы ресурсов, в которой этот командлет удаляет модуль.</span><span class="sxs-lookup"><span data-stu-id="3a651-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="3a651-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a651-121">-Confirm</span></span>
<span data-ttu-id="3a651-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a651-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a651-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a651-123">-WhatIf</span></span>
<span data-ttu-id="3a651-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a651-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a651-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a651-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a651-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a651-126">CommonParameters</span></span>
<span data-ttu-id="3a651-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a651-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a651-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a651-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a651-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a651-129">INPUTS</span></span>

### <span data-ttu-id="3a651-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="3a651-130">None</span></span>
<span data-ttu-id="3a651-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3a651-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a651-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a651-132">OUTPUTS</span></span>

## <span data-ttu-id="3a651-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a651-133">NOTES</span></span>

## <span data-ttu-id="3a651-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a651-134">RELATED LINKS</span></span>

[<span data-ttu-id="3a651-135">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="3a651-135">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="3a651-136">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="3a651-136">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="3a651-137">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="3a651-137">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


