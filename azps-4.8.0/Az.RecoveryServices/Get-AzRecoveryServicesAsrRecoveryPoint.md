---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 67e38be81ddce808151824ee307f27dd758768ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077697"
---
# <span data-ttu-id="36f99-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="36f99-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="36f99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36f99-102">SYNOPSIS</span></span>
<span data-ttu-id="36f99-103">Получает доступные точки восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="36f99-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="36f99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36f99-104">SYNTAX</span></span>

### <span data-ttu-id="36f99-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36f99-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36f99-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="36f99-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36f99-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36f99-107">DESCRIPTION</span></span>
<span data-ttu-id="36f99-108">Командлет **Get-AzRecoveryServicesAsrRecoveryPoint** получает список доступных точек восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="36f99-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="36f99-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36f99-109">EXAMPLES</span></span>

### <span data-ttu-id="36f99-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36f99-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="36f99-111">Возвращает точки восстановления для указанного элемента, защищенного репликацией ASR.</span><span class="sxs-lookup"><span data-stu-id="36f99-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="36f99-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36f99-112">PARAMETERS</span></span>

### <span data-ttu-id="36f99-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f99-113">-DefaultProfile</span></span>
<span data-ttu-id="36f99-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36f99-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="36f99-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36f99-115">-Name</span></span>
<span data-ttu-id="36f99-116">Указывает имя точки восстановления, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="36f99-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="36f99-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="36f99-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="36f99-118">Указывает объект элемента, защищенного репликацией Azure Site Recovery, для которого требуется получить список доступных точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="36f99-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="36f99-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f99-119">CommonParameters</span></span>
<span data-ttu-id="36f99-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36f99-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f99-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36f99-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f99-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36f99-122">INPUTS</span></span>

### <span data-ttu-id="36f99-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="36f99-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="36f99-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36f99-124">OUTPUTS</span></span>

### <span data-ttu-id="36f99-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="36f99-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="36f99-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="36f99-126">NOTES</span></span>

## <span data-ttu-id="36f99-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36f99-127">RELATED LINKS</span></span>

[<span data-ttu-id="36f99-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="36f99-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="36f99-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="36f99-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="36f99-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="36f99-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="36f99-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="36f99-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="36f99-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="36f99-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
