---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 67e38be81ddce808151824ee307f27dd758768ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065079"
---
# <span data-ttu-id="1f436-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1f436-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="1f436-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f436-102">SYNOPSIS</span></span>
<span data-ttu-id="1f436-103">Получает доступные точки восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="1f436-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="1f436-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f436-104">SYNTAX</span></span>

### <span data-ttu-id="1f436-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f436-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f436-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="1f436-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f436-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f436-107">DESCRIPTION</span></span>
<span data-ttu-id="1f436-108">Командлет **Get-AzRecoveryServicesAsrRecoveryPoint** получает список доступных точек восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="1f436-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="1f436-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f436-109">EXAMPLES</span></span>

### <span data-ttu-id="1f436-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f436-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="1f436-111">Возвращает точки восстановления для указанного элемента, защищенного репликацией ASR.</span><span class="sxs-lookup"><span data-stu-id="1f436-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="1f436-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f436-112">PARAMETERS</span></span>

### <span data-ttu-id="1f436-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f436-113">-DefaultProfile</span></span>
<span data-ttu-id="1f436-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f436-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1f436-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f436-115">-Name</span></span>
<span data-ttu-id="1f436-116">Указывает имя точки восстановления, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="1f436-116">Specifies the name of the recovery point to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f436-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1f436-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1f436-118">Указывает объект элемента, защищенного репликацией Azure Site Recovery, для которого требуется получить список доступных точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="1f436-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f436-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f436-119">CommonParameters</span></span>
<span data-ttu-id="1f436-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f436-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f436-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f436-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f436-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f436-122">INPUTS</span></span>

### <span data-ttu-id="1f436-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1f436-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1f436-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f436-124">OUTPUTS</span></span>

### <span data-ttu-id="1f436-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1f436-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="1f436-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f436-126">NOTES</span></span>

## <span data-ttu-id="1f436-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f436-127">RELATED LINKS</span></span>

[<span data-ttu-id="1f436-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1f436-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1f436-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1f436-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1f436-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1f436-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1f436-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1f436-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1f436-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1f436-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
