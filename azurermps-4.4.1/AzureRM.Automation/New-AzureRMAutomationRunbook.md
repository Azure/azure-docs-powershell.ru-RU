---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 664bfb83be4394c5aa50213177eda9f16f5ec6b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565684"
---
# <span data-ttu-id="6d1e9-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6d1e9-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="6d1e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="6d1e9-103">Создает Runbook автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d1e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d1e9-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d1e9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d1e9-105">DESCRIPTION</span></span>
<span data-ttu-id="6d1e9-106">Командлет **New-AzureRmAutomationRunbook** создает пустой Runbook службы автоматизации Azure с помощью ТД.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="6d1e9-107">Укажите имя для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="6d1e9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d1e9-108">EXAMPLES</span></span>

### <span data-ttu-id="6d1e9-109">Пример 1: создание Runbook</span><span class="sxs-lookup"><span data-stu-id="6d1e9-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6d1e9-110">Эта команда создает Runbook с именем Runbook02 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="6d1e9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d1e9-111">PARAMETERS</span></span>

### <span data-ttu-id="6d1e9-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6d1e9-112">-AutomationAccountName</span></span>
<span data-ttu-id="6d1e9-113">Указывает имя учетной записи автоматизации, в которой этот командлет создает Runbook.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="6d1e9-114">-Описание</span><span class="sxs-lookup"><span data-stu-id="6d1e9-114">-Description</span></span>
<span data-ttu-id="6d1e9-115">Задает описание для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-115">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="6d1e9-116">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="6d1e9-116">-LogProgress</span></span>
<span data-ttu-id="6d1e9-117">Указывает, выполняется ли журнал Runbook.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-117">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="6d1e9-118">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="6d1e9-118">-LogVerbose</span></span>
<span data-ttu-id="6d1e9-119">Указывает, включаются ли в ведение журнала подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-119">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="6d1e9-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d1e9-120">-Name</span></span>
<span data-ttu-id="6d1e9-121">Задает имя для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-121">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="6d1e9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d1e9-122">-ResourceGroupName</span></span>
<span data-ttu-id="6d1e9-123">Указывает имя группы ресурсов, для которой этот командлет создает Runbook.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-123">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="6d1e9-124">-Теги</span><span class="sxs-lookup"><span data-stu-id="6d1e9-124">-Tags</span></span>
<span data-ttu-id="6d1e9-125">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6d1e9-126">Например:</span><span class="sxs-lookup"><span data-stu-id="6d1e9-126">For example:</span></span>

<span data-ttu-id="6d1e9-127">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="6d1e9-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6d1e9-128">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="6d1e9-128">-Type</span></span>
<span data-ttu-id="6d1e9-129">Указывает тип Runbook, создаваемый этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-129">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="6d1e9-130">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6d1e9-130">Valid values are:</span></span>

- <span data-ttu-id="6d1e9-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6d1e9-131">PowerShell</span></span>
- <span data-ttu-id="6d1e9-132">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="6d1e9-132">GraphicalPowerShell</span></span>
- <span data-ttu-id="6d1e9-133">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="6d1e9-133">PowerShellWorkflow</span></span>
- <span data-ttu-id="6d1e9-134">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="6d1e9-134">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="6d1e9-135">Виде</span><span class="sxs-lookup"><span data-stu-id="6d1e9-135">Graph</span></span>

<span data-ttu-id="6d1e9-136">Диаграмма значений устарела.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-136">The value Graph is obsolete.</span></span>
<span data-ttu-id="6d1e9-137">Это эквивалентно GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1e9-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d1e9-138">-DefaultProfile</span></span>
<span data-ttu-id="6d1e9-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d1e9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d1e9-140">CommonParameters</span></span>
<span data-ttu-id="6d1e9-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d1e9-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d1e9-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d1e9-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d1e9-143">INPUTS</span></span>

## <span data-ttu-id="6d1e9-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d1e9-144">OUTPUTS</span></span>

### <span data-ttu-id="6d1e9-145">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="6d1e9-145">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="6d1e9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d1e9-146">NOTES</span></span>

## <span data-ttu-id="6d1e9-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d1e9-147">RELATED LINKS</span></span>

[<span data-ttu-id="6d1e9-148">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6d1e9-148">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6d1e9-149">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6d1e9-149">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6d1e9-150">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6d1e9-150">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6d1e9-151">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6d1e9-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6d1e9-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6d1e9-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6d1e9-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6d1e9-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6d1e9-154">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6d1e9-154">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
