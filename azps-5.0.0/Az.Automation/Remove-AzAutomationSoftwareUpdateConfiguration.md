---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: bd5e51b8951d2b246036b45ddddf3d1bbe4b8e4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246825"
---
# <span data-ttu-id="339ce-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="339ce-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="339ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="339ce-102">SYNOPSIS</span></span>
<span data-ttu-id="339ce-103">Удаляет конфигурацию обновления программного обеспечения Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="339ce-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="339ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="339ce-104">SYNTAX</span></span>

### <span data-ttu-id="339ce-105">BySucName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="339ce-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="339ce-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="339ce-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="339ce-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="339ce-107">DESCRIPTION</span></span>
<span data-ttu-id="339ce-108">Этот командлет удалил конфигурацию обновления программного обеспечения Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="339ce-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="339ce-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="339ce-109">EXAMPLES</span></span>

### <span data-ttu-id="339ce-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="339ce-110">Example 1</span></span>
<span data-ttu-id="339ce-111">В этом примере показано, как удалить "MyUpdateConfiguration" из учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="339ce-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="339ce-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="339ce-112">PARAMETERS</span></span>

### <span data-ttu-id="339ce-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="339ce-113">-AutomationAccountName</span></span>
<span data-ttu-id="339ce-114">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="339ce-114">The automation account name.</span></span>

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

### <span data-ttu-id="339ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339ce-115">-DefaultProfile</span></span>
<span data-ttu-id="339ce-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="339ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="339ce-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="339ce-117">-Name</span></span>
<span data-ttu-id="339ce-118">Имя конфигурации обновления программного обеспечения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="339ce-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="339ce-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="339ce-119">-PassThru</span></span>
<span data-ttu-id="339ce-120">Функция PassThru возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="339ce-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="339ce-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="339ce-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="339ce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339ce-122">-ResourceGroupName</span></span>
<span data-ttu-id="339ce-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="339ce-123">The resource group name.</span></span>

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

### <span data-ttu-id="339ce-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="339ce-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="339ce-125">Конфигурация обновления программного обеспечения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="339ce-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="339ce-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="339ce-126">-Confirm</span></span>
<span data-ttu-id="339ce-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="339ce-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="339ce-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="339ce-128">-WhatIf</span></span>
<span data-ttu-id="339ce-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="339ce-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="339ce-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="339ce-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="339ce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339ce-131">CommonParameters</span></span>
<span data-ttu-id="339ce-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="339ce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339ce-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="339ce-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339ce-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="339ce-134">INPUTS</span></span>

### <span data-ttu-id="339ce-135">System. String</span><span class="sxs-lookup"><span data-stu-id="339ce-135">System.String</span></span>

### <span data-ttu-id="339ce-136">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="339ce-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="339ce-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="339ce-137">OUTPUTS</span></span>

### <span data-ttu-id="339ce-138">System. void</span><span class="sxs-lookup"><span data-stu-id="339ce-138">System.Void</span></span>

### <span data-ttu-id="339ce-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="339ce-139">System.Boolean</span></span>

## <span data-ttu-id="339ce-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="339ce-140">NOTES</span></span>

## <span data-ttu-id="339ce-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="339ce-141">RELATED LINKS</span></span>
