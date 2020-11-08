---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: e5422cc9254b8393330152bcaab880013b5ef99c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074921"
---
# <span data-ttu-id="dd6b6-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="dd6b6-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="dd6b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd6b6-102">SYNOPSIS</span></span>
<span data-ttu-id="dd6b6-103">Удаляет элемент управления источником автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="dd6b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd6b6-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd6b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd6b6-105">DESCRIPTION</span></span>
<span data-ttu-id="dd6b6-106">Командлет Remove-AzAutomationSourceControl удаляет исходный элемент управления из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="dd6b6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd6b6-107">EXAMPLES</span></span>

### <span data-ttu-id="dd6b6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dd6b6-108">Example 1</span></span>
<span data-ttu-id="dd6b6-109">Эта команда удаляет элемент управления источником автоматизации с именем VSTSNative в учетной записи с именем devAccount.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="dd6b6-110">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="dd6b6-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="dd6b6-111">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="dd6b6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd6b6-112">PARAMETERS</span></span>

### <span data-ttu-id="dd6b6-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dd6b6-113">-AutomationAccountName</span></span>
<span data-ttu-id="dd6b6-114">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-114">The automation account name.</span></span>

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

### <span data-ttu-id="dd6b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd6b6-115">-DefaultProfile</span></span>
<span data-ttu-id="dd6b6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd6b6-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd6b6-117">-Name</span></span>
<span data-ttu-id="dd6b6-118">Имя исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-118">The source control name.</span></span>

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

### <span data-ttu-id="dd6b6-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd6b6-119">-PassThru</span></span>
<span data-ttu-id="dd6b6-120">Функция PassThru возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dd6b6-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6b6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd6b6-122">-ResourceGroupName</span></span>
<span data-ttu-id="dd6b6-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-123">The resource group name.</span></span>

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

### <span data-ttu-id="dd6b6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd6b6-124">-Confirm</span></span>
<span data-ttu-id="dd6b6-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd6b6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd6b6-126">-WhatIf</span></span>
<span data-ttu-id="dd6b6-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd6b6-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd6b6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd6b6-129">CommonParameters</span></span>
<span data-ttu-id="dd6b6-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd6b6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd6b6-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd6b6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd6b6-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd6b6-132">INPUTS</span></span>

### <span data-ttu-id="dd6b6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dd6b6-133">System.String</span></span>

## <span data-ttu-id="dd6b6-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd6b6-134">OUTPUTS</span></span>

### <span data-ttu-id="dd6b6-135">System. void</span><span class="sxs-lookup"><span data-stu-id="dd6b6-135">System.Void</span></span>

### <span data-ttu-id="dd6b6-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd6b6-136">System.Boolean</span></span>

## <span data-ttu-id="dd6b6-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd6b6-137">NOTES</span></span>

## <span data-ttu-id="dd6b6-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd6b6-138">RELATED LINKS</span></span>
