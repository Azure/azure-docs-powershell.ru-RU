---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 03a57c35063a401aa5f730e11538532bdbbbc58c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398076"
---
# <span data-ttu-id="ad37d-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad37d-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="ad37d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad37d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad37d-103">Экспорт книги автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ad37d-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="ad37d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad37d-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad37d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad37d-105">DESCRIPTION</span></span>
<span data-ttu-id="ad37d-106">С помощью cmdlet **Export-AzAutomationRunbook** можно экспортировать книгу автоматизации Azure в файл сценария wps_2 (PS1), в wps_2 или wps_2 workflow runbook, а также в графический файл runbook (Graphrunbook) для графических книг.</span><span class="sxs-lookup"><span data-stu-id="ad37d-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="ad37d-107">Имя книги становится именем экспортируемого файла.</span><span class="sxs-lookup"><span data-stu-id="ad37d-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="ad37d-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad37d-108">EXAMPLES</span></span>

### <span data-ttu-id="ad37d-109">Пример 1. Экспорт книги</span><span class="sxs-lookup"><span data-stu-id="ad37d-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="ad37d-110">Эта команда экспортирует опубликованную версию книги автоматизации на рабочий стол пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad37d-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="ad37d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad37d-111">PARAMETERS</span></span>

### <span data-ttu-id="ad37d-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ad37d-112">-AutomationAccountName</span></span>
<span data-ttu-id="ad37d-113">Указывает имя учетной записи автоматизации, в которую этот cmdlet экспортирует книгу.</span><span class="sxs-lookup"><span data-stu-id="ad37d-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="ad37d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad37d-114">-DefaultProfile</span></span>
<span data-ttu-id="ad37d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ad37d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad37d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ad37d-116">-Force</span></span>
<span data-ttu-id="ad37d-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="ad37d-117">ps_force</span></span>

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

### <span data-ttu-id="ad37d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ad37d-118">-Name</span></span>
<span data-ttu-id="ad37d-119">Указывает имя книги, которую экспортирует этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad37d-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="ad37d-120">Имя книги становится именем файла экспорта.</span><span class="sxs-lookup"><span data-stu-id="ad37d-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="ad37d-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="ad37d-121">-OutputFolder</span></span>
<span data-ttu-id="ad37d-122">Путь к папке, в которой этот cmdlet создает файл экспорта.</span><span class="sxs-lookup"><span data-stu-id="ad37d-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="ad37d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad37d-123">-ResourceGroupName</span></span>
<span data-ttu-id="ad37d-124">Имя группы ресурсов, для которой этот cmdlet экспортирует книгу.</span><span class="sxs-lookup"><span data-stu-id="ad37d-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="ad37d-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="ad37d-125">-Slot</span></span>
<span data-ttu-id="ad37d-126">Определяет, будет ли этот cmdlet экспортировать черновик или опубликованное содержимое книги.</span><span class="sxs-lookup"><span data-stu-id="ad37d-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="ad37d-127">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="ad37d-127">Valid values are:</span></span> 
- <span data-ttu-id="ad37d-128">Опубликовано</span><span class="sxs-lookup"><span data-stu-id="ad37d-128">Published</span></span> 
- <span data-ttu-id="ad37d-129">Черновик</span><span class="sxs-lookup"><span data-stu-id="ad37d-129">Draft</span></span>

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

### <span data-ttu-id="ad37d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad37d-130">-Confirm</span></span>
<span data-ttu-id="ad37d-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad37d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad37d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad37d-132">-WhatIf</span></span>
<span data-ttu-id="ad37d-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad37d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad37d-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ad37d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad37d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad37d-135">CommonParameters</span></span>
<span data-ttu-id="ad37d-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad37d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad37d-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad37d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad37d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad37d-138">INPUTS</span></span>

### <span data-ttu-id="ad37d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ad37d-139">System.String</span></span>

## <span data-ttu-id="ad37d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad37d-140">OUTPUTS</span></span>

### <span data-ttu-id="ad37d-141">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="ad37d-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="ad37d-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad37d-142">NOTES</span></span>

## <span data-ttu-id="ad37d-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad37d-143">RELATED LINKS</span></span>

[<span data-ttu-id="ad37d-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad37d-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="ad37d-145">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad37d-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="ad37d-146">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad37d-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ad37d-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad37d-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ad37d-148">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad37d-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="ad37d-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad37d-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="ad37d-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad37d-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="ad37d-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ad37d-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


