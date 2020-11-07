---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
ms.openlocfilehash: bbf86c6744e064b2958acaf5fe7928d537548805
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731564"
---
# <span data-ttu-id="2d758-101">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d758-101">New-AzAutomationRunbook</span></span>

## <span data-ttu-id="2d758-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d758-102">SYNOPSIS</span></span>
<span data-ttu-id="2d758-103">Создает Runbook автоматизации.</span><span class="sxs-lookup"><span data-stu-id="2d758-103">Creates an Automation runbook.</span></span>

## <span data-ttu-id="2d758-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d758-104">SYNTAX</span></span>

```
New-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d758-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d758-105">DESCRIPTION</span></span>
<span data-ttu-id="2d758-106">Командлет **New-AzAutomationRunbook** создает пустой Runbook службы автоматизации Azure с помощью ТД.</span><span class="sxs-lookup"><span data-stu-id="2d758-106">The **New-AzAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="2d758-107">Укажите имя для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="2d758-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="2d758-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d758-108">EXAMPLES</span></span>

### <span data-ttu-id="2d758-109">Пример 1: создание Runbook</span><span class="sxs-lookup"><span data-stu-id="2d758-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2d758-110">Эта команда создает Runbook с именем Runbook02 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2d758-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="2d758-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d758-111">PARAMETERS</span></span>

### <span data-ttu-id="2d758-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2d758-112">-AutomationAccountName</span></span>
<span data-ttu-id="2d758-113">Указывает имя учетной записи автоматизации, в которой этот командлет создает Runbook.</span><span class="sxs-lookup"><span data-stu-id="2d758-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="2d758-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d758-114">-DefaultProfile</span></span>
<span data-ttu-id="2d758-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2d758-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d758-116">-Описание</span><span class="sxs-lookup"><span data-stu-id="2d758-116">-Description</span></span>
<span data-ttu-id="2d758-117">Задает описание для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="2d758-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="2d758-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="2d758-118">-LogProgress</span></span>
<span data-ttu-id="2d758-119">Указывает, выполняется ли журнал Runbook.</span><span class="sxs-lookup"><span data-stu-id="2d758-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="2d758-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="2d758-120">-LogVerbose</span></span>
<span data-ttu-id="2d758-121">Указывает, включаются ли в ведение журнала подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="2d758-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="2d758-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d758-122">-Name</span></span>
<span data-ttu-id="2d758-123">Задает имя для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="2d758-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="2d758-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d758-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d758-125">Указывает имя группы ресурсов, для которой этот командлет создает Runbook.</span><span class="sxs-lookup"><span data-stu-id="2d758-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="2d758-126">-Теги</span><span class="sxs-lookup"><span data-stu-id="2d758-126">-Tags</span></span>
<span data-ttu-id="2d758-127">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2d758-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2d758-128">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2d758-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d758-129">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="2d758-129">-Type</span></span>
<span data-ttu-id="2d758-130">Указывает тип Runbook, создаваемый этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2d758-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="2d758-131">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2d758-131">Valid values are:</span></span>
- <span data-ttu-id="2d758-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2d758-132">PowerShell</span></span>
- <span data-ttu-id="2d758-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="2d758-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="2d758-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="2d758-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="2d758-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="2d758-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="2d758-136">Виде</span><span class="sxs-lookup"><span data-stu-id="2d758-136">Graph</span></span>
- <span data-ttu-id="2d758-137">Python2 значение графика устарело.</span><span class="sxs-lookup"><span data-stu-id="2d758-137">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="2d758-138">Это эквивалентно GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="2d758-138">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d758-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d758-139">CommonParameters</span></span>
<span data-ttu-id="2d758-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d758-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d758-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d758-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d758-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d758-142">INPUTS</span></span>

### <span data-ttu-id="2d758-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2d758-143">System.String</span></span>

### <span data-ttu-id="2d758-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="2d758-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="2d758-145">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2d758-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2d758-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d758-146">OUTPUTS</span></span>

### <span data-ttu-id="2d758-147">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="2d758-147">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="2d758-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d758-148">NOTES</span></span>

## <span data-ttu-id="2d758-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d758-149">RELATED LINKS</span></span>

[<span data-ttu-id="2d758-150">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d758-150">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="2d758-151">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d758-151">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="2d758-152">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d758-152">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="2d758-153">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d758-153">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="2d758-154">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d758-154">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="2d758-155">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d758-155">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="2d758-156">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d758-156">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
