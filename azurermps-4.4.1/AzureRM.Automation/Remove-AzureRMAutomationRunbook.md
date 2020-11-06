---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: 96a82f4cc39952517bf5cfaeca24191cc4dd2d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566321"
---
# <span data-ttu-id="f8ed6-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ed6-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="f8ed6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ed6-103">Удаление модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8ed6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8ed6-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8ed6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8ed6-105">DESCRIPTION</span></span>
<span data-ttu-id="f8ed6-106">Командлет **Remove-AzureRmAutomationRunbook** удаляет Runbook из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="f8ed6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8ed6-107">EXAMPLES</span></span>

### <span data-ttu-id="f8ed6-108">Пример 1: удаление Runbook</span><span class="sxs-lookup"><span data-stu-id="f8ed6-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f8ed6-109">Эта команда удаляет Runbook с именем Runbook03 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f8ed6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8ed6-110">PARAMETERS</span></span>

### <span data-ttu-id="f8ed6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f8ed6-111">-AutomationAccountName</span></span>
<span data-ttu-id="f8ed6-112">Указывает имя учетной записи автоматизации, в которой этот командлет удаляет Runbook.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="f8ed6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f8ed6-113">-Force</span></span>
<span data-ttu-id="f8ed6-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="f8ed6-114">ps_force</span></span>

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

### <span data-ttu-id="f8ed6-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f8ed6-115">-Name</span></span>
<span data-ttu-id="f8ed6-116">Указывает имя Runbook, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-116">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8ed6-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8ed6-118">Указывает имя группы ресурсов, для которой этот командлет публикует Runbook.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="f8ed6-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8ed6-119">-Confirm</span></span>
<span data-ttu-id="f8ed6-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8ed6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8ed6-121">-WhatIf</span></span>
<span data-ttu-id="f8ed6-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8ed6-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8ed6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ed6-124">-DefaultProfile</span></span>
<span data-ttu-id="f8ed6-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8ed6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ed6-126">CommonParameters</span></span>
<span data-ttu-id="f8ed6-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8ed6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ed6-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ed6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ed6-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8ed6-129">INPUTS</span></span>

## <span data-ttu-id="f8ed6-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8ed6-130">OUTPUTS</span></span>

## <span data-ttu-id="f8ed6-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8ed6-131">NOTES</span></span>

## <span data-ttu-id="f8ed6-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8ed6-132">RELATED LINKS</span></span>

[<span data-ttu-id="f8ed6-133">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ed6-133">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8ed6-134">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ed6-134">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8ed6-135">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ed6-135">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8ed6-136">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ed6-136">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8ed6-137">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ed6-137">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8ed6-138">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ed6-138">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8ed6-139">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ed6-139">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="f8ed6-140">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="f8ed6-140">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


