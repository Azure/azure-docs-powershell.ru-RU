---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: e0e74aa910c11a10c26cf6bed623d2e2c02f93ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561179"
---
# <span data-ttu-id="74410-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="74410-101">Remove-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="74410-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74410-102">SYNOPSIS</span></span>
<span data-ttu-id="74410-103">Удаляет конфигурацию обновления программного обеспечения Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="74410-103">Removes an azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74410-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74410-104">SYNTAX</span></span>

### <span data-ttu-id="74410-105">BySucName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74410-105">BySucName (Default)</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74410-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="74410-106">BySuc</span></span>
```
Remove-AzureRmAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74410-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74410-107">DESCRIPTION</span></span>
<span data-ttu-id="74410-108">Этот командлет удалил конфигурацию обновления программного обеспечения Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="74410-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="74410-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74410-109">EXAMPLES</span></span>

### <span data-ttu-id="74410-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74410-110">Example 1</span></span>
<span data-ttu-id="74410-111">В этом примере показано, как удалить "MyUpdateConfiguration" из учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="74410-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="74410-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74410-112">PARAMETERS</span></span>

### <span data-ttu-id="74410-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="74410-113">-AutomationAccountName</span></span>
<span data-ttu-id="74410-114">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="74410-114">The automation account name.</span></span>

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

### <span data-ttu-id="74410-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74410-115">-DefaultProfile</span></span>
<span data-ttu-id="74410-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74410-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74410-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74410-117">-Name</span></span>
<span data-ttu-id="74410-118">Имя конфигурации обновления программного обеспечения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="74410-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="74410-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74410-119">-PassThru</span></span>
<span data-ttu-id="74410-120">Функция PassThru возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="74410-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="74410-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="74410-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="74410-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74410-122">-ResourceGroupName</span></span>
<span data-ttu-id="74410-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="74410-123">The resource group name.</span></span>

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

### <span data-ttu-id="74410-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="74410-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="74410-125">Конфигурация обновления программного обеспечения, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="74410-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="74410-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74410-126">-Confirm</span></span>
<span data-ttu-id="74410-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74410-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74410-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74410-128">-WhatIf</span></span>
<span data-ttu-id="74410-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74410-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74410-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74410-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74410-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74410-131">CommonParameters</span></span>
<span data-ttu-id="74410-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74410-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74410-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74410-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74410-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74410-134">INPUTS</span></span>

### <span data-ttu-id="74410-135">System. String</span><span class="sxs-lookup"><span data-stu-id="74410-135">System.String</span></span>

### <span data-ttu-id="74410-136">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="74410-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="74410-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74410-137">OUTPUTS</span></span>

### <span data-ttu-id="74410-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="74410-138">System.Object</span></span>
## <span data-ttu-id="74410-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="74410-139">NOTES</span></span>

## <span data-ttu-id="74410-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74410-140">RELATED LINKS</span></span>
