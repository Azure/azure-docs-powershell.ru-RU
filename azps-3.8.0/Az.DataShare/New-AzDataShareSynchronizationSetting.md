---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: d7f6429ebc3e8a3ebf1f8dd2749e6b7f66005ecd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066300"
---
# <span data-ttu-id="830c7-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="830c7-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="830c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="830c7-102">SYNOPSIS</span></span>
<span data-ttu-id="830c7-103">Создание параметров синхронизации для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="830c7-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="830c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="830c7-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="830c7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="830c7-105">DESCRIPTION</span></span>
<span data-ttu-id="830c7-106">**Новый параметр-AzDataShareSynchronizationSetting** создает параметры синхронизации для предоставления общего доступа к учетной записи в течение ежедневного или часового интервала в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="830c7-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="830c7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="830c7-107">EXAMPLES</span></span>

### <span data-ttu-id="830c7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="830c7-108">Example 1</span></span>
```
PS C:\>  New-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization" -RecurrenceInterval "Day" -SynchronizationTime 9:00
RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : Ads Company
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="830c7-109">Эти команды создают параметр синхронизации для ежедневного интервала повторения в 9:00, чтобы предоставить общий доступ к AdsShare в WikiAds учетной записи для общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="830c7-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="830c7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="830c7-110">PARAMETERS</span></span>

### <span data-ttu-id="830c7-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="830c7-111">-AccountName</span></span>
<span data-ttu-id="830c7-112">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="830c7-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830c7-113">-DefaultProfile</span></span>
<span data-ttu-id="830c7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="830c7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="830c7-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="830c7-115">-Name</span></span>
<span data-ttu-id="830c7-116">Имя параметра синхронизации</span><span class="sxs-lookup"><span data-stu-id="830c7-116">Synchronization setting name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c7-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="830c7-117">-RecurrenceInterval</span></span>
<span data-ttu-id="830c7-118">Интервал повторения для параметра синхронизации (день или час)</span><span class="sxs-lookup"><span data-stu-id="830c7-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="830c7-119">-ResourceGroupName</span></span>
<span data-ttu-id="830c7-120">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="830c7-120">Resource group name of azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c7-121">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="830c7-121">-ShareName</span></span>
<span data-ttu-id="830c7-122">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="830c7-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c7-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="830c7-123">-SynchronizationTime</span></span>
<span data-ttu-id="830c7-124">Время начала запланированной синхронизации</span><span class="sxs-lookup"><span data-stu-id="830c7-124">The start time of the scheduled synchronization setting</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c7-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="830c7-125">-Confirm</span></span>
<span data-ttu-id="830c7-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="830c7-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830c7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="830c7-127">-WhatIf</span></span>
<span data-ttu-id="830c7-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="830c7-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="830c7-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="830c7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="830c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830c7-130">CommonParameters</span></span>
<span data-ttu-id="830c7-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="830c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830c7-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="830c7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830c7-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="830c7-133">INPUTS</span></span>

### <span data-ttu-id="830c7-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="830c7-134">None</span></span>

## <span data-ttu-id="830c7-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="830c7-135">OUTPUTS</span></span>

### <span data-ttu-id="830c7-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="830c7-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="830c7-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="830c7-137">NOTES</span></span>

## <span data-ttu-id="830c7-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="830c7-138">RELATED LINKS</span></span>
