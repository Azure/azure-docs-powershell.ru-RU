---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 02a6d7a129dc084b982f1827d678354265ddbc66
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509869"
---
# <span data-ttu-id="4e392-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4e392-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="4e392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e392-102">SYNOPSIS</span></span>
<span data-ttu-id="4e392-103">Изменяет конфигурацию узла, с которую соедует узел DSC.</span><span class="sxs-lookup"><span data-stu-id="4e392-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="4e392-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e392-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e392-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e392-105">DESCRIPTION</span></span>
<span data-ttu-id="4e392-106">**Cmdlet Set-AzAutomationDscNode** изменяет конфигурацию узла APS Desired State Configuration (DSC).</span><span class="sxs-lookup"><span data-stu-id="4e392-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="4e392-107">Azure Automation хранит конфигурацию узла DSC в документе конфигурации "Управляемый формат объекта" (MOF).</span><span class="sxs-lookup"><span data-stu-id="4e392-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="4e392-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e392-108">EXAMPLES</span></span>

### <span data-ttu-id="4e392-109">Пример 1. Изменение сопоставления конфигурации узла</span><span class="sxs-lookup"><span data-stu-id="4e392-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="4e392-110">Эта команда назначает конфигурацию узла с именем Contoso.NodeConfiguration01 узлу с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="4e392-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="4e392-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e392-111">PARAMETERS</span></span>

### <span data-ttu-id="4e392-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4e392-112">-AutomationAccountName</span></span>
<span data-ttu-id="4e392-113">Указывает имя учетной записи автоматизации, которая содержит узел DSC, для которого этот cmdlet изменяет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="4e392-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="4e392-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e392-114">-DefaultProfile</span></span>
<span data-ttu-id="4e392-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4e392-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e392-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4e392-116">-Force</span></span>
<span data-ttu-id="4e392-117">ps_force выполнить команду без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4e392-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4e392-118">-Id</span><span class="sxs-lookup"><span data-stu-id="4e392-118">-Id</span></span>
<span data-ttu-id="4e392-119">Указывает уникальный код узла DSC, для которого этот cmdlet изменяет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="4e392-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="4e392-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4e392-120">-NodeConfigurationName</span></span>
<span data-ttu-id="4e392-121">Указывает имя конфигурации узла, в которой этот cmdlet сопоирует узел.</span><span class="sxs-lookup"><span data-stu-id="4e392-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

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

### <span data-ttu-id="4e392-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e392-122">-ResourceGroupName</span></span>
<span data-ttu-id="4e392-123">Указывает имя группы ресурсов, в которой этот cmdlet изменяет конфигурацию узла DSC.</span><span class="sxs-lookup"><span data-stu-id="4e392-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="4e392-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e392-124">-Confirm</span></span>
<span data-ttu-id="4e392-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e392-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e392-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e392-126">-WhatIf</span></span>
<span data-ttu-id="4e392-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e392-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e392-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4e392-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e392-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e392-129">CommonParameters</span></span>
<span data-ttu-id="4e392-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e392-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e392-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e392-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e392-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e392-132">INPUTS</span></span>

### <span data-ttu-id="4e392-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4e392-133">System.Guid</span></span>

### <span data-ttu-id="4e392-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4e392-134">System.String</span></span>

## <span data-ttu-id="4e392-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e392-135">OUTPUTS</span></span>

### <span data-ttu-id="4e392-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="4e392-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="4e392-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e392-137">NOTES</span></span>

## <span data-ttu-id="4e392-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e392-138">RELATED LINKS</span></span>

[<span data-ttu-id="4e392-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4e392-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="4e392-140">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4e392-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="4e392-141">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4e392-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


