---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912904"
---
# <span data-ttu-id="bd837-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bd837-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="bd837-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd837-102">SYNOPSIS</span></span>
<span data-ttu-id="bd837-103">Изменение модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="bd837-103">Modifies a runbook.</span></span>

## <span data-ttu-id="bd837-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd837-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd837-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd837-105">DESCRIPTION</span></span>
<span data-ttu-id="bd837-106">Командлет **Set-AzAutomationRunbook** изменяет конфигурацию Azure Automation RUNBOOK в ТД.</span><span class="sxs-lookup"><span data-stu-id="bd837-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="bd837-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd837-107">EXAMPLES</span></span>

### <span data-ttu-id="bd837-108">Пример 1: включение подробного ведения журнала для модуля Runbook</span><span class="sxs-lookup"><span data-stu-id="bd837-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bd837-109">Эта команда включает подробный журнал для заданий указанного Runbook в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bd837-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="bd837-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd837-110">PARAMETERS</span></span>

### <span data-ttu-id="bd837-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bd837-111">-AutomationAccountName</span></span>
<span data-ttu-id="bd837-112">Указывает имя учетной записи автоматизации, в которой этот командлет изменяет Runbook.</span><span class="sxs-lookup"><span data-stu-id="bd837-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="bd837-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd837-113">-DefaultProfile</span></span>
<span data-ttu-id="bd837-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bd837-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd837-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="bd837-115">-Description</span></span>
<span data-ttu-id="bd837-116">Задает описание для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="bd837-116">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd837-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="bd837-117">-LogProgress</span></span>
<span data-ttu-id="bd837-118">Указывает, выполняется ли журнал Runbook.</span><span class="sxs-lookup"><span data-stu-id="bd837-118">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd837-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="bd837-119">-LogVerbose</span></span>
<span data-ttu-id="bd837-120">Указывает, включаются ли в ведение журнала подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="bd837-120">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd837-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bd837-121">-Name</span></span>
<span data-ttu-id="bd837-122">Указывает имя Runbook, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bd837-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bd837-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd837-123">-ResourceGroupName</span></span>
<span data-ttu-id="bd837-124">Указывает имя группы ресурсов, для которой этот командлет изменяет Runbook.</span><span class="sxs-lookup"><span data-stu-id="bd837-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="bd837-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="bd837-125">-Tag</span></span>
<span data-ttu-id="bd837-126">Теги Runbook.</span><span class="sxs-lookup"><span data-stu-id="bd837-126">The runbook tags.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd837-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd837-127">CommonParameters</span></span>
<span data-ttu-id="bd837-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd837-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd837-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd837-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd837-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd837-130">INPUTS</span></span>

### <span data-ttu-id="bd837-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bd837-131">System.String</span></span>

### <span data-ttu-id="bd837-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="bd837-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="bd837-133">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bd837-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bd837-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd837-134">OUTPUTS</span></span>

### <span data-ttu-id="bd837-135">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="bd837-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="bd837-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd837-136">NOTES</span></span>

## <span data-ttu-id="bd837-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd837-137">RELATED LINKS</span></span>

[<span data-ttu-id="bd837-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bd837-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="bd837-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bd837-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="bd837-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bd837-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="bd837-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bd837-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="bd837-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bd837-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="bd837-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bd837-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="bd837-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bd837-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="bd837-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bd837-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


