---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 78674e3245da1b8a58e099948bff23df9159efec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239557"
---
# <span data-ttu-id="b415c-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="b415c-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="b415c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b415c-102">SYNOPSIS</span></span>
<span data-ttu-id="b415c-103">Гибридная группа сотрудников удаляется из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b415c-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="b415c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b415c-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b415c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b415c-105">DESCRIPTION</span></span>
<span data-ttu-id="b415c-106">Этот Remove-AzAutomationHybridWorkerGroup удаляет гибридную группу сотрудников из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b415c-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="b415c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b415c-107">EXAMPLES</span></span>

### <span data-ttu-id="b415c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b415c-108">Example 1</span></span>
<span data-ttu-id="b415c-109">Эта команда удаляет гибридного сотрудника по имени.</span><span class="sxs-lookup"><span data-stu-id="b415c-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="b415c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b415c-110">PARAMETERS</span></span>

### <span data-ttu-id="b415c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b415c-111">-AutomationAccountName</span></span>
<span data-ttu-id="b415c-112">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b415c-112">The automation account name.</span></span>

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

### <span data-ttu-id="b415c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b415c-113">-DefaultProfile</span></span>
<span data-ttu-id="b415c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b415c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b415c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b415c-115">-Name</span></span>
<span data-ttu-id="b415c-116">Имя гибридной группы сотрудников.</span><span class="sxs-lookup"><span data-stu-id="b415c-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="b415c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b415c-117">-ResourceGroupName</span></span>
<span data-ttu-id="b415c-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b415c-118">The resource group name.</span></span>

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

### <span data-ttu-id="b415c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b415c-119">-Confirm</span></span>
<span data-ttu-id="b415c-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b415c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b415c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b415c-121">-WhatIf</span></span>
<span data-ttu-id="b415c-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b415c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b415c-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b415c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b415c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b415c-124">CommonParameters</span></span>
<span data-ttu-id="b415c-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b415c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b415c-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b415c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b415c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b415c-127">INPUTS</span></span>

### <span data-ttu-id="b415c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b415c-128">System.String</span></span>

## <span data-ttu-id="b415c-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b415c-129">OUTPUTS</span></span>

### <span data-ttu-id="b415c-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="b415c-130">System.Void</span></span>

## <span data-ttu-id="b415c-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b415c-131">NOTES</span></span>

## <span data-ttu-id="b415c-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b415c-132">RELATED LINKS</span></span>
