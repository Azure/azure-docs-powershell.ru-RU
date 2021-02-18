---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 03a57c35063a401aa5f730e11538532bdbbbc58c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239648"
---
# <span data-ttu-id="1d4d3-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d4d3-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="1d4d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="1d4d3-103">Экспорт книги автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="1d4d3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1d4d3-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d4d3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d4d3-105">DESCRIPTION</span></span>
<span data-ttu-id="1d4d3-106">С помощью cmdlet **Export-AzAutomationRunbook** можно экспортировать книгу автоматизации Azure в файл сценария wps_2 (PS1), для wps_2 или wps_2 workflow runbook, а также графический файл runbook (Graphrunbook) для графических runbooks.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="1d4d3-107">Имя книги становится именем экспортируемого файла.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="1d4d3-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1d4d3-108">EXAMPLES</span></span>

### <span data-ttu-id="1d4d3-109">Пример 1. Экспорт книги</span><span class="sxs-lookup"><span data-stu-id="1d4d3-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="1d4d3-110">Эта команда экспортирует опубликованную версию книги автоматизации на рабочий стол пользователя.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="1d4d3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d4d3-111">PARAMETERS</span></span>

### <span data-ttu-id="1d4d3-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1d4d3-112">-AutomationAccountName</span></span>
<span data-ttu-id="1d4d3-113">Указывает имя учетной записи автоматизации, в которую этот cmdlet экспортирует книгу.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="1d4d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d4d3-114">-DefaultProfile</span></span>
<span data-ttu-id="1d4d3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1d4d3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d4d3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1d4d3-116">-Force</span></span>
<span data-ttu-id="1d4d3-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="1d4d3-117">ps_force</span></span>

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

### <span data-ttu-id="1d4d3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1d4d3-118">-Name</span></span>
<span data-ttu-id="1d4d3-119">Определяет имя книги, которую экспортирует этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="1d4d3-120">Имя книги становится именем файла экспорта.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="1d4d3-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="1d4d3-121">-OutputFolder</span></span>
<span data-ttu-id="1d4d3-122">Путь к папке, в которой этот cmdlet создает файл экспорта.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="1d4d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d4d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="1d4d3-124">Имя группы ресурсов, для которой этот cmdlet экспортирует книгу.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="1d4d3-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="1d4d3-125">-Slot</span></span>
<span data-ttu-id="1d4d3-126">Определяет, будет ли этот cmdlet экспортировать черновик или опубликованное содержимое книги.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="1d4d3-127">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="1d4d3-127">Valid values are:</span></span> 
- <span data-ttu-id="1d4d3-128">Опубликовано</span><span class="sxs-lookup"><span data-stu-id="1d4d3-128">Published</span></span> 
- <span data-ttu-id="1d4d3-129">Черновик</span><span class="sxs-lookup"><span data-stu-id="1d4d3-129">Draft</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d4d3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d4d3-130">-Confirm</span></span>
<span data-ttu-id="1d4d3-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d4d3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d4d3-132">-WhatIf</span></span>
<span data-ttu-id="1d4d3-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d4d3-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d4d3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d4d3-135">CommonParameters</span></span>
<span data-ttu-id="1d4d3-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d4d3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d4d3-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d4d3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d4d3-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d4d3-138">INPUTS</span></span>

### <span data-ttu-id="1d4d3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1d4d3-139">System.String</span></span>

## <span data-ttu-id="1d4d3-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1d4d3-140">OUTPUTS</span></span>

### <span data-ttu-id="1d4d3-141">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="1d4d3-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="1d4d3-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1d4d3-142">NOTES</span></span>

## <span data-ttu-id="1d4d3-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d4d3-143">RELATED LINKS</span></span>

[<span data-ttu-id="1d4d3-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d4d3-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="1d4d3-145">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d4d3-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="1d4d3-146">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d4d3-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1d4d3-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d4d3-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="1d4d3-148">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d4d3-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="1d4d3-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d4d3-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="1d4d3-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d4d3-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="1d4d3-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1d4d3-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


