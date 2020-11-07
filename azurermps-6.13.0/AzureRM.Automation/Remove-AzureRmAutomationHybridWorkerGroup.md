---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
ms.openlocfilehash: b6f15bc55c2e9f9a05e60e7e6f2c139ddbb70454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732324"
---
# <span data-ttu-id="7a2bd-101">Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="7a2bd-101">Remove-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="7a2bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7a2bd-102">SYNOPSIS</span></span>
<span data-ttu-id="7a2bd-103">Удаляет группу гибридного рабочего процесса из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7a2bd-103">Removes hybrid worker group from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a2bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7a2bd-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a2bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a2bd-105">DESCRIPTION</span></span>
<span data-ttu-id="7a2bd-106">Командлет Remove-AzureRmAutomationHybridWorkerGroup удаляет группу гибридного рабочего процесса из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7a2bd-106">The Remove-AzureRmAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="7a2bd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7a2bd-107">EXAMPLES</span></span>

### <span data-ttu-id="7a2bd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a2bd-108">Example 1</span></span>
<span data-ttu-id="7a2bd-109">Эта команда удаляет гибридный рабочий процесс по имени.</span><span class="sxs-lookup"><span data-stu-id="7a2bd-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="7a2bd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7a2bd-110">PARAMETERS</span></span>

### <span data-ttu-id="7a2bd-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7a2bd-111">-AutomationAccountName</span></span>
<span data-ttu-id="7a2bd-112">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7a2bd-112">The automation account name.</span></span>

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

### <span data-ttu-id="7a2bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a2bd-113">-DefaultProfile</span></span>
<span data-ttu-id="7a2bd-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a2bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a2bd-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7a2bd-115">-Name</span></span>
<span data-ttu-id="7a2bd-116">Имя гибридной группы рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="7a2bd-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="7a2bd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a2bd-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a2bd-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a2bd-118">The resource group name.</span></span>

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

### <span data-ttu-id="7a2bd-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a2bd-119">-Confirm</span></span>
<span data-ttu-id="7a2bd-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7a2bd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a2bd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a2bd-121">-WhatIf</span></span>
<span data-ttu-id="7a2bd-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7a2bd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a2bd-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7a2bd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a2bd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a2bd-124">CommonParameters</span></span>
<span data-ttu-id="7a2bd-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7a2bd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a2bd-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a2bd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a2bd-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7a2bd-127">INPUTS</span></span>

### <span data-ttu-id="7a2bd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7a2bd-128">System.String</span></span>

## <span data-ttu-id="7a2bd-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a2bd-129">OUTPUTS</span></span>

### <span data-ttu-id="7a2bd-130">System. void</span><span class="sxs-lookup"><span data-stu-id="7a2bd-130">System.Void</span></span>

## <span data-ttu-id="7a2bd-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7a2bd-131">NOTES</span></span>

## <span data-ttu-id="7a2bd-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a2bd-132">RELATED LINKS</span></span>
