---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: d6d233bcd9ac439d163c0b6de6866a0c7dac0b04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509802"
---
# <span data-ttu-id="7566c-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7566c-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="7566c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7566c-102">SYNOPSIS</span></span>
<span data-ttu-id="7566c-103">Удаляет узел DSC из управления учетной записью автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7566c-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="7566c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7566c-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7566c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7566c-105">DESCRIPTION</span></span>
<span data-ttu-id="7566c-106">Для управления учетной записью автоматизации Azure узел APS Desired State Configuration (DSC) удаляется с помощью команды **Unregister-AzAutomationDscNode.**</span><span class="sxs-lookup"><span data-stu-id="7566c-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="7566c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7566c-107">EXAMPLES</span></span>

### <span data-ttu-id="7566c-108">Пример 1. Удаление узла DSC Azure из управления учетной записью автоматизации</span><span class="sxs-lookup"><span data-stu-id="7566c-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="7566c-109">Эта команда удаляет узел DSC, у которого указан GUID, из управления учетной записью автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7566c-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7566c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7566c-110">PARAMETERS</span></span>

### <span data-ttu-id="7566c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7566c-111">-AutomationAccountName</span></span>
<span data-ttu-id="7566c-112">Указывает имя учетной записи автоматизации, из которой этот cmdlet удаляет узел DSC.</span><span class="sxs-lookup"><span data-stu-id="7566c-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="7566c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7566c-113">-DefaultProfile</span></span>
<span data-ttu-id="7566c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7566c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7566c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7566c-115">-Force</span></span>
<span data-ttu-id="7566c-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="7566c-116">ps_force</span></span>

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

### <span data-ttu-id="7566c-117">-Id</span><span class="sxs-lookup"><span data-stu-id="7566c-117">-Id</span></span>
<span data-ttu-id="7566c-118">Указывает уникальный код узла DSC, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7566c-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7566c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7566c-119">-ResourceGroupName</span></span>
<span data-ttu-id="7566c-120">Указывает имя группы ресурсов, в которой этот cmdlet отрегистрирует узел DSC.</span><span class="sxs-lookup"><span data-stu-id="7566c-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="7566c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7566c-121">-Confirm</span></span>
<span data-ttu-id="7566c-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7566c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7566c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7566c-123">-WhatIf</span></span>
<span data-ttu-id="7566c-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7566c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7566c-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7566c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7566c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7566c-126">CommonParameters</span></span>
<span data-ttu-id="7566c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7566c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7566c-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7566c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7566c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7566c-129">INPUTS</span></span>

### <span data-ttu-id="7566c-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7566c-130">System.Guid</span></span>

### <span data-ttu-id="7566c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7566c-131">System.String</span></span>

## <span data-ttu-id="7566c-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7566c-132">OUTPUTS</span></span>

### <span data-ttu-id="7566c-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="7566c-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="7566c-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7566c-134">NOTES</span></span>

## <span data-ttu-id="7566c-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7566c-135">RELATED LINKS</span></span>

[<span data-ttu-id="7566c-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7566c-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="7566c-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7566c-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="7566c-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7566c-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


