---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 5f2c72eb3b456d19b51651bbed79676093ba8685
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731486"
---
# <span data-ttu-id="b1371-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="b1371-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="b1371-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1371-102">SYNOPSIS</span></span>
<span data-ttu-id="b1371-103">Запускает задание синхронизации для системы управления версиями Azure.</span><span class="sxs-lookup"><span data-stu-id="b1371-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="b1371-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1371-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1371-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1371-105">DESCRIPTION</span></span>
<span data-ttu-id="b1371-106">Командлет Start-AzAutomationSourceControlSyncJob запускает задание синхронизации элемента управления Azure Automation исходных для заданного имени исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b1371-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation souce control sync job for the given source control name.</span></span>

## <span data-ttu-id="b1371-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1371-107">EXAMPLES</span></span>

### <span data-ttu-id="b1371-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1371-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="b1371-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1371-109">PARAMETERS</span></span>

### <span data-ttu-id="b1371-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b1371-110">-AutomationAccountName</span></span>
<span data-ttu-id="b1371-111">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b1371-111">The automation account name.</span></span>

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

### <span data-ttu-id="b1371-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1371-112">-DefaultProfile</span></span>
<span data-ttu-id="b1371-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1371-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1371-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="b1371-114">-JobId</span></span>
<span data-ttu-id="b1371-115">Идентификатор задания синхронизации системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="b1371-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="b1371-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1371-116">-ResourceGroupName</span></span>
<span data-ttu-id="b1371-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1371-117">The resource group name.</span></span>

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

### <span data-ttu-id="b1371-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="b1371-118">-SourceControlName</span></span>
<span data-ttu-id="b1371-119">Имя исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="b1371-119">The source control name.</span></span>

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

### <span data-ttu-id="b1371-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1371-120">-Confirm</span></span>
<span data-ttu-id="b1371-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b1371-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1371-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1371-122">-WhatIf</span></span>
<span data-ttu-id="b1371-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b1371-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1371-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b1371-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1371-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1371-125">CommonParameters</span></span>
<span data-ttu-id="b1371-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1371-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1371-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1371-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1371-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1371-128">INPUTS</span></span>

### <span data-ttu-id="b1371-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b1371-129">System.String</span></span>

## <span data-ttu-id="b1371-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1371-130">OUTPUTS</span></span>

### <span data-ttu-id="b1371-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="b1371-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="b1371-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1371-132">NOTES</span></span>

## <span data-ttu-id="b1371-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1371-133">RELATED LINKS</span></span>
