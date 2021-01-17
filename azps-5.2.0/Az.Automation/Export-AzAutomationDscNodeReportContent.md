---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: dd29a092ec0ca3b24614b363147d4c50bf14dcbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399439"
---
# <span data-ttu-id="db8c8-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="db8c8-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="db8c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="db8c8-103">Экспорт необработанных данных отчета DSC, отправленных с узла DSC, в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="db8c8-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="db8c8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="db8c8-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db8c8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db8c8-105">DESCRIPTION</span></span>
<span data-ttu-id="db8c8-106">Для **экспорта-AzAutomationDscNodeReportContent** можно экспортировать необработанные содержимого отчета APS Desired State Configuration (DSC).</span><span class="sxs-lookup"><span data-stu-id="db8c8-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="db8c8-107">Узел DSC отправляет отчет DSC в автоматизацию Azure.</span><span class="sxs-lookup"><span data-stu-id="db8c8-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="db8c8-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="db8c8-108">EXAMPLES</span></span>

### <span data-ttu-id="db8c8-109">Пример 1. Экспорт отчета из узла DSC</span><span class="sxs-lookup"><span data-stu-id="db8c8-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="db8c8-110">Этот набор команд экспортирует на рабочий стол последнюю версию отчета с узла DSC "Компьютер14".</span><span class="sxs-lookup"><span data-stu-id="db8c8-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="db8c8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db8c8-111">PARAMETERS</span></span>

### <span data-ttu-id="db8c8-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="db8c8-112">-AutomationAccountName</span></span>
<span data-ttu-id="db8c8-113">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="db8c8-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="db8c8-114">Этот cmdlet экспортирует содержимое отчета для узла DSC, который принадлежит учетной записи автоматизации, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="db8c8-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="db8c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db8c8-115">-DefaultProfile</span></span>
<span data-ttu-id="db8c8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="db8c8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db8c8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="db8c8-117">-Force</span></span>
<span data-ttu-id="db8c8-118">Указывает на то, что этот cmdlet заменяет существующий локальный файл новым файлом с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="db8c8-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="db8c8-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="db8c8-119">-NodeId</span></span>
<span data-ttu-id="db8c8-120">Указывает уникальный код узла DSC, для которого этот cmdlet экспортирует содержимое отчета.</span><span class="sxs-lookup"><span data-stu-id="db8c8-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db8c8-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="db8c8-121">-OutputFolder</span></span>
<span data-ttu-id="db8c8-122">Определяет папку вывода, в которой этот cmdlet экспортирует содержимое отчета.</span><span class="sxs-lookup"><span data-stu-id="db8c8-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="db8c8-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="db8c8-123">-ReportId</span></span>
<span data-ttu-id="db8c8-124">Указывает уникальный код отчета узла DSC, экспортируемого этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db8c8-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db8c8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db8c8-125">-ResourceGroupName</span></span>
<span data-ttu-id="db8c8-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db8c8-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="db8c8-127">Этот cmdlet экспортирует содержимое отчета для узла DSC, который принадлежит к группе ресурсов, указанной этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db8c8-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="db8c8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db8c8-128">-Confirm</span></span>
<span data-ttu-id="db8c8-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db8c8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db8c8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db8c8-130">-WhatIf</span></span>
<span data-ttu-id="db8c8-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db8c8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db8c8-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="db8c8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db8c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db8c8-133">CommonParameters</span></span>
<span data-ttu-id="db8c8-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db8c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db8c8-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db8c8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db8c8-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db8c8-136">INPUTS</span></span>

### <span data-ttu-id="db8c8-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="db8c8-137">System.Guid</span></span>

### <span data-ttu-id="db8c8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="db8c8-138">System.String</span></span>

## <span data-ttu-id="db8c8-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db8c8-139">OUTPUTS</span></span>

### <span data-ttu-id="db8c8-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="db8c8-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="db8c8-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="db8c8-141">NOTES</span></span>

## <span data-ttu-id="db8c8-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db8c8-142">RELATED LINKS</span></span>

[<span data-ttu-id="db8c8-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="db8c8-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="db8c8-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="db8c8-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="db8c8-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="db8c8-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


