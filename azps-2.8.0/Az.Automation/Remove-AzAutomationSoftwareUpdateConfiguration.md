---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 3b608feb9ed496be72d1d74f4a5a2be0569714de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727758"
---
# <span data-ttu-id="edcde-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="edcde-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="edcde-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="edcde-102">SYNOPSIS</span></span>
<span data-ttu-id="edcde-103">Удаляет конфигурацию обновления программного обеспечения Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="edcde-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="edcde-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="edcde-104">SYNTAX</span></span>

### <span data-ttu-id="edcde-105">BySucName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="edcde-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edcde-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="edcde-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edcde-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edcde-107">DESCRIPTION</span></span>
<span data-ttu-id="edcde-108">Этот командлет удалил конфигурацию обновления программного обеспечения Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="edcde-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="edcde-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="edcde-109">EXAMPLES</span></span>

### <span data-ttu-id="edcde-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="edcde-110">Example 1</span></span>
<span data-ttu-id="edcde-111">В этом примере показано, как удалить "MyUpdateConfiguration" из учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="edcde-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="edcde-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="edcde-112">PARAMETERS</span></span>

### <span data-ttu-id="edcde-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="edcde-113">-AutomationAccountName</span></span>
<span data-ttu-id="edcde-114">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="edcde-114">The automation account name.</span></span>

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

### <span data-ttu-id="edcde-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edcde-115">-DefaultProfile</span></span>
<span data-ttu-id="edcde-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="edcde-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edcde-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="edcde-117">-Name</span></span>
<span data-ttu-id="edcde-118">Имя конфигурации обновления программного обеспечения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="edcde-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edcde-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edcde-119">-PassThru</span></span>
<span data-ttu-id="edcde-120">Функция PassThru возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="edcde-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="edcde-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="edcde-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edcde-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edcde-122">-ResourceGroupName</span></span>
<span data-ttu-id="edcde-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="edcde-123">The resource group name.</span></span>

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

### <span data-ttu-id="edcde-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="edcde-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="edcde-125">Конфигурация обновления программного обеспечения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="edcde-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edcde-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edcde-126">-Confirm</span></span>
<span data-ttu-id="edcde-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="edcde-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edcde-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edcde-128">-WhatIf</span></span>
<span data-ttu-id="edcde-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="edcde-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edcde-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="edcde-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edcde-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edcde-131">CommonParameters</span></span>
<span data-ttu-id="edcde-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="edcde-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edcde-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edcde-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edcde-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="edcde-134">INPUTS</span></span>

### <span data-ttu-id="edcde-135">System. String</span><span class="sxs-lookup"><span data-stu-id="edcde-135">System.String</span></span>

### <span data-ttu-id="edcde-136">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="edcde-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="edcde-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="edcde-137">OUTPUTS</span></span>

### <span data-ttu-id="edcde-138">System. void</span><span class="sxs-lookup"><span data-stu-id="edcde-138">System.Void</span></span>

### <span data-ttu-id="edcde-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="edcde-139">System.Boolean</span></span>

## <span data-ttu-id="edcde-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="edcde-140">NOTES</span></span>

## <span data-ttu-id="edcde-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edcde-141">RELATED LINKS</span></span>
