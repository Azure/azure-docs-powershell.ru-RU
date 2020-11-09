---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: 1f685307ae1d6f9a030ac5c242af9fcec97c032b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316211"
---
# <span data-ttu-id="ecece-101">Start-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="ecece-101">Start-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="ecece-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ecece-102">SYNOPSIS</span></span>
<span data-ttu-id="ecece-103">Запускает задание синхронизации для системы управления версиями Azure.</span><span class="sxs-lookup"><span data-stu-id="ecece-103">Starts an Azure Automation source control sync job.</span></span>

## <span data-ttu-id="ecece-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ecece-104">SYNTAX</span></span>

```
Start-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecece-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecece-105">DESCRIPTION</span></span>
<span data-ttu-id="ecece-106">Командлет Start-AzAutomationSourceControlSyncJob запускает задание синхронизации для элемента управления источником автоматизации Azure для заданного имени исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ecece-106">The Start-AzAutomationSourceControlSyncJob cmdlet starts a Azure Automation source control sync job for the given source control name.</span></span>

## <span data-ttu-id="ecece-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ecece-107">EXAMPLES</span></span>

### <span data-ttu-id="ecece-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ecece-108">Example 1</span></span>
```powershell
PS C:\> Start-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="ecece-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ecece-109">PARAMETERS</span></span>

### <span data-ttu-id="ecece-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ecece-110">-AutomationAccountName</span></span>
<span data-ttu-id="ecece-111">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ecece-111">The automation account name.</span></span>

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

### <span data-ttu-id="ecece-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecece-112">-DefaultProfile</span></span>
<span data-ttu-id="ecece-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ecece-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecece-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="ecece-114">-JobId</span></span>
<span data-ttu-id="ecece-115">Идентификатор задания синхронизации системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="ecece-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="ecece-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecece-116">-ResourceGroupName</span></span>
<span data-ttu-id="ecece-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ecece-117">The resource group name.</span></span>

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

### <span data-ttu-id="ecece-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="ecece-118">-SourceControlName</span></span>
<span data-ttu-id="ecece-119">Имя исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ecece-119">The source control name.</span></span>

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

### <span data-ttu-id="ecece-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecece-120">-Confirm</span></span>
<span data-ttu-id="ecece-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ecece-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecece-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecece-122">-WhatIf</span></span>
<span data-ttu-id="ecece-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ecece-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecece-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ecece-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecece-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecece-125">CommonParameters</span></span>
<span data-ttu-id="ecece-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ecece-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecece-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecece-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecece-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ecece-128">INPUTS</span></span>

### <span data-ttu-id="ecece-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ecece-129">System.String</span></span>

## <span data-ttu-id="ecece-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecece-130">OUTPUTS</span></span>

### <span data-ttu-id="ecece-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="ecece-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="ecece-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ecece-132">NOTES</span></span>

## <span data-ttu-id="ecece-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecece-133">RELATED LINKS</span></span>
