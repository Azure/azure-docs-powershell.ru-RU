---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: bd5e51b8951d2b246036b45ddddf3d1bbe4b8e4e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239517"
---
# <span data-ttu-id="8f4ba-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f4ba-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="8f4ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f4ba-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4ba-103">Удаляет конфигурацию обновления программного обеспечения автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="8f4ba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8f4ba-104">SYNTAX</span></span>

### <span data-ttu-id="8f4ba-105">BySucName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f4ba-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f4ba-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="8f4ba-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f4ba-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f4ba-107">DESCRIPTION</span></span>
<span data-ttu-id="8f4ba-108">Этот cmdlet удалил конфигурацию обновления программного обеспечения автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="8f4ba-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8f4ba-109">EXAMPLES</span></span>

### <span data-ttu-id="8f4ba-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f4ba-110">Example 1</span></span>
<span data-ttu-id="8f4ba-111">В этом примере показано, как удалить myUpdateConfiguration из учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="8f4ba-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="8f4ba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f4ba-112">PARAMETERS</span></span>

### <span data-ttu-id="8f4ba-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8f4ba-113">-AutomationAccountName</span></span>
<span data-ttu-id="8f4ba-114">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-114">The automation account name.</span></span>

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

### <span data-ttu-id="8f4ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4ba-115">-DefaultProfile</span></span>
<span data-ttu-id="8f4ba-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f4ba-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8f4ba-117">-Name</span></span>
<span data-ttu-id="8f4ba-118">Имя конфигурации обновления программного обеспечения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="8f4ba-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f4ba-119">-PassThru</span></span>
<span data-ttu-id="8f4ba-120">PassThru возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8f4ba-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8f4ba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f4ba-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f4ba-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-123">The resource group name.</span></span>

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

### <span data-ttu-id="8f4ba-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f4ba-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="8f4ba-125">Конфигурация обновления программного обеспечения, удаляемая.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="8f4ba-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f4ba-126">-Confirm</span></span>
<span data-ttu-id="8f4ba-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f4ba-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f4ba-128">-WhatIf</span></span>
<span data-ttu-id="8f4ba-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f4ba-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f4ba-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4ba-131">CommonParameters</span></span>
<span data-ttu-id="8f4ba-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f4ba-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4ba-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f4ba-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4ba-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f4ba-134">INPUTS</span></span>

### <span data-ttu-id="8f4ba-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8f4ba-135">System.String</span></span>

### <span data-ttu-id="8f4ba-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f4ba-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="8f4ba-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f4ba-137">OUTPUTS</span></span>

### <span data-ttu-id="8f4ba-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="8f4ba-138">System.Void</span></span>

### <span data-ttu-id="8f4ba-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f4ba-139">System.Boolean</span></span>

## <span data-ttu-id="8f4ba-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8f4ba-140">NOTES</span></span>

## <span data-ttu-id="8f4ba-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f4ba-141">RELATED LINKS</span></span>
