---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 78674e3245da1b8a58e099948bff23df9159efec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074926"
---
# <span data-ttu-id="b7fb5-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="b7fb5-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="b7fb5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7fb5-102">SYNOPSIS</span></span>
<span data-ttu-id="b7fb5-103">Удаляет группу гибридного рабочего процесса из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b7fb5-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="b7fb5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7fb5-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7fb5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7fb5-105">DESCRIPTION</span></span>
<span data-ttu-id="b7fb5-106">Командлет Remove-AzAutomationHybridWorkerGroup удаляет группу гибридного рабочего процесса из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b7fb5-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="b7fb5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7fb5-107">EXAMPLES</span></span>

### <span data-ttu-id="b7fb5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7fb5-108">Example 1</span></span>
<span data-ttu-id="b7fb5-109">Эта команда удаляет гибридный рабочий процесс по имени.</span><span class="sxs-lookup"><span data-stu-id="b7fb5-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="b7fb5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7fb5-110">PARAMETERS</span></span>

### <span data-ttu-id="b7fb5-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b7fb5-111">-AutomationAccountName</span></span>
<span data-ttu-id="b7fb5-112">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b7fb5-112">The automation account name.</span></span>

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

### <span data-ttu-id="b7fb5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7fb5-113">-DefaultProfile</span></span>
<span data-ttu-id="b7fb5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7fb5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7fb5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7fb5-115">-Name</span></span>
<span data-ttu-id="b7fb5-116">Имя гибридной группы рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="b7fb5-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="b7fb5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7fb5-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7fb5-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7fb5-118">The resource group name.</span></span>

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

### <span data-ttu-id="b7fb5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7fb5-119">-Confirm</span></span>
<span data-ttu-id="b7fb5-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b7fb5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7fb5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7fb5-121">-WhatIf</span></span>
<span data-ttu-id="b7fb5-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b7fb5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7fb5-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b7fb5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7fb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7fb5-124">CommonParameters</span></span>
<span data-ttu-id="b7fb5-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7fb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7fb5-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7fb5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7fb5-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7fb5-127">INPUTS</span></span>

### <span data-ttu-id="b7fb5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b7fb5-128">System.String</span></span>

## <span data-ttu-id="b7fb5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7fb5-129">OUTPUTS</span></span>

### <span data-ttu-id="b7fb5-130">System. void</span><span class="sxs-lookup"><span data-stu-id="b7fb5-130">System.Void</span></span>

## <span data-ttu-id="b7fb5-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7fb5-131">NOTES</span></span>

## <span data-ttu-id="b7fb5-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7fb5-132">RELATED LINKS</span></span>
