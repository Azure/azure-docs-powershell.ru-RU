---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 5aa70f15b5f542b36420e5f8df1cc65bb5dbd09a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004728"
---
# <span data-ttu-id="3840a-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3840a-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="3840a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3840a-102">SYNOPSIS</span></span>
<span data-ttu-id="3840a-103">Изменяет конфигурацию узла, с чем соедует узел DSC.</span><span class="sxs-lookup"><span data-stu-id="3840a-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="3840a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3840a-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3840a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3840a-105">DESCRIPTION</span></span>
<span data-ttu-id="3840a-106">**Cmdlet Set-AzAutomationDscNode** изменяет конфигурацию узла APS Desired State Configuration (DSC).</span><span class="sxs-lookup"><span data-stu-id="3840a-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="3840a-107">Azure Automation хранит конфигурацию узла DSC в документе конфигурации "Управляемый формат объекта" (MOF).</span><span class="sxs-lookup"><span data-stu-id="3840a-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="3840a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3840a-108">EXAMPLES</span></span>

### <span data-ttu-id="3840a-109">Пример 1. Изменение сопоставления конфигурации узла</span><span class="sxs-lookup"><span data-stu-id="3840a-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="3840a-110">Эта команда назначает конфигурацию узла с именем Contoso.NodeConfiguration01 узлу с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="3840a-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="3840a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3840a-111">PARAMETERS</span></span>

### <span data-ttu-id="3840a-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3840a-112">-AutomationAccountName</span></span>
<span data-ttu-id="3840a-113">Указывает имя учетной записи автоматизации, которая содержит узел DSC, для которого этот cmdlet изменяет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="3840a-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="3840a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3840a-114">-DefaultProfile</span></span>
<span data-ttu-id="3840a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3840a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3840a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3840a-116">-Force</span></span>
<span data-ttu-id="3840a-117">ps_force выполнить команду без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="3840a-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3840a-118">-Id</span><span class="sxs-lookup"><span data-stu-id="3840a-118">-Id</span></span>
<span data-ttu-id="3840a-119">Указывает уникальный код узла DSC, для которого этот cmdlet изменяет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="3840a-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3840a-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3840a-120">-NodeConfigurationName</span></span>
<span data-ttu-id="3840a-121">Указывает имя конфигурации узла, в которой этот cmdlet сопоирует узел.</span><span class="sxs-lookup"><span data-stu-id="3840a-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3840a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3840a-122">-ResourceGroupName</span></span>
<span data-ttu-id="3840a-123">Указывает имя группы ресурсов, в которой этот cmdlet изменяет конфигурацию узла DSC.</span><span class="sxs-lookup"><span data-stu-id="3840a-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="3840a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3840a-124">-Confirm</span></span>
<span data-ttu-id="3840a-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3840a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3840a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3840a-126">-WhatIf</span></span>
<span data-ttu-id="3840a-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3840a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3840a-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3840a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3840a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3840a-129">CommonParameters</span></span>
<span data-ttu-id="3840a-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3840a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3840a-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3840a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3840a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3840a-132">INPUTS</span></span>

### <span data-ttu-id="3840a-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3840a-133">System.Guid</span></span>

### <span data-ttu-id="3840a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3840a-134">System.String</span></span>

## <span data-ttu-id="3840a-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3840a-135">OUTPUTS</span></span>

### <span data-ttu-id="3840a-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="3840a-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="3840a-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3840a-137">NOTES</span></span>

## <span data-ttu-id="3840a-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3840a-138">RELATED LINKS</span></span>

[<span data-ttu-id="3840a-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3840a-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="3840a-140">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3840a-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="3840a-141">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3840a-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


