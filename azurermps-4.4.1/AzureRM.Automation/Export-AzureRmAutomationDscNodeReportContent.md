---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
ms.openlocfilehash: 23c17a0614a28a571b58e19ff2556c45679e6c82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565709"
---
# <span data-ttu-id="1aa2d-101">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="1aa2d-101">Export-AzureRmAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="1aa2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1aa2d-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa2d-103">Экспортирует необработанное содержимое отчета DSC, отправленное с узла DSC в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1aa2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1aa2d-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aa2d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1aa2d-105">DESCRIPTION</span></span>
<span data-ttu-id="1aa2d-106">Командлет **Export-AzureRmAutomationDscNodeReportContent** экспортирует необработанное содержимое отчета о настройке требуемого состояния ТД (DSC).</span><span class="sxs-lookup"><span data-stu-id="1aa2d-106">The **Export-AzureRmAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="1aa2d-107">Узел DSC отправляет отчет DSC в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="1aa2d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1aa2d-108">EXAMPLES</span></span>

### <span data-ttu-id="1aa2d-109">Пример 1: экспорт отчета из узла DSC</span><span class="sxs-lookup"><span data-stu-id="1aa2d-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzureRmAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="1aa2d-110">Этот набор команд экспортирует последний отчет из узла DSC с именем Computer14 на Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="1aa2d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1aa2d-111">PARAMETERS</span></span>

### <span data-ttu-id="1aa2d-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1aa2d-112">-AutomationAccountName</span></span>
<span data-ttu-id="1aa2d-113">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="1aa2d-114">Этот командлет экспортирует содержимое отчета для узла DSC, который принадлежит учетной записи автоматизации, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="1aa2d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1aa2d-115">-Force</span></span>
<span data-ttu-id="1aa2d-116">Указывает на то, что этот командлет заменяет существующий локальный файл новым файлом с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-116">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="1aa2d-117">-NodeId</span><span class="sxs-lookup"><span data-stu-id="1aa2d-117">-NodeId</span></span>
<span data-ttu-id="1aa2d-118">Указывает уникальный идентификатор узла DSC, для которого этот командлет экспортирует содержимое отчета.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-118">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="1aa2d-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="1aa2d-119">-OutputFolder</span></span>
<span data-ttu-id="1aa2d-120">Указывает папку выходных данных, в которой этот командлет экспортирует содержимое отчета.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-120">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="1aa2d-121">-ReportId</span><span class="sxs-lookup"><span data-stu-id="1aa2d-121">-ReportId</span></span>
<span data-ttu-id="1aa2d-122">Указывает уникальный идентификатор отчета узла DSC, который экспортируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-122">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="1aa2d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aa2d-123">-ResourceGroupName</span></span>
<span data-ttu-id="1aa2d-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1aa2d-125">Этот командлет экспортирует содержимое отчета для узла DSC, который принадлежит к группе ресурсов, которую указывает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-125">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="1aa2d-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1aa2d-126">-Confirm</span></span>
<span data-ttu-id="1aa2d-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aa2d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aa2d-128">-WhatIf</span></span>
<span data-ttu-id="1aa2d-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aa2d-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aa2d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa2d-131">-DefaultProfile</span></span>
<span data-ttu-id="1aa2d-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1aa2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa2d-133">CommonParameters</span></span>
<span data-ttu-id="1aa2d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1aa2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa2d-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aa2d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa2d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1aa2d-136">INPUTS</span></span>

## <span data-ttu-id="1aa2d-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1aa2d-137">OUTPUTS</span></span>

### <span data-ttu-id="1aa2d-138">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="1aa2d-138">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="1aa2d-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1aa2d-139">NOTES</span></span>

## <span data-ttu-id="1aa2d-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1aa2d-140">RELATED LINKS</span></span>

[<span data-ttu-id="1aa2d-141">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="1aa2d-141">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)

[<span data-ttu-id="1aa2d-142">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="1aa2d-142">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="1aa2d-143">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="1aa2d-143">Get-AzureRmAutomationDscNodeReport</span></span>](./Get-AzureRmAutomationDscNodeReport.md)


