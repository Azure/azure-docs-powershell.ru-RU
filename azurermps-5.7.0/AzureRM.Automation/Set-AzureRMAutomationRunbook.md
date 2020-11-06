---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 46c77e1538c367e38220a022bf3b84e796dd0ec3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567477"
---
# <span data-ttu-id="eb62d-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb62d-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="eb62d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb62d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb62d-103">Изменение модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="eb62d-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb62d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb62d-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb62d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb62d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb62d-106">Командлет **Set-AzureRmAutomationRunbook** изменяет конфигурацию Azure Automation RUNBOOK в ТД.</span><span class="sxs-lookup"><span data-stu-id="eb62d-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="eb62d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb62d-107">EXAMPLES</span></span>

### <span data-ttu-id="eb62d-108">Пример 1: включение подробного ведения журнала для модуля Runbook</span><span class="sxs-lookup"><span data-stu-id="eb62d-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="eb62d-109">Эта команда включает подробный журнал для заданий указанного Runbook в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="eb62d-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="eb62d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb62d-110">PARAMETERS</span></span>

### <span data-ttu-id="eb62d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eb62d-111">-AutomationAccountName</span></span>
<span data-ttu-id="eb62d-112">Указывает имя учетной записи автоматизации, в которой этот командлет изменяет Runbook.</span><span class="sxs-lookup"><span data-stu-id="eb62d-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="eb62d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb62d-113">-DefaultProfile</span></span>
<span data-ttu-id="eb62d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eb62d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb62d-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="eb62d-115">-Description</span></span>
<span data-ttu-id="eb62d-116">Задает описание для модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="eb62d-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="eb62d-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="eb62d-117">-LogProgress</span></span>
<span data-ttu-id="eb62d-118">Указывает, выполняется ли журнал Runbook.</span><span class="sxs-lookup"><span data-stu-id="eb62d-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="eb62d-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="eb62d-119">-LogVerbose</span></span>
<span data-ttu-id="eb62d-120">Указывает, включаются ли в ведение журнала подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb62d-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="eb62d-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eb62d-121">-Name</span></span>
<span data-ttu-id="eb62d-122">Указывает имя Runbook, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eb62d-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="eb62d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb62d-123">-ResourceGroupName</span></span>
<span data-ttu-id="eb62d-124">Указывает имя группы ресурсов, для которой этот командлет изменяет Runbook.</span><span class="sxs-lookup"><span data-stu-id="eb62d-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="eb62d-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="eb62d-125">-Tag</span></span>
<span data-ttu-id="eb62d-126">Теги Runbook.</span><span class="sxs-lookup"><span data-stu-id="eb62d-126">The runbook tags.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb62d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb62d-127">CommonParameters</span></span>
<span data-ttu-id="eb62d-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb62d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb62d-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb62d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb62d-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb62d-130">INPUTS</span></span>

### <span data-ttu-id="eb62d-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="eb62d-131">None</span></span>
<span data-ttu-id="eb62d-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="eb62d-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb62d-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb62d-133">OUTPUTS</span></span>

### <span data-ttu-id="eb62d-134">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="eb62d-134">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="eb62d-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb62d-135">NOTES</span></span>

## <span data-ttu-id="eb62d-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb62d-136">RELATED LINKS</span></span>

[<span data-ttu-id="eb62d-137">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb62d-137">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb62d-138">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb62d-138">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb62d-139">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb62d-139">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb62d-140">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb62d-140">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb62d-141">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb62d-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb62d-142">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb62d-142">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb62d-143">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb62d-143">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="eb62d-144">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="eb62d-144">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


