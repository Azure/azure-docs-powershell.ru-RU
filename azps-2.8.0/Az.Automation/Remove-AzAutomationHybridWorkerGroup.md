---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: b9f23105b6fa84781ef1b0f0ba4be0e52e06ee08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727761"
---
# <span data-ttu-id="181dc-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="181dc-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="181dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="181dc-102">SYNOPSIS</span></span>
<span data-ttu-id="181dc-103">Удаляет группу гибридного рабочего процесса из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="181dc-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="181dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="181dc-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="181dc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="181dc-105">DESCRIPTION</span></span>
<span data-ttu-id="181dc-106">Командлет Remove-AzAutomationHybridWorkerGroup удаляет группу гибридного рабочего процесса из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="181dc-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="181dc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="181dc-107">EXAMPLES</span></span>

### <span data-ttu-id="181dc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="181dc-108">Example 1</span></span>
<span data-ttu-id="181dc-109">Эта команда удаляет гибридный рабочий процесс по имени.</span><span class="sxs-lookup"><span data-stu-id="181dc-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="181dc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="181dc-110">PARAMETERS</span></span>

### <span data-ttu-id="181dc-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="181dc-111">-AutomationAccountName</span></span>
<span data-ttu-id="181dc-112">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="181dc-112">The automation account name.</span></span>

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

### <span data-ttu-id="181dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="181dc-113">-DefaultProfile</span></span>
<span data-ttu-id="181dc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="181dc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="181dc-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="181dc-115">-Name</span></span>
<span data-ttu-id="181dc-116">Имя гибридной группы рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="181dc-116">The hybrid worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="181dc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="181dc-117">-ResourceGroupName</span></span>
<span data-ttu-id="181dc-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="181dc-118">The resource group name.</span></span>

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

### <span data-ttu-id="181dc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="181dc-119">-Confirm</span></span>
<span data-ttu-id="181dc-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="181dc-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181dc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="181dc-121">-WhatIf</span></span>
<span data-ttu-id="181dc-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="181dc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="181dc-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="181dc-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="181dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="181dc-124">CommonParameters</span></span>
<span data-ttu-id="181dc-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="181dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="181dc-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="181dc-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="181dc-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="181dc-127">INPUTS</span></span>

### <span data-ttu-id="181dc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="181dc-128">System.String</span></span>

## <span data-ttu-id="181dc-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="181dc-129">OUTPUTS</span></span>

### <span data-ttu-id="181dc-130">System. void</span><span class="sxs-lookup"><span data-stu-id="181dc-130">System.Void</span></span>

## <span data-ttu-id="181dc-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="181dc-131">NOTES</span></span>

## <span data-ttu-id="181dc-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="181dc-132">RELATED LINKS</span></span>
