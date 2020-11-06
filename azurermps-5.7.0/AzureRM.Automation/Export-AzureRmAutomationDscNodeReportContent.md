---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
ms.openlocfilehash: aba2a95492a72f1b88aec4f38a037b315ede17a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565590"
---
# <span data-ttu-id="8d753-101">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="8d753-101">Export-AzureRmAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="8d753-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d753-102">SYNOPSIS</span></span>
<span data-ttu-id="8d753-103">Экспортирует необработанное содержимое отчета DSC, отправленное с узла DSC в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="8d753-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d753-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d753-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d753-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d753-105">DESCRIPTION</span></span>
<span data-ttu-id="8d753-106">Командлет **Export-AzureRmAutomationDscNodeReportContent** экспортирует необработанное содержимое отчета о настройке требуемого состояния ТД (DSC).</span><span class="sxs-lookup"><span data-stu-id="8d753-106">The **Export-AzureRmAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="8d753-107">Узел DSC отправляет отчет DSC в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="8d753-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="8d753-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d753-108">EXAMPLES</span></span>

### <span data-ttu-id="8d753-109">Пример 1: экспорт отчета из узла DSC</span><span class="sxs-lookup"><span data-stu-id="8d753-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzureRmAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="8d753-110">Этот набор команд экспортирует последний отчет из узла DSC с именем Computer14 на Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="8d753-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="8d753-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d753-111">PARAMETERS</span></span>

### <span data-ttu-id="8d753-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8d753-112">-AutomationAccountName</span></span>
<span data-ttu-id="8d753-113">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8d753-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="8d753-114">Этот командлет экспортирует содержимое отчета для узла DSC, который принадлежит учетной записи автоматизации, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="8d753-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="8d753-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d753-115">-DefaultProfile</span></span>
<span data-ttu-id="8d753-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8d753-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d753-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8d753-117">-Force</span></span>
<span data-ttu-id="8d753-118">Указывает на то, что этот командлет заменяет существующий локальный файл новым файлом с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="8d753-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d753-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="8d753-119">-NodeId</span></span>
<span data-ttu-id="8d753-120">Указывает уникальный идентификатор узла DSC, для которого этот командлет экспортирует содержимое отчета.</span><span class="sxs-lookup"><span data-stu-id="8d753-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d753-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="8d753-121">-OutputFolder</span></span>
<span data-ttu-id="8d753-122">Указывает папку выходных данных, в которой этот командлет экспортирует содержимое отчета.</span><span class="sxs-lookup"><span data-stu-id="8d753-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="8d753-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="8d753-123">-ReportId</span></span>
<span data-ttu-id="8d753-124">Указывает уникальный идентификатор отчета узла DSC, который экспортируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8d753-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d753-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d753-125">-ResourceGroupName</span></span>
<span data-ttu-id="8d753-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8d753-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8d753-127">Этот командлет экспортирует содержимое отчета для узла DSC, который принадлежит к группе ресурсов, которую указывает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8d753-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="8d753-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d753-128">-Confirm</span></span>
<span data-ttu-id="8d753-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8d753-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d753-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d753-130">-WhatIf</span></span>
<span data-ttu-id="8d753-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8d753-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d753-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8d753-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d753-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d753-133">CommonParameters</span></span>
<span data-ttu-id="8d753-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d753-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d753-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d753-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d753-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d753-136">INPUTS</span></span>

### <span data-ttu-id="8d753-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="8d753-137">None</span></span>
<span data-ttu-id="8d753-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8d753-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8d753-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d753-139">OUTPUTS</span></span>

### <span data-ttu-id="8d753-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="8d753-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="8d753-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d753-141">NOTES</span></span>

## <span data-ttu-id="8d753-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d753-142">RELATED LINKS</span></span>

[<span data-ttu-id="8d753-143">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="8d753-143">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)

[<span data-ttu-id="8d753-144">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="8d753-144">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="8d753-145">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="8d753-145">Get-AzureRmAutomationDscNodeReport</span></span>](./Get-AzureRmAutomationDscNodeReport.md)


