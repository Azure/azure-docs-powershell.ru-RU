---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJobOutput.md
ms.openlocfilehash: 6567d479ad0db7df959e4059155149f4fc06e1a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235217"
---
# <span data-ttu-id="05f29-101">Get-AzAutomationSourceControlSyncJobOutput</span><span class="sxs-lookup"><span data-stu-id="05f29-101">Get-AzAutomationSourceControlSyncJobOutput</span></span>

## <span data-ttu-id="05f29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05f29-102">SYNOPSIS</span></span>
<span data-ttu-id="05f29-103">Возвращает результат задания синхронизации источников автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="05f29-103">Gets the output of an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="05f29-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="05f29-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJobOutput -SourceControlName <String> -JobId <Guid>
 [-Stream <SourceControlSyncJobStreamType>] [-StreamId <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05f29-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05f29-105">DESCRIPTION</span></span>
<span data-ttu-id="05f29-106">Командалет **Get-AzAutomationSourceControlSyncJobOutput** получает выходные данные для задания синхронизации источника данных автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="05f29-106">The **Get-AzAutomationSourceControlSyncJobOutput** cmdlet gets the output for a Azure Automation source control sync job.</span></span>

## <span data-ttu-id="05f29-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="05f29-107">EXAMPLES</span></span>

### <span data-ttu-id="05f29-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="05f29-108">Example 1</span></span>
<span data-ttu-id="05f29-109">Эта команда получает результат задания синхронизации управления источником с кодом 08d6d266-27b6-463c-beea-bc48a67ace15 для средства VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="05f29-109">This command gets the output of source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


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

## <span data-ttu-id="05f29-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05f29-110">PARAMETERS</span></span>

### <span data-ttu-id="05f29-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="05f29-111">-AutomationAccountName</span></span>
<span data-ttu-id="05f29-112">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="05f29-112">The automation account name.</span></span>

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

### <span data-ttu-id="05f29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05f29-113">-DefaultProfile</span></span>
<span data-ttu-id="05f29-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05f29-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05f29-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="05f29-115">-JobId</span></span>
<span data-ttu-id="05f29-116">Код задания синхронизации для управления источником.</span><span class="sxs-lookup"><span data-stu-id="05f29-116">The source control sync job id.</span></span>

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

### <span data-ttu-id="05f29-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05f29-117">-ResourceGroupName</span></span>
<span data-ttu-id="05f29-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="05f29-118">The resource group name.</span></span>

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

### <span data-ttu-id="05f29-119">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="05f29-119">-SourceControlName</span></span>
<span data-ttu-id="05f29-120">Имя источника.</span><span class="sxs-lookup"><span data-stu-id="05f29-120">The source control name.</span></span>

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

### <span data-ttu-id="05f29-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="05f29-121">-Stream</span></span>
<span data-ttu-id="05f29-122">Тип потока.</span><span class="sxs-lookup"><span data-stu-id="05f29-122">The stream type.</span></span>
<span data-ttu-id="05f29-123">По умолчанию значение Any.</span><span class="sxs-lookup"><span data-stu-id="05f29-123">Defaults to Any.</span></span>

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

### <span data-ttu-id="05f29-124">-StreamId</span><span class="sxs-lookup"><span data-stu-id="05f29-124">-StreamId</span></span>
<span data-ttu-id="05f29-125">The stream id.</span><span class="sxs-lookup"><span data-stu-id="05f29-125">The stream id.</span></span>

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

### <span data-ttu-id="05f29-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f29-126">CommonParameters</span></span>
<span data-ttu-id="05f29-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05f29-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f29-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05f29-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f29-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05f29-129">INPUTS</span></span>

### <span data-ttu-id="05f29-130">System.String</span><span class="sxs-lookup"><span data-stu-id="05f29-130">System.String</span></span>

### <span data-ttu-id="05f29-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="05f29-131">System.Guid</span></span>

### <span data-ttu-id="05f29-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span><span class="sxs-lookup"><span data-stu-id="05f29-132">Microsoft.Azure.Commands.Automation.Common.SourceControlSyncJobStreamType</span></span>

## <span data-ttu-id="05f29-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="05f29-133">OUTPUTS</span></span>

### <span data-ttu-id="05f29-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span><span class="sxs-lookup"><span data-stu-id="05f29-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStream</span></span>

### <span data-ttu-id="05f29-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="05f29-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobStreamRecord</span></span>

## <span data-ttu-id="05f29-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="05f29-136">NOTES</span></span>

## <span data-ttu-id="05f29-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05f29-137">RELATED LINKS</span></span>
