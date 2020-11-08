---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247663"
---
# <span data-ttu-id="58c68-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58c68-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="58c68-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58c68-102">SYNOPSIS</span></span>
<span data-ttu-id="58c68-103">Изменение модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="58c68-103">Modifies a runbook.</span></span>

## <span data-ttu-id="58c68-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58c68-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58c68-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58c68-105">DESCRIPTION</span></span>
<span data-ttu-id="58c68-106">Командлет **Set-AzAutomationRunbook** изменяет конфигурацию Azure Automation RUNBOOK в ТД.</span><span class="sxs-lookup"><span data-stu-id="58c68-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="58c68-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58c68-107">EXAMPLES</span></span>

### <span data-ttu-id="58c68-108">Пример 1: включение подробного ведения журнала для модуля Runbook</span><span class="sxs-lookup"><span data-stu-id="58c68-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="58c68-109">Эта команда включает подробный журнал для заданий указанного Runbook в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="58c68-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="58c68-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58c68-110">PARAMETERS</span></span>

### <span data-ttu-id="58c68-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="58c68-111">-AutomationAccountName</span></span>
<span data-ttu-id="58c68-112">Указывает имя учетной записи автоматизации, в которой этот командлет изменяет Runbook.</span><span class="sxs-lookup"><span data-stu-id="58c68-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="58c68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c68-113">-DefaultProfile</span></span>
<span data-ttu-id="58c68-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="58c68-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58c68-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="58c68-115">-Description</span></span>
<span data-ttu-id="58c68-116">Задает описание для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="58c68-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="58c68-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="58c68-117">-LogProgress</span></span>
<span data-ttu-id="58c68-118">Указывает, выполняется ли журнал Runbook.</span><span class="sxs-lookup"><span data-stu-id="58c68-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="58c68-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="58c68-119">-LogVerbose</span></span>
<span data-ttu-id="58c68-120">Указывает, включаются ли в ведение журнала подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="58c68-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="58c68-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58c68-121">-Name</span></span>
<span data-ttu-id="58c68-122">Указывает имя Runbook, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="58c68-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="58c68-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c68-123">-ResourceGroupName</span></span>
<span data-ttu-id="58c68-124">Указывает имя группы ресурсов, для которой этот командлет изменяет Runbook.</span><span class="sxs-lookup"><span data-stu-id="58c68-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="58c68-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="58c68-125">-Tag</span></span>
<span data-ttu-id="58c68-126">Теги Runbook.</span><span class="sxs-lookup"><span data-stu-id="58c68-126">The runbook tags.</span></span>

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

### <span data-ttu-id="58c68-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c68-127">CommonParameters</span></span>
<span data-ttu-id="58c68-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58c68-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c68-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58c68-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c68-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58c68-130">INPUTS</span></span>

### <span data-ttu-id="58c68-131">System. String</span><span class="sxs-lookup"><span data-stu-id="58c68-131">System.String</span></span>

### <span data-ttu-id="58c68-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="58c68-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="58c68-133">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="58c68-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="58c68-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58c68-134">OUTPUTS</span></span>

### <span data-ttu-id="58c68-135">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="58c68-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="58c68-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="58c68-136">NOTES</span></span>

## <span data-ttu-id="58c68-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58c68-137">RELATED LINKS</span></span>

[<span data-ttu-id="58c68-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58c68-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="58c68-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58c68-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="58c68-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58c68-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="58c68-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58c68-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="58c68-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58c68-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="58c68-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58c68-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="58c68-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58c68-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="58c68-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="58c68-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


