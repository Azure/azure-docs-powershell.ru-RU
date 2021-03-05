---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 35ef4a5629726b33a8d9099da78134e6a0bac8b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009939"
---
# <span data-ttu-id="d747e-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="d747e-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="d747e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d747e-102">SYNOPSIS</span></span>
<span data-ttu-id="d747e-103">Гибридная группа сотрудников удаляется из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d747e-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="d747e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d747e-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d747e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d747e-105">DESCRIPTION</span></span>
<span data-ttu-id="d747e-106">Этот Remove-AzAutomationHybridWorkerGroup удаляет гибридную группу сотрудников из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d747e-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="d747e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d747e-107">EXAMPLES</span></span>

### <span data-ttu-id="d747e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d747e-108">Example 1</span></span>
<span data-ttu-id="d747e-109">Эта команда удаляет гибридного сотрудника по имени.</span><span class="sxs-lookup"><span data-stu-id="d747e-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="d747e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d747e-110">PARAMETERS</span></span>

### <span data-ttu-id="d747e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d747e-111">-AutomationAccountName</span></span>
<span data-ttu-id="d747e-112">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d747e-112">The automation account name.</span></span>

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

### <span data-ttu-id="d747e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d747e-113">-DefaultProfile</span></span>
<span data-ttu-id="d747e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d747e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d747e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d747e-115">-Name</span></span>
<span data-ttu-id="d747e-116">Имя гибридной группы сотрудников.</span><span class="sxs-lookup"><span data-stu-id="d747e-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="d747e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d747e-117">-ResourceGroupName</span></span>
<span data-ttu-id="d747e-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d747e-118">The resource group name.</span></span>

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

### <span data-ttu-id="d747e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d747e-119">-Confirm</span></span>
<span data-ttu-id="d747e-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d747e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d747e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d747e-121">-WhatIf</span></span>
<span data-ttu-id="d747e-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d747e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d747e-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d747e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d747e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d747e-124">CommonParameters</span></span>
<span data-ttu-id="d747e-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d747e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d747e-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d747e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d747e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d747e-127">INPUTS</span></span>

### <span data-ttu-id="d747e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d747e-128">System.String</span></span>

## <span data-ttu-id="d747e-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d747e-129">OUTPUTS</span></span>

### <span data-ttu-id="d747e-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="d747e-130">System.Void</span></span>

## <span data-ttu-id="d747e-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d747e-131">NOTES</span></span>

## <span data-ttu-id="d747e-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d747e-132">RELATED LINKS</span></span>
