---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 938fde14fb62ea7f7fd4e04baf5e309615957799
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731531"
---
# <span data-ttu-id="2fdbf-101">Remove-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fdbf-101">Remove-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="2fdbf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fdbf-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdbf-103">Удаляет метаданные из конфигураций узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-103">Removes metadata from DSC node configurations in Automation.</span></span>

## <span data-ttu-id="2fdbf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fdbf-104">SYNTAX</span></span>

```
Remove-AzAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fdbf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fdbf-105">DESCRIPTION</span></span>
<span data-ttu-id="2fdbf-106">Командлет **Remove-AzAutomationDscNodeConfiguration** удаляет метаданные из точек доступа к нужной конфигурации узла (DSC) в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-106">The **Remove-AzAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="2fdbf-107">Модель автоматизации хранит конфигурацию узла DSC в виде документа конфигурации MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="2fdbf-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="2fdbf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fdbf-108">EXAMPLES</span></span>

## <span data-ttu-id="2fdbf-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fdbf-109">PARAMETERS</span></span>

### <span data-ttu-id="2fdbf-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2fdbf-110">-AutomationAccountName</span></span>
<span data-ttu-id="2fdbf-111">Указывает имя учетной записи автоматизации, которая содержит конфигурации узла DSC, для которых этот командлет удаляет метаданные.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="2fdbf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fdbf-112">-DefaultProfile</span></span>
<span data-ttu-id="2fdbf-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2fdbf-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fdbf-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2fdbf-114">-Force</span></span>
<span data-ttu-id="2fdbf-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="2fdbf-115">ps_force</span></span>

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

### <span data-ttu-id="2fdbf-116">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="2fdbf-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="2fdbf-117">Указывает на то, что этот командлет не учитывает сопоставления узлов.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-117">Indicates that this cmdlet ignores node mappings.</span></span>

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

### <span data-ttu-id="2fdbf-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2fdbf-118">-Name</span></span>
<span data-ttu-id="2fdbf-119">Указывает имя конфигурации узла DSC, для которого этот командлет удаляет метаданные.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

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

### <span data-ttu-id="2fdbf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fdbf-120">-ResourceGroupName</span></span>
<span data-ttu-id="2fdbf-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2fdbf-122">Этот командлет удаляет метаданные для конфигураций узла DSC в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2fdbf-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fdbf-123">-Confirm</span></span>
<span data-ttu-id="2fdbf-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fdbf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fdbf-125">-WhatIf</span></span>
<span data-ttu-id="2fdbf-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fdbf-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fdbf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdbf-128">CommonParameters</span></span>
<span data-ttu-id="2fdbf-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fdbf-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fdbf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdbf-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fdbf-131">INPUTS</span></span>

### <span data-ttu-id="2fdbf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2fdbf-132">System.String</span></span>

## <span data-ttu-id="2fdbf-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fdbf-133">OUTPUTS</span></span>

### <span data-ttu-id="2fdbf-134">System. void</span><span class="sxs-lookup"><span data-stu-id="2fdbf-134">System.Void</span></span>

## <span data-ttu-id="2fdbf-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fdbf-135">NOTES</span></span>

## <span data-ttu-id="2fdbf-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fdbf-136">RELATED LINKS</span></span>

[<span data-ttu-id="2fdbf-137">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fdbf-137">Get-AzAutomationDscNodeConfiguration</span></span>](./Get-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="2fdbf-138">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fdbf-138">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="2fdbf-139">Командлеты службы автоматизации Azure</span><span class="sxs-lookup"><span data-stu-id="2fdbf-139">Azure Automation Cmdlets</span></span>](./Az.Automation.md)


