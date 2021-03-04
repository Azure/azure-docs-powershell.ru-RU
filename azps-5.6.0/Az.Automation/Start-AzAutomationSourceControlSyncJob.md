---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: f232f876ff77944beb1d506e5763621f9470cd21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957667"
---
# <span data-ttu-id="06316-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="06316-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="06316-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06316-102">SYNOPSIS</span></span>
<span data-ttu-id="06316-103">Запускает задание синхронизации источников автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="06316-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="06316-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="06316-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06316-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06316-105">DESCRIPTION</span></span>
<span data-ttu-id="06316-106">С Start-AzAutomationSourceControlSyncJob запускается задание синхронизации источников автоматизации Azure для заданного имени.</span><span class="sxs-lookup"><span data-stu-id="06316-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="06316-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="06316-107">EXAMPLES</span></span>

### <span data-ttu-id="06316-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="06316-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="06316-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06316-109">PARAMETERS</span></span>

### <span data-ttu-id="06316-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="06316-110">-AutomationAccountName</span></span>
<span data-ttu-id="06316-111">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="06316-111">The automation account name.</span></span>

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

### <span data-ttu-id="06316-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06316-112">-DefaultProfile</span></span>
<span data-ttu-id="06316-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="06316-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06316-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="06316-114">-JobId</span></span>
<span data-ttu-id="06316-115">Код задания синхронизации для управления источником.</span><span class="sxs-lookup"><span data-stu-id="06316-115">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06316-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06316-116">-ResourceGroupName</span></span>
<span data-ttu-id="06316-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="06316-117">The resource group name.</span></span>

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

### <span data-ttu-id="06316-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="06316-118">-SourceControlName</span></span>
<span data-ttu-id="06316-119">Имя источника.</span><span class="sxs-lookup"><span data-stu-id="06316-119">The source control name.</span></span>

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

### <span data-ttu-id="06316-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06316-120">-Confirm</span></span>
<span data-ttu-id="06316-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06316-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06316-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06316-122">-WhatIf</span></span>
<span data-ttu-id="06316-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06316-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06316-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="06316-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06316-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06316-125">CommonParameters</span></span>
<span data-ttu-id="06316-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06316-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06316-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06316-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06316-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06316-128">INPUTS</span></span>

### <span data-ttu-id="06316-129">System.String</span><span class="sxs-lookup"><span data-stu-id="06316-129">System.String</span></span>

## <span data-ttu-id="06316-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06316-130">OUTPUTS</span></span>

### <span data-ttu-id="06316-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="06316-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="06316-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="06316-132">NOTES</span></span>

## <span data-ttu-id="06316-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06316-133">RELATED LINKS</span></span>
