---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 4a5864e9572a21442a5333232fe5f705fb1b5687
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556840"
---
# <span data-ttu-id="ebbe0-101">Start-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="ebbe0-101">Start-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="ebbe0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebbe0-102">SYNOPSIS</span></span>
<span data-ttu-id="ebbe0-103">Запускает задание синхронизации для системы управления версиями Azure.</span><span class="sxs-lookup"><span data-stu-id="ebbe0-103">Starts an Azure Automation source control sync job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebbe0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebbe0-104">SYNTAX</span></span>

```
Start-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebbe0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebbe0-105">DESCRIPTION</span></span>
<span data-ttu-id="ebbe0-106">Командлет Start-AzureRmAutomationSourceControlSyncJob запускает задание синхронизации элемента управления Azure Automation исходных для заданного имени исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ebbe0-106">The Start-AzureRmAutomationSourceControlSyncJob cmdlet starts a Azure Automation souce control sync job for the given source control name.</span></span>

## <span data-ttu-id="ebbe0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebbe0-107">EXAMPLES</span></span>

### <span data-ttu-id="ebbe0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ebbe0-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                    -AutomationAccountName "devAccount" `
                                                    -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status  StartTime EndTime
----------------------               -------- ------  --------- -------
b51aed78-bef6-40d4-a966-cd45fd5af576 FullSync Running
```

## <span data-ttu-id="ebbe0-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebbe0-109">PARAMETERS</span></span>

### <span data-ttu-id="ebbe0-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ebbe0-110">-AutomationAccountName</span></span>
<span data-ttu-id="ebbe0-111">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ebbe0-111">The automation account name.</span></span>

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

### <span data-ttu-id="ebbe0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebbe0-112">-DefaultProfile</span></span>
<span data-ttu-id="ebbe0-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebbe0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebbe0-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="ebbe0-114">-JobId</span></span>
<span data-ttu-id="ebbe0-115">Идентификатор задания синхронизации системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="ebbe0-115">The source control sync job id.</span></span>

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

### <span data-ttu-id="ebbe0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebbe0-116">-ResourceGroupName</span></span>
<span data-ttu-id="ebbe0-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ebbe0-117">The resource group name.</span></span>

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

### <span data-ttu-id="ebbe0-118">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="ebbe0-118">-SourceControlName</span></span>
<span data-ttu-id="ebbe0-119">Имя исходного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="ebbe0-119">The source control name.</span></span>

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

### <span data-ttu-id="ebbe0-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebbe0-120">-Confirm</span></span>
<span data-ttu-id="ebbe0-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebbe0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebbe0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebbe0-122">-WhatIf</span></span>
<span data-ttu-id="ebbe0-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebbe0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebbe0-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebbe0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebbe0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebbe0-125">CommonParameters</span></span>
<span data-ttu-id="ebbe0-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebbe0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebbe0-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebbe0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebbe0-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebbe0-128">INPUTS</span></span>

### <span data-ttu-id="ebbe0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ebbe0-129">System.String</span></span>

## <span data-ttu-id="ebbe0-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebbe0-130">OUTPUTS</span></span>

### <span data-ttu-id="ebbe0-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="ebbe0-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

## <span data-ttu-id="ebbe0-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebbe0-132">NOTES</span></span>

## <span data-ttu-id="ebbe0-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebbe0-133">RELATED LINKS</span></span>
