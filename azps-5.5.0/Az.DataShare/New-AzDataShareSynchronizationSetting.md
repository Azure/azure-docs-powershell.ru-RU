---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: df8f61b10750f50bef1b3417da7f28be4ec0d0d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228652"
---
# <span data-ttu-id="c32ff-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="c32ff-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="c32ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c32ff-102">SYNOPSIS</span></span>
<span data-ttu-id="c32ff-103">Создает параметр синхронизации для поделиться.</span><span class="sxs-lookup"><span data-stu-id="c32ff-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="c32ff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c32ff-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c32ff-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c32ff-105">DESCRIPTION</span></span>
<span data-ttu-id="c32ff-106">Параметр синхронизации для параметра **New-AzDataShareSynchronizationSetting** создает параметр синхронизации для учетной записи share для интервала повторения (ежедневно или почасово) в определенное время.</span><span class="sxs-lookup"><span data-stu-id="c32ff-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="c32ff-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c32ff-107">EXAMPLES</span></span>

### <span data-ttu-id="c32ff-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c32ff-108">Example 1</span></span>
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

<span data-ttu-id="c32ff-109">Эти команды создают параметр синхронизации с ежедневным интервалом повторения в 9:00 для share AdsShare в учетной записи Share Data Share WikiAds.</span><span class="sxs-lookup"><span data-stu-id="c32ff-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="c32ff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c32ff-110">PARAMETERS</span></span>

### <span data-ttu-id="c32ff-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c32ff-111">-AccountName</span></span>
<span data-ttu-id="c32ff-112">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="c32ff-112">Azure data share account name</span></span>

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

### <span data-ttu-id="c32ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c32ff-113">-DefaultProfile</span></span>
<span data-ttu-id="c32ff-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c32ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c32ff-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c32ff-115">-Name</span></span>
<span data-ttu-id="c32ff-116">Имя параметра синхронизации</span><span class="sxs-lookup"><span data-stu-id="c32ff-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="c32ff-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="c32ff-117">-RecurrenceInterval</span></span>
<span data-ttu-id="c32ff-118">Интервал повторения для параметра синхронизации (день или час)</span><span class="sxs-lookup"><span data-stu-id="c32ff-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="c32ff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c32ff-119">-ResourceGroupName</span></span>
<span data-ttu-id="c32ff-120">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="c32ff-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="c32ff-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c32ff-121">-ShareName</span></span>
<span data-ttu-id="c32ff-122">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="c32ff-122">Azure data share name</span></span>

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

### <span data-ttu-id="c32ff-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="c32ff-123">-SynchronizationTime</span></span>
<span data-ttu-id="c32ff-124">Время начала запланированной синхронизации</span><span class="sxs-lookup"><span data-stu-id="c32ff-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="c32ff-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c32ff-125">-Confirm</span></span>
<span data-ttu-id="c32ff-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c32ff-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c32ff-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c32ff-127">-WhatIf</span></span>
<span data-ttu-id="c32ff-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c32ff-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c32ff-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c32ff-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c32ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c32ff-130">CommonParameters</span></span>
<span data-ttu-id="c32ff-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c32ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c32ff-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c32ff-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c32ff-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c32ff-133">INPUTS</span></span>

### <span data-ttu-id="c32ff-134">Нет</span><span class="sxs-lookup"><span data-stu-id="c32ff-134">None</span></span>

## <span data-ttu-id="c32ff-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c32ff-135">OUTPUTS</span></span>

### <span data-ttu-id="c32ff-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="c32ff-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="c32ff-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c32ff-137">NOTES</span></span>

## <span data-ttu-id="c32ff-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c32ff-138">RELATED LINKS</span></span>
