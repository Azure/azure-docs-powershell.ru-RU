---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 63ff1ea82f3167738161191900e9516513b034bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727821"
---
# <span data-ttu-id="c87ea-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="c87ea-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="c87ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c87ea-102">SYNOPSIS</span></span>
<span data-ttu-id="c87ea-103">Получает выходные данные задания синхронизации для системы управления версиями Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c87ea-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="c87ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c87ea-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c87ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c87ea-105">DESCRIPTION</span></span>
<span data-ttu-id="c87ea-106">Командлет **Get-AzAutomationSourceControlSyncJobOutput** получает выходные данные для задания синхронизации системы управления версиями для Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c87ea-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="c87ea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c87ea-107">EXAMPLES</span></span>

### <span data-ttu-id="c87ea-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c87ea-108">Example 1</span></span>
<span data-ttu-id="c87ea-109">Эта команда получает выходные данные задания синхронизации системы управления версиями с ИД 08d6d266-27b6-463c-beea-bc48a67ace15 для элемента управления источником VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="c87ea-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJobOutput -ResourceGroupName "rg1" `
                                                        -AutomationAccountName "devAccount" `
                                                        -Name "VSTSNative"
                                                        -Id "08d6d266-27b6-463c-beea-bc48a67ace15" `
                                                        -Stream Output | ForEach-Object {$_.summary}

========================================================================================================

Azure Automation Source Control Public Preview.
Supported runbooks to sync: PowerShell Workflow, PowerShell Scripts, DSC Configurations, Graphical, and Python 2.
Setting AzureRmEnvironment.
Getting AzureRunAsConnection.
Logging in to Azure...
Source control information for syncing:
[RepoUrl = https://contoso.visualstudio.com/_git/GitDemo] [Branch  = master] [FolderPath = /]
Verifying url: https://fcontoso.visualstudio.com/_git/GitDemo
Connecting to VSTS...

Source Control Sync Summary:

2 files synced:
 - RunbookA.ps1
 - RunbookB.ps1

Failed to import runbook:
 - RunbookC.ps1

File is not a runbook:
 - README.md
 - text_file.txt

File size exceeds 1Mb:
 - RunbookD_GreatherThan1MB.ps1

Invalid runbook name:
 - RunbookZ_ĈĦŕĬŞ.ps1

========================================================================================================
```

## <span data-ttu-id="c87ea-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c87ea-110">PARAMETERS</span></span>

### <span data-ttu-id="c87ea-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c87ea-111">-AutomationAccountName</span></span>
<span data-ttu-id="c87ea-112">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="c87ea-112">The automation account name.</span></span>

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

### <span data-ttu-id="c87ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c87ea-113">-DefaultProfile</span></span>
<span data-ttu-id="c87ea-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c87ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c87ea-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="c87ea-115">-JobId</span></span>
<span data-ttu-id="c87ea-116">Идентификатор задания синхронизации системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="c87ea-116">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87ea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c87ea-117">-ResourceGroupName</span></span>
<span data-ttu-id="c87ea-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c87ea-118">The resource group name.</span></span>

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

### <span data-ttu-id="c87ea-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="c87ea-119">-SourceControlName</span></span>
<span data-ttu-id="c87ea-120">Имя исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c87ea-120">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87ea-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="c87ea-121">-Stream</span></span>
<span data-ttu-id="c87ea-122">Тип потока.</span><span class="sxs-lookup"><span data-stu-id="c87ea-122">The stream type.</span></span>
<span data-ttu-id="c87ea-123">По умолчанию используется значение Any.</span><span class="sxs-lookup"><span data-stu-id="c87ea-123">Defaults to Any.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Output, Error

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87ea-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="c87ea-124">-StreamId</span></span>
<span data-ttu-id="c87ea-125">Идентификатор потока.</span><span class="sxs-lookup"><span data-stu-id="c87ea-125">The stream id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceControlSyncJobStreamId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c87ea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87ea-126">CommonParameters</span></span>
<span data-ttu-id="c87ea-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c87ea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87ea-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c87ea-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87ea-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c87ea-129">INPUTS</span></span>

### <span data-ttu-id="c87ea-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c87ea-130">System.String</span></span>

### <span data-ttu-id="c87ea-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c87ea-131">System.Guid</span></span>

### <span data-ttu-id="c87ea-132">Microsoft. Azure. Commands. Automation. Common. SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="c87ea-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="c87ea-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c87ea-133">OUTPUTS</span></span>

### <span data-ttu-id="c87ea-134">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="c87ea-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="c87ea-135">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="c87ea-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="c87ea-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="c87ea-136">NOTES</span></span>

## <span data-ttu-id="c87ea-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c87ea-137">RELATED LINKS</span></span>
