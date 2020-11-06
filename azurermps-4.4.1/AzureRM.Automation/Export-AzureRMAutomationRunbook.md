---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: b78b992e74252f645faabcf284c817b1cb3c1d5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557963"
---
# <span data-ttu-id="232df-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232df-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="232df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="232df-102">SYNOPSIS</span></span>
<span data-ttu-id="232df-103">Экспортирует Runbook автоматизации.</span><span class="sxs-lookup"><span data-stu-id="232df-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="232df-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="232df-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="232df-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="232df-105">DESCRIPTION</span></span>
<span data-ttu-id="232df-106">Командлет **Export-AzureRmAutomationRunbook** экспортирует Runbook службы автоматизации Azure в файл сценария wps_2 (PS1) для wps_2 или wps_2 Runbooks рабочего процесса или в графический файл Runbook (graphrunbook) для графических Runbook.</span><span class="sxs-lookup"><span data-stu-id="232df-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="232df-107">Имя модуля Runbook становится именем экспортируемого файла.</span><span class="sxs-lookup"><span data-stu-id="232df-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="232df-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="232df-108">EXAMPLES</span></span>

### <span data-ttu-id="232df-109">Пример 1: экспорт Runbook</span><span class="sxs-lookup"><span data-stu-id="232df-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="232df-110">Эта команда экспортирует опубликованную версию Runbook Automation на Рабочий стол пользователя.</span><span class="sxs-lookup"><span data-stu-id="232df-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="232df-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="232df-111">PARAMETERS</span></span>

### <span data-ttu-id="232df-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="232df-112">-AutomationAccountName</span></span>
<span data-ttu-id="232df-113">Указывает имя учетной записи автоматизации, в которой этот командлет экспортирует Runbook.</span><span class="sxs-lookup"><span data-stu-id="232df-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="232df-114">-Force</span><span class="sxs-lookup"><span data-stu-id="232df-114">-Force</span></span>
<span data-ttu-id="232df-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="232df-115">ps_force</span></span>

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

### <span data-ttu-id="232df-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="232df-116">-Name</span></span>
<span data-ttu-id="232df-117">Указывает имя Runbook, который экспортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="232df-117">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="232df-118">Имя модуля Runbook становится именем файла экспорта.</span><span class="sxs-lookup"><span data-stu-id="232df-118">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="232df-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="232df-119">-OutputFolder</span></span>
<span data-ttu-id="232df-120">Указывает путь к папке, в которой этот командлет создает файл экспорта.</span><span class="sxs-lookup"><span data-stu-id="232df-120">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="232df-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="232df-121">-ResourceGroupName</span></span>
<span data-ttu-id="232df-122">Указывает имя группы ресурсов, для которой этот командлет экспортирует Runbook.</span><span class="sxs-lookup"><span data-stu-id="232df-122">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="232df-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="232df-123">-Slot</span></span>
<span data-ttu-id="232df-124">Указывает, экспортирует ли этот командлет черновик или опубликованное содержимое Runbook.</span><span class="sxs-lookup"><span data-stu-id="232df-124">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="232df-125">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="232df-125">Valid values are:</span></span> 

- <span data-ttu-id="232df-126">Отменить</span><span class="sxs-lookup"><span data-stu-id="232df-126">Published</span></span> 
- <span data-ttu-id="232df-127">Проверяем</span><span class="sxs-lookup"><span data-stu-id="232df-127">Draft</span></span>

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

### <span data-ttu-id="232df-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="232df-128">-Confirm</span></span>
<span data-ttu-id="232df-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="232df-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="232df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="232df-130">-WhatIf</span></span>
<span data-ttu-id="232df-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="232df-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="232df-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="232df-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="232df-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232df-133">-DefaultProfile</span></span>
<span data-ttu-id="232df-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="232df-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="232df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232df-135">CommonParameters</span></span>
<span data-ttu-id="232df-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="232df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232df-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="232df-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232df-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="232df-138">INPUTS</span></span>

## <span data-ttu-id="232df-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="232df-139">OUTPUTS</span></span>

### <span data-ttu-id="232df-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="232df-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="232df-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="232df-141">NOTES</span></span>

## <span data-ttu-id="232df-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="232df-142">RELATED LINKS</span></span>

[<span data-ttu-id="232df-143">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232df-143">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232df-144">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232df-144">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232df-145">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232df-145">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232df-146">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232df-146">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232df-147">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232df-147">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232df-148">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232df-148">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232df-149">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232df-149">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="232df-150">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="232df-150">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


