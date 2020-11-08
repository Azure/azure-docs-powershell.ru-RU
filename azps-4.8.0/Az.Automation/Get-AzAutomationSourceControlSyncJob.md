---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrolsyncjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControlSyncJob.md
ms.openlocfilehash: a6d8a618ea9561c244b161407807ddfbe99b854a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077953"
---
# <span data-ttu-id="92d2f-101">Get-AzAutomationSourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="92d2f-101">Get-AzAutomationSourceControlSyncJob</span></span>

## <span data-ttu-id="92d2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="92d2f-103">Возвращает задания синхронизации для системы управления версиями Azure.</span><span class="sxs-lookup"><span data-stu-id="92d2f-103">Gets Azure Automation source control sync jobs.</span></span>

## <span data-ttu-id="92d2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92d2f-104">SYNTAX</span></span>

```
Get-AzAutomationSourceControlSyncJob -SourceControlName <String> [-JobId <Guid>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92d2f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92d2f-105">DESCRIPTION</span></span>
<span data-ttu-id="92d2f-106">Командлет Get-AzAutomationSourceControlSyncJob получает задания синхронизации управления источниками для Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="92d2f-106">The Get-AzAutomationSourceControlSyncJob cmdlet gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="92d2f-107">Чтобы получить определенное задание синхронизации системы управления версиями, укажите его идентификатор.</span><span class="sxs-lookup"><span data-stu-id="92d2f-107">To get a specific source control sync job, specify its id.</span></span>

## <span data-ttu-id="92d2f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92d2f-108">EXAMPLES</span></span>

### <span data-ttu-id="92d2f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="92d2f-109">Example 1</span></span>
<span data-ttu-id="92d2f-110">Эта команда получает все задания синхронизации системы управления версиями для автоматизации для системы управления версиями VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="92d2f-110">This command gets all the Automation source control sync jobs for the source control VSTSNative.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative"

SourceControlSyncJobId               SyncType Status StartTime           EndTime
----------------------               -------- ------ ---------           -------
08d6d266-27b6-463c-beea-bc48a67ace15 FullSync Failed 08/15/2018 09:17 AM 08/15/2018 09:18 AM
b566d564-878a-4641-8c44-25bf7850531e FullSync Failed 08/15/2018 09:09 AM 08/15/2018 09:10 AM
```

### <span data-ttu-id="92d2f-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="92d2f-111">Example 2</span></span>
<span data-ttu-id="92d2f-112">Эта команда получает задание синхронизации системы управления версиями с ИД 08d6d266-27b6-463c-beea-bc48a67ace15 для элемента управления источником VSTSNative.</span><span class="sxs-lookup"><span data-stu-id="92d2f-112">This command gets the source control sync job with id 08d6d266-27b6-463c-beea-bc48a67ace15 for the source control VSTSNative.</span></span> 


```powershell
PS C:\> Get-AzAutomationSourceControlSyncJob -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "VSTSNative" `
                                                  -JobId "08d6d266-27b6-463c-beea-bc48a67ace15"

Status SyncType Exception
------ -------- ---------
Failed FullSync There were errors while syncing the user runbooks. Please see error streams for more information. (T...
```

### <span data-ttu-id="92d2f-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="92d2f-113">Example 3</span></span>

<span data-ttu-id="92d2f-114">Возвращает задания синхронизации для системы управления версиями Azure.</span><span class="sxs-lookup"><span data-stu-id="92d2f-114">Gets Azure Automation source control sync jobs.</span></span> <span data-ttu-id="92d2f-115">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="92d2f-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzAutomationSourceControlSyncJob -AutomationAccountName 'devAccount' -JobId 00000000-0000-0000-0000-00000000000000000 -ResourceGroupName 'rg1' -SourceControlName 'VSTSNative'
```

## <span data-ttu-id="92d2f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92d2f-116">PARAMETERS</span></span>

### <span data-ttu-id="92d2f-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="92d2f-117">-AutomationAccountName</span></span>
<span data-ttu-id="92d2f-118">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="92d2f-118">The automation account name.</span></span>

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

### <span data-ttu-id="92d2f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d2f-119">-DefaultProfile</span></span>
<span data-ttu-id="92d2f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92d2f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d2f-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="92d2f-121">-JobId</span></span>
<span data-ttu-id="92d2f-122">Идентификатор задания синхронизации системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="92d2f-122">The source control sync job id.</span></span>

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

### <span data-ttu-id="92d2f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92d2f-123">-ResourceGroupName</span></span>
<span data-ttu-id="92d2f-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92d2f-124">The resource group name.</span></span>

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

### <span data-ttu-id="92d2f-125">-SourceControlName</span><span class="sxs-lookup"><span data-stu-id="92d2f-125">-SourceControlName</span></span>
<span data-ttu-id="92d2f-126">Имя задания в системе управления версиями.</span><span class="sxs-lookup"><span data-stu-id="92d2f-126">The source control name of the job.</span></span>

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

### <span data-ttu-id="92d2f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d2f-127">CommonParameters</span></span>
<span data-ttu-id="92d2f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92d2f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d2f-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92d2f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d2f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92d2f-130">INPUTS</span></span>

### <span data-ttu-id="92d2f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="92d2f-131">System.String</span></span>

### <span data-ttu-id="92d2f-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="92d2f-132">System.Guid</span></span>

## <span data-ttu-id="92d2f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92d2f-133">OUTPUTS</span></span>

### <span data-ttu-id="92d2f-134">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJob</span><span class="sxs-lookup"><span data-stu-id="92d2f-134">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJob</span></span>

### <span data-ttu-id="92d2f-135">Microsoft. Azure. Commands. Automation. Model. SourceControlSyncJobRecord</span><span class="sxs-lookup"><span data-stu-id="92d2f-135">Microsoft.Azure.Commands.Automation.Model.SourceControlSyncJobRecord</span></span>

## <span data-ttu-id="92d2f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="92d2f-136">NOTES</span></span>

## <span data-ttu-id="92d2f-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92d2f-137">RELATED LINKS</span></span>
