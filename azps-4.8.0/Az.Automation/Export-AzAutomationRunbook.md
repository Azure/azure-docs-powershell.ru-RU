---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 03a57c35063a401aa5f730e11538532bdbbbc58c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077971"
---
# <span data-ttu-id="a4c40-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a4c40-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="a4c40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4c40-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c40-103">Экспортирует Runbook автоматизации.</span><span class="sxs-lookup"><span data-stu-id="a4c40-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="a4c40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4c40-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4c40-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4c40-105">DESCRIPTION</span></span>
<span data-ttu-id="a4c40-106">Командлет **Export-AzAutomationRunbook** экспортирует Runbook службы автоматизации Azure в файл сценария wps_2 (PS1) для wps_2 или wps_2 Runbooks рабочего процесса или в графический файл Runbook (graphrunbook) для графических Runbook.</span><span class="sxs-lookup"><span data-stu-id="a4c40-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="a4c40-107">Имя модуля Runbook становится именем экспортируемого файла.</span><span class="sxs-lookup"><span data-stu-id="a4c40-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="a4c40-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4c40-108">EXAMPLES</span></span>

### <span data-ttu-id="a4c40-109">Пример 1: экспорт Runbook</span><span class="sxs-lookup"><span data-stu-id="a4c40-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="a4c40-110">Эта команда экспортирует опубликованную версию Runbook Automation на Рабочий стол пользователя.</span><span class="sxs-lookup"><span data-stu-id="a4c40-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="a4c40-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4c40-111">PARAMETERS</span></span>

### <span data-ttu-id="a4c40-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a4c40-112">-AutomationAccountName</span></span>
<span data-ttu-id="a4c40-113">Указывает имя учетной записи автоматизации, в которой этот командлет экспортирует Runbook.</span><span class="sxs-lookup"><span data-stu-id="a4c40-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="a4c40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c40-114">-DefaultProfile</span></span>
<span data-ttu-id="a4c40-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a4c40-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4c40-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a4c40-116">-Force</span></span>
<span data-ttu-id="a4c40-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="a4c40-117">ps_force</span></span>

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

### <span data-ttu-id="a4c40-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4c40-118">-Name</span></span>
<span data-ttu-id="a4c40-119">Указывает имя Runbook, который экспортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4c40-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="a4c40-120">Имя модуля Runbook становится именем файла экспорта.</span><span class="sxs-lookup"><span data-stu-id="a4c40-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="a4c40-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="a4c40-121">-OutputFolder</span></span>
<span data-ttu-id="a4c40-122">Указывает путь к папке, в которой этот командлет создает файл экспорта.</span><span class="sxs-lookup"><span data-stu-id="a4c40-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="a4c40-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c40-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4c40-124">Указывает имя группы ресурсов, для которой этот командлет экспортирует Runbook.</span><span class="sxs-lookup"><span data-stu-id="a4c40-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="a4c40-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="a4c40-125">-Slot</span></span>
<span data-ttu-id="a4c40-126">Указывает, экспортирует ли этот командлет черновик или опубликованное содержимое Runbook.</span><span class="sxs-lookup"><span data-stu-id="a4c40-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="a4c40-127">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a4c40-127">Valid values are:</span></span> 
- <span data-ttu-id="a4c40-128">Отменить</span><span class="sxs-lookup"><span data-stu-id="a4c40-128">Published</span></span> 
- <span data-ttu-id="a4c40-129">Проверяем</span><span class="sxs-lookup"><span data-stu-id="a4c40-129">Draft</span></span>

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

### <span data-ttu-id="a4c40-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4c40-130">-Confirm</span></span>
<span data-ttu-id="a4c40-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4c40-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4c40-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4c40-132">-WhatIf</span></span>
<span data-ttu-id="a4c40-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4c40-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4c40-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4c40-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4c40-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c40-135">CommonParameters</span></span>
<span data-ttu-id="a4c40-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4c40-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c40-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4c40-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c40-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4c40-138">INPUTS</span></span>

### <span data-ttu-id="a4c40-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a4c40-139">System.String</span></span>

## <span data-ttu-id="a4c40-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4c40-140">OUTPUTS</span></span>

### <span data-ttu-id="a4c40-141">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="a4c40-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="a4c40-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4c40-142">NOTES</span></span>

## <span data-ttu-id="a4c40-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4c40-143">RELATED LINKS</span></span>

[<span data-ttu-id="a4c40-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a4c40-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="a4c40-145">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a4c40-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="a4c40-146">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a4c40-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a4c40-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a4c40-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a4c40-148">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a4c40-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="a4c40-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a4c40-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="a4c40-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a4c40-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="a4c40-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a4c40-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


