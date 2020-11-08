---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/stop-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: bb5c78d6c0ae29d415e02d3e78e79f963bc3315c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076714"
---
# <span data-ttu-id="25b7c-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="25b7c-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="25b7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="25b7c-103">Отмена задания миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="25b7c-103">Cancel a disk migration job.</span></span>

## <span data-ttu-id="25b7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25b7c-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25b7c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25b7c-105">DESCRIPTION</span></span>
<span data-ttu-id="25b7c-106">Отмена задания миграции дисков.</span><span class="sxs-lookup"><span data-stu-id="25b7c-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="25b7c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25b7c-107">EXAMPLES</span></span>

### <span data-ttu-id="25b7c-108">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="25b7c-108">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsDiskMigrationJob -Name TestJob

CreationTime : 2/26/2020 11:06:40 AM
EndTime      : 2/26/2020 11:07:24 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob
Location     : redmond
MigrationId  : TestJob
Name         : redmond/TestJob
StartTime    : 2/26/2020 11:06:40 AM
Status       : Canceled
Subtask      : {47774498-6bc7-4ce2-98ca-738739ded2fc, b09ac623-f71d-480c-98bc-88fa3f603f2c}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_4
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="25b7c-109">Отмена задания миграции управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="25b7c-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="25b7c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25b7c-110">PARAMETERS</span></span>

### <span data-ttu-id="25b7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b7c-111">-DefaultProfile</span></span>
<span data-ttu-id="25b7c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25b7c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25b7c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="25b7c-113">-Location</span></span>
<span data-ttu-id="25b7c-114">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="25b7c-114">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25b7c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="25b7c-115">-Name</span></span>
<span data-ttu-id="25b7c-116">Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="25b7c-116">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25b7c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25b7c-117">-SubscriptionId</span></span>
<span data-ttu-id="25b7c-118">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="25b7c-118">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="25b7c-119">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="25b7c-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="25b7c-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25b7c-120">-Confirm</span></span>
<span data-ttu-id="25b7c-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="25b7c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25b7c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25b7c-122">-WhatIf</span></span>
<span data-ttu-id="25b7c-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="25b7c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25b7c-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25b7c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25b7c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b7c-125">CommonParameters</span></span>
<span data-ttu-id="25b7c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25b7c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b7c-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25b7c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b7c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25b7c-128">INPUTS</span></span>

## <span data-ttu-id="25b7c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25b7c-129">OUTPUTS</span></span>

### <span data-ttu-id="25b7c-130">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="25b7c-130">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="25b7c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="25b7c-131">NOTES</span></span>

## <span data-ttu-id="25b7c-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25b7c-132">RELATED LINKS</span></span>

