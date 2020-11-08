---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 16e0f858b11e98df3599a568805e72f7ae8f6a8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242639"
---
# <span data-ttu-id="c276d-101">Remove-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c276d-101">Remove-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="c276d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c276d-102">SYNOPSIS</span></span>
<span data-ttu-id="c276d-103">Удаляет метаданные из конфигураций узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c276d-103">Removes metadata from DSC node configurations in Automation.</span></span>

## <span data-ttu-id="c276d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c276d-104">SYNTAX</span></span>

```
Remove-AzAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c276d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c276d-105">DESCRIPTION</span></span>
<span data-ttu-id="c276d-106">Командлет **Remove-AzAutomationDscNodeConfiguration** удаляет метаданные из точек доступа к нужной конфигурации узла (DSC) в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="c276d-106">The **Remove-AzAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="c276d-107">Модель автоматизации хранит конфигурацию узла DSC в виде документа конфигурации MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="c276d-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="c276d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c276d-108">EXAMPLES</span></span>

### <span data-ttu-id="c276d-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c276d-109">Example 1</span></span>

<span data-ttu-id="c276d-110">Удаляет метаданные из конфигураций узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c276d-110">Removes metadata from DSC node configurations in Automation.</span></span> <span data-ttu-id="c276d-111">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="c276d-111">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Remove-AzAutomationDscNodeConfiguration -AutomationAccountName 'AutomationAccount01' -IgnoreNodeMappings -Name 'Configuration01' -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="c276d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c276d-112">PARAMETERS</span></span>

### <span data-ttu-id="c276d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c276d-113">-AutomationAccountName</span></span>
<span data-ttu-id="c276d-114">Указывает имя учетной записи автоматизации, которая содержит конфигурации узла DSC, для которых этот командлет удаляет метаданные.</span><span class="sxs-lookup"><span data-stu-id="c276d-114">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="c276d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c276d-115">-DefaultProfile</span></span>
<span data-ttu-id="c276d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c276d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c276d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c276d-117">-Force</span></span>
<span data-ttu-id="c276d-118">ps_force</span><span class="sxs-lookup"><span data-stu-id="c276d-118">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c276d-119">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="c276d-119">-IgnoreNodeMappings</span></span>
<span data-ttu-id="c276d-120">Указывает на то, что этот командлет не учитывает сопоставления узлов.</span><span class="sxs-lookup"><span data-stu-id="c276d-120">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c276d-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c276d-121">-Name</span></span>
<span data-ttu-id="c276d-122">Указывает имя конфигурации узла DSC, для которого этот командлет удаляет метаданные.</span><span class="sxs-lookup"><span data-stu-id="c276d-122">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c276d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c276d-123">-ResourceGroupName</span></span>
<span data-ttu-id="c276d-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c276d-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c276d-125">Этот командлет удаляет метаданные для конфигураций узла DSC в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="c276d-125">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c276d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c276d-126">-Confirm</span></span>
<span data-ttu-id="c276d-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c276d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c276d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c276d-128">-WhatIf</span></span>
<span data-ttu-id="c276d-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c276d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c276d-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c276d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c276d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c276d-131">CommonParameters</span></span>
<span data-ttu-id="c276d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c276d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c276d-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c276d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c276d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c276d-134">INPUTS</span></span>

### <span data-ttu-id="c276d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c276d-135">System.String</span></span>

## <span data-ttu-id="c276d-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c276d-136">OUTPUTS</span></span>

### <span data-ttu-id="c276d-137">System. void</span><span class="sxs-lookup"><span data-stu-id="c276d-137">System.Void</span></span>

## <span data-ttu-id="c276d-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c276d-138">NOTES</span></span>

## <span data-ttu-id="c276d-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c276d-139">RELATED LINKS</span></span>

[<span data-ttu-id="c276d-140">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c276d-140">Get-AzAutomationDscNodeConfiguration</span></span>](./Get-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="c276d-141">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c276d-141">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="c276d-142">Командлеты службы автоматизации Azure</span><span class="sxs-lookup"><span data-stu-id="c276d-142">Azure Automation Cmdlets</span></span>](/powershell/module/Az.Automation/)