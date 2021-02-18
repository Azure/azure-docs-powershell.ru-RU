---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216153"
---
# <span data-ttu-id="d781e-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="d781e-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="d781e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d781e-102">SYNOPSIS</span></span>
<span data-ttu-id="d781e-103">Запускает задание синхронизации источников автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d781e-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="d781e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d781e-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d781e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d781e-105">DESCRIPTION</span></span>
<span data-ttu-id="d781e-106">С Start-AzAutomationSourceControlSyncJob запускается задание синхронизации источников автоматизации Azure для заданного имени.</span><span class="sxs-lookup"><span data-stu-id="d781e-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="d781e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d781e-107">EXAMPLES</span></span>

### <span data-ttu-id="d781e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d781e-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="d781e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d781e-109">PARAMETERS</span></span>

### <span data-ttu-id="d781e-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d781e-110">-AutomationAccountName</span></span>
<span data-ttu-id="d781e-111">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d781e-111">The automation account name.</span></span>

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

### <span data-ttu-id="d781e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d781e-112">-DefaultProfile</span></span>
<span data-ttu-id="d781e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d781e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d781e-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="d781e-114">-JobId</span></span>
<span data-ttu-id="d781e-115">Код задания синхронизации для управления источником.</span><span class="sxs-lookup"><span data-stu-id="d781e-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="d781e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d781e-116">-ResourceGroupName</span></span>
<span data-ttu-id="d781e-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d781e-117">The resource group name.</span></span>

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

### <span data-ttu-id="d781e-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="d781e-118">-SourceControlName</span></span>
<span data-ttu-id="d781e-119">Имя источника.</span><span class="sxs-lookup"><span data-stu-id="d781e-119">The source control name.</span></span>

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

### <span data-ttu-id="d781e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d781e-120">-Confirm</span></span>
<span data-ttu-id="d781e-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d781e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d781e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d781e-122">-WhatIf</span></span>
<span data-ttu-id="d781e-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d781e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d781e-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d781e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d781e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d781e-125">CommonParameters</span></span>
<span data-ttu-id="d781e-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d781e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d781e-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d781e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d781e-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d781e-128">INPUTS</span></span>

### <span data-ttu-id="d781e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d781e-129">System.String</span></span>

## <span data-ttu-id="d781e-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d781e-130">OUTPUTS</span></span>

### <span data-ttu-id="d781e-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="d781e-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="d781e-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d781e-132">NOTES</span></span>

## <span data-ttu-id="d781e-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d781e-133">RELATED LINKS</span></span>
