---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 96a30621bc545b635262fd7937e0e55739d0be7c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569255"
---
# <span data-ttu-id="22cbb-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="22cbb-101">Get-AzureRmRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="22cbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="22cbb-103">Получает доступные точки восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="22cbb-103">Gets the available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22cbb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22cbb-104">SYNTAX</span></span>

### <span data-ttu-id="22cbb-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22cbb-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [<CommonParameters>]
```

### <span data-ttu-id="22cbb-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="22cbb-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPoint -Name <String>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [<CommonParameters>]
```

## <span data-ttu-id="22cbb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22cbb-107">DESCRIPTION</span></span>
<span data-ttu-id="22cbb-108">Командлет **Get-AzureRmRecoveryServicesAsrRecoveryPoint** получает список доступных точек восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="22cbb-108">The **Get-AzureRmRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="22cbb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22cbb-109">EXAMPLES</span></span>

### <span data-ttu-id="22cbb-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22cbb-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzureRmRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="22cbb-111">Возвращает точки восстановления для указанного элемента, защищенного репликацией ASR.</span><span class="sxs-lookup"><span data-stu-id="22cbb-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="22cbb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22cbb-112">PARAMETERS</span></span>

### <span data-ttu-id="22cbb-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="22cbb-113">-Name</span></span>
<span data-ttu-id="22cbb-114">Указывает имя точки восстановления, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="22cbb-114">Specifies the name of the recovery point to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22cbb-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="22cbb-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="22cbb-116">Указывает объект элемента, защищенного репликацией Azure Site Recovery, для которого требуется получить список доступных точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="22cbb-116">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22cbb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cbb-117">CommonParameters</span></span>
<span data-ttu-id="22cbb-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22cbb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cbb-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22cbb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cbb-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22cbb-120">INPUTS</span></span>

### <span data-ttu-id="22cbb-121">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="22cbb-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="22cbb-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22cbb-122">OUTPUTS</span></span>

### <span data-ttu-id="22cbb-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="22cbb-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="22cbb-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="22cbb-124">NOTES</span></span>

## <span data-ttu-id="22cbb-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22cbb-125">RELATED LINKS</span></span>

[<span data-ttu-id="22cbb-126">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22cbb-126">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="22cbb-127">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22cbb-127">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="22cbb-128">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22cbb-128">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="22cbb-129">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22cbb-129">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="22cbb-130">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="22cbb-130">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
