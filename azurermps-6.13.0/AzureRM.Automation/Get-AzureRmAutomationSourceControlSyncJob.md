---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControlSyncJob.md
ms.openlocfilehash: 213df264e4ecd458c8505d521556f49265577333
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567311"
---
# <span data-ttu-id="f60ff-101">Get-AzureRmAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="f60ff-101">Get-AzureRmAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="f60ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f60ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f60ff-103">Возвращает задания синхронизации для системы управления версиями Azure.</span><span class="sxs-lookup"><span data-stu-id="f60ff-103">Gets Azure Automation source control sync jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f60ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f60ff-104">SYNTAX</span></span>

```
Get-AzureRmAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f60ff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f60ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f60ff-106">Командлет Get-AzureRmAutomationSourceControlSyncJob получает задания синхронизации управления источниками для Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f60ff-106">The Get-AzureRmAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="f60ff-107">Чтобы получить определенное задание синхронизации системы управления версиями, укажите его идентификатор.</span><span class="sxs-lookup"><span data-stu-id="f60ff-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="f60ff-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f60ff-108">EXAMPLES</span></span>

### <span data-ttu-id="f60ff-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f60ff-109">Example 1</span></span>
<span data-ttu-id="f60ff-110">Эта команда получает все задания синхронизации системы управления версиями для автоматизации для системы управления версиями VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="f60ff-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="f60ff-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f60ff-111">Example 2</span></span>
<span data-ttu-id="f60ff-112">Эта команда получает задание синхронизации системы управления версиями с ИД 08d6d266-27b6-463c-beea-bc48a67ace15 для элемента управления источником VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="f60ff-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzureRmAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"
                                                  -Id "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

## <span data-ttu-id="f60ff-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f60ff-113">PARAMETERS</span></span>

### <span data-ttu-id="f60ff-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f60ff-114">-AutomationAccountName</span></span>
<span data-ttu-id="f60ff-115">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="f60ff-115">The automation account name.</span></span>

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

### <span data-ttu-id="f60ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60ff-116">-DefaultProfile</span></span>
<span data-ttu-id="f60ff-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f60ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f60ff-118">-JobId</span><span class="sxs-lookup"><span data-stu-id="f60ff-118">-JobId</span></span>
<span data-ttu-id="f60ff-119">Идентификатор задания синхронизации системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="f60ff-119">The source control sync job id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: SourceControlSyncJobId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f60ff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f60ff-120">-ResourceGroupName</span></span>
<span data-ttu-id="f60ff-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f60ff-121">The resource group name.</span></span>

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

### <span data-ttu-id="f60ff-122">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="f60ff-122">-SourceControlName</span></span>
<span data-ttu-id="f60ff-123">Имя задания в системе управления версиями.</span><span class="sxs-lookup"><span data-stu-id="f60ff-123">The source control name of the job.</span></span>

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

### <span data-ttu-id="f60ff-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60ff-124">CommonParameters</span></span>
<span data-ttu-id="f60ff-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f60ff-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60ff-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f60ff-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60ff-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f60ff-127">INPUTS</span></span>

### <span data-ttu-id="f60ff-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f60ff-128">System.String</span></span>

### <span data-ttu-id="f60ff-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f60ff-129">System.Guid</span></span>

## <span data-ttu-id="f60ff-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f60ff-130">OUTPUTS</span></span>

### <span data-ttu-id="f60ff-131">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="f60ff-131">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="f60ff-132">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="f60ff-132">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="f60ff-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f60ff-133">NOTES</span></span>

## <span data-ttu-id="f60ff-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f60ff-134">RELATED LINKS</span></span>
