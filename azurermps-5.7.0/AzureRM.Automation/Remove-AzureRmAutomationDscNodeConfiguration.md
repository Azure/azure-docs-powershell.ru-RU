---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6C6C7142-31CD-4245-BC55-CB7916EA12E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 662ab70f3bda94e614742043521856d7a3fb99c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570287"
---
# <span data-ttu-id="4283c-101">Remove-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4283c-101">Remove-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="4283c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4283c-102">SYNOPSIS</span></span>
<span data-ttu-id="4283c-103">Удаляет метаданные из конфигураций узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4283c-103">Removes metadata from DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4283c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4283c-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscNodeConfiguration [-Name] <String> [-Force] [-IgnoreNodeMappings]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4283c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4283c-105">DESCRIPTION</span></span>
<span data-ttu-id="4283c-106">Командлет **Remove-AzureRmAutomationDscNodeConfiguration** удаляет метаданные из точек доступа к нужной конфигурации узла (DSC) в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="4283c-106">The **Remove-AzureRmAutomationDscNodeConfiguration** cmdlet removes metadata from APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="4283c-107">Модель автоматизации хранит конфигурацию узла DSC в виде документа конфигурации MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="4283c-107">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="4283c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4283c-108">EXAMPLES</span></span>

## <span data-ttu-id="4283c-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4283c-109">PARAMETERS</span></span>

### <span data-ttu-id="4283c-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4283c-110">-AutomationAccountName</span></span>
<span data-ttu-id="4283c-111">Указывает имя учетной записи автоматизации, которая содержит конфигурации узла DSC, для которых этот командлет удаляет метаданные.</span><span class="sxs-lookup"><span data-stu-id="4283c-111">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet removes metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4283c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4283c-112">-DefaultProfile</span></span>
<span data-ttu-id="4283c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4283c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4283c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4283c-114">-Force</span></span>
<span data-ttu-id="4283c-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="4283c-115">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4283c-116">-IgnoreNodeMappings</span><span class="sxs-lookup"><span data-stu-id="4283c-116">-IgnoreNodeMappings</span></span>
<span data-ttu-id="4283c-117">Указывает на то, что этот командлет не учитывает сопоставления узлов.</span><span class="sxs-lookup"><span data-stu-id="4283c-117">Indicates that this cmdlet ignores node mappings.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4283c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4283c-118">-Name</span></span>
<span data-ttu-id="4283c-119">Указывает имя конфигурации узла DSC, для которого этот командлет удаляет метаданные.</span><span class="sxs-lookup"><span data-stu-id="4283c-119">Specifies the name of the DSC node configuration for which this cmdlet removes metadata.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NodeConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4283c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4283c-120">-ResourceGroupName</span></span>
<span data-ttu-id="4283c-121">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4283c-121">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4283c-122">Этот командлет удаляет метаданные для конфигураций узла DSC в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="4283c-122">This cmdlet removes metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4283c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4283c-123">-Confirm</span></span>
<span data-ttu-id="4283c-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4283c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4283c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4283c-125">-WhatIf</span></span>
<span data-ttu-id="4283c-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4283c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4283c-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4283c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4283c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4283c-128">CommonParameters</span></span>
<span data-ttu-id="4283c-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4283c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4283c-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4283c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4283c-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4283c-131">INPUTS</span></span>

### <span data-ttu-id="4283c-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="4283c-132">None</span></span>
<span data-ttu-id="4283c-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4283c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4283c-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4283c-134">OUTPUTS</span></span>

## <span data-ttu-id="4283c-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="4283c-135">NOTES</span></span>

## <span data-ttu-id="4283c-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4283c-136">RELATED LINKS</span></span>

[<span data-ttu-id="4283c-137">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4283c-137">Get-AzureRmAutomationDscNodeConfiguration</span></span>](./Get-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="4283c-138">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4283c-138">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="4283c-139">Командлеты службы автоматизации Azure</span><span class="sxs-lookup"><span data-stu-id="4283c-139">Azure Automation Cmdlets</span></span>](./AzureRM.Automation.md)


