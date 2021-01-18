---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509826"
---
# <span data-ttu-id="94cf9-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="94cf9-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="94cf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="94cf9-103">Запускает задание синхронизации источников автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="94cf9-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="94cf9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94cf9-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94cf9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="94cf9-106">С Start-AzAutomationSourceControlSyncJob запускается задание синхронизации источников автоматизации Azure для заданного имени.</span><span class="sxs-lookup"><span data-stu-id="94cf9-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="94cf9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94cf9-107">EXAMPLES</span></span>

### <span data-ttu-id="94cf9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="94cf9-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="94cf9-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94cf9-109">PARAMETERS</span></span>

### <span data-ttu-id="94cf9-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="94cf9-110">-AutomationAccountName</span></span>
<span data-ttu-id="94cf9-111">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="94cf9-111">The automation account name.</span></span>

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

### <span data-ttu-id="94cf9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94cf9-112">-DefaultProfile</span></span>
<span data-ttu-id="94cf9-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94cf9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94cf9-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="94cf9-114">-JobId</span></span>
<span data-ttu-id="94cf9-115">Код задания синхронизации для управления источником.</span><span class="sxs-lookup"><span data-stu-id="94cf9-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="94cf9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94cf9-116">-ResourceGroupName</span></span>
<span data-ttu-id="94cf9-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94cf9-117">The resource group name.</span></span>

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

### <span data-ttu-id="94cf9-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="94cf9-118">-SourceControlName</span></span>
<span data-ttu-id="94cf9-119">Имя источника.</span><span class="sxs-lookup"><span data-stu-id="94cf9-119">The source control name.</span></span>

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

### <span data-ttu-id="94cf9-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94cf9-120">-Confirm</span></span>
<span data-ttu-id="94cf9-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94cf9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94cf9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94cf9-122">-WhatIf</span></span>
<span data-ttu-id="94cf9-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94cf9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94cf9-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94cf9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94cf9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94cf9-125">CommonParameters</span></span>
<span data-ttu-id="94cf9-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94cf9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94cf9-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94cf9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94cf9-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94cf9-128">INPUTS</span></span>

### <span data-ttu-id="94cf9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="94cf9-129">System.String</span></span>

## <span data-ttu-id="94cf9-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94cf9-130">OUTPUTS</span></span>

### <span data-ttu-id="94cf9-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="94cf9-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="94cf9-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94cf9-132">NOTES</span></span>

## <span data-ttu-id="94cf9-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94cf9-133">RELATED LINKS</span></span>
