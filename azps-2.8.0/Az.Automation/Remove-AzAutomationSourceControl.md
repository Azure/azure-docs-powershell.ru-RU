---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSourceControl.md
ms.openlocfilehash: 165850e0212969fea76e85f209d3fcf7c2040b79
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727757"
---
# <span data-ttu-id="72326-101">Remove-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="72326-101">Remove-AzAutomationSourceControl</span></span>

## <span data-ttu-id="72326-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72326-102">SYNOPSIS</span></span>
<span data-ttu-id="72326-103">Удаляет элемент управления источником автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="72326-103">Removes an Azure Automation source control.</span></span>

## <span data-ttu-id="72326-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72326-104">SYNTAX</span></span>

```
Remove-AzAutomationSourceControl [-Name] <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72326-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72326-105">DESCRIPTION</span></span>
<span data-ttu-id="72326-106">Командлет Remove-AzAutomationSourceControl удаляет исходный элемент управления из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="72326-106">The Remove-AzAutomationSourceControl cmdlet removes a source control from Azure Automation.</span></span>

## <span data-ttu-id="72326-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72326-107">EXAMPLES</span></span>

### <span data-ttu-id="72326-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="72326-108">Example 1</span></span>
<span data-ttu-id="72326-109">Эта команда удаляет элемент управления источником автоматизации с именем VSTSNative в учетной записи с именем devAccount.</span><span class="sxs-lookup"><span data-stu-id="72326-109">This command removes the Automation source control named VSTSNative in the account named devAccount.</span></span>
<span data-ttu-id="72326-110">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="72326-110">This command specifies the *Force* parameter.</span></span> <span data-ttu-id="72326-111">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="72326-111">Therefore, it does not prompt you for confirmation.</span></span>

```powershell
PS C:\> Remove-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                              -AutomationAccountName "devAccount" `
                                              -Name "VSTSNative" `
                                              -Force
```

## <span data-ttu-id="72326-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72326-112">PARAMETERS</span></span>

### <span data-ttu-id="72326-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="72326-113">-AutomationAccountName</span></span>
<span data-ttu-id="72326-114">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="72326-114">The automation account name.</span></span>

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

### <span data-ttu-id="72326-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72326-115">-DefaultProfile</span></span>
<span data-ttu-id="72326-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72326-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72326-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="72326-117">-Name</span></span>
<span data-ttu-id="72326-118">Имя исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="72326-118">The source control name.</span></span>

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

### <span data-ttu-id="72326-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72326-119">-PassThru</span></span>
<span data-ttu-id="72326-120">Функция PassThru возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="72326-120">PassThru returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="72326-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="72326-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="72326-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72326-122">-ResourceGroupName</span></span>
<span data-ttu-id="72326-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72326-123">The resource group name.</span></span>

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

### <span data-ttu-id="72326-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72326-124">-Confirm</span></span>
<span data-ttu-id="72326-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="72326-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72326-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72326-126">-WhatIf</span></span>
<span data-ttu-id="72326-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="72326-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72326-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="72326-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72326-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72326-129">CommonParameters</span></span>
<span data-ttu-id="72326-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72326-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72326-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72326-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72326-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72326-132">INPUTS</span></span>

### <span data-ttu-id="72326-133">System. String</span><span class="sxs-lookup"><span data-stu-id="72326-133">System.String</span></span>

## <span data-ttu-id="72326-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72326-134">OUTPUTS</span></span>

### <span data-ttu-id="72326-135">System. void</span><span class="sxs-lookup"><span data-stu-id="72326-135">System.Void</span></span>

### <span data-ttu-id="72326-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72326-136">System.Boolean</span></span>

## <span data-ttu-id="72326-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="72326-137">NOTES</span></span>

## <span data-ttu-id="72326-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72326-138">RELATED LINKS</span></span>
