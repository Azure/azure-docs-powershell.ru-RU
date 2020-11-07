---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 77c089e4ab46972892a7fe9ad3cc519dc7f20551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734190"
---
# <span data-ttu-id="30c67-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30c67-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="30c67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30c67-102">SYNOPSIS</span></span>
<span data-ttu-id="30c67-103">Создает Runbook автоматизации.</span><span class="sxs-lookup"><span data-stu-id="30c67-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30c67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30c67-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30c67-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30c67-105">DESCRIPTION</span></span>
<span data-ttu-id="30c67-106">Командлет **New-AzureRmAutomationRunbook** создает пустой Runbook службы автоматизации Azure с помощью ТД.</span><span class="sxs-lookup"><span data-stu-id="30c67-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="30c67-107">Укажите имя для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="30c67-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="30c67-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30c67-108">EXAMPLES</span></span>

### <span data-ttu-id="30c67-109">Пример 1: создание Runbook</span><span class="sxs-lookup"><span data-stu-id="30c67-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="30c67-110">Эта команда создает Runbook с именем Runbook02 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="30c67-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="30c67-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30c67-111">PARAMETERS</span></span>

### <span data-ttu-id="30c67-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="30c67-112">-AutomationAccountName</span></span>
<span data-ttu-id="30c67-113">Указывает имя учетной записи автоматизации, в которой этот командлет создает Runbook.</span><span class="sxs-lookup"><span data-stu-id="30c67-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="30c67-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c67-114">-DefaultProfile</span></span>
<span data-ttu-id="30c67-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="30c67-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30c67-116">-Описание</span><span class="sxs-lookup"><span data-stu-id="30c67-116">-Description</span></span>
<span data-ttu-id="30c67-117">Задает описание для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="30c67-117">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30c67-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="30c67-118">-LogProgress</span></span>
<span data-ttu-id="30c67-119">Указывает, выполняется ли журнал Runbook.</span><span class="sxs-lookup"><span data-stu-id="30c67-119">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30c67-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="30c67-120">-LogVerbose</span></span>
<span data-ttu-id="30c67-121">Указывает, включаются ли в ведение журнала подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="30c67-121">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30c67-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30c67-122">-Name</span></span>
<span data-ttu-id="30c67-123">Задает имя для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="30c67-123">Specifies a name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30c67-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30c67-124">-ResourceGroupName</span></span>
<span data-ttu-id="30c67-125">Указывает имя группы ресурсов, для которой этот командлет создает Runbook.</span><span class="sxs-lookup"><span data-stu-id="30c67-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="30c67-126">-Теги</span><span class="sxs-lookup"><span data-stu-id="30c67-126">-Tags</span></span>
<span data-ttu-id="30c67-127">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="30c67-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="30c67-128">Например:</span><span class="sxs-lookup"><span data-stu-id="30c67-128">For example:</span></span>

<span data-ttu-id="30c67-129">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="30c67-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30c67-130">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="30c67-130">-Type</span></span>
<span data-ttu-id="30c67-131">Указывает тип Runbook, создаваемый этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="30c67-131">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="30c67-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="30c67-132">Valid values are:</span></span>

- <span data-ttu-id="30c67-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="30c67-133">PowerShell</span></span>
- <span data-ttu-id="30c67-134">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="30c67-134">GraphicalPowerShell</span></span>
- <span data-ttu-id="30c67-135">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="30c67-135">PowerShellWorkflow</span></span>
- <span data-ttu-id="30c67-136">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="30c67-136">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="30c67-137">Виде</span><span class="sxs-lookup"><span data-stu-id="30c67-137">Graph</span></span>

<span data-ttu-id="30c67-138">Диаграмма значений устарела.</span><span class="sxs-lookup"><span data-stu-id="30c67-138">The value Graph is obsolete.</span></span>
<span data-ttu-id="30c67-139">Это эквивалентно GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="30c67-139">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30c67-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c67-140">CommonParameters</span></span>
<span data-ttu-id="30c67-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30c67-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c67-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30c67-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c67-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30c67-143">INPUTS</span></span>

### <span data-ttu-id="30c67-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="30c67-144">None</span></span>
<span data-ttu-id="30c67-145">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="30c67-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30c67-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30c67-146">OUTPUTS</span></span>

### <span data-ttu-id="30c67-147">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="30c67-147">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="30c67-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="30c67-148">NOTES</span></span>

## <span data-ttu-id="30c67-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30c67-149">RELATED LINKS</span></span>

[<span data-ttu-id="30c67-150">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30c67-150">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30c67-151">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30c67-151">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30c67-152">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30c67-152">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30c67-153">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30c67-153">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30c67-154">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30c67-154">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30c67-155">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30c67-155">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30c67-156">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30c67-156">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
