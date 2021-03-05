---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPoint.md
ms.openlocfilehash: 27f1f0f03da7a4ad912be28a2de85bf6e7cf58f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014936"
---
# <span data-ttu-id="2529f-101">Get-AzRecoveryServicesAsrRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2529f-101">Get-AzRecoveryServicesAsrRecoveryPoint</span></span>

## <span data-ttu-id="2529f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2529f-102">SYNOPSIS</span></span>
<span data-ttu-id="2529f-103">Возвращает доступные точки восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="2529f-103">Gets the available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="2529f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2529f-104">SYNTAX</span></span>

### <span data-ttu-id="2529f-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2529f-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2529f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2529f-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2529f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2529f-107">DESCRIPTION</span></span>
<span data-ttu-id="2529f-108">Чтобы получить список доступных точек восстановления для элемента, защищенного репликацией, можно получить список баллов, доступных для **azRecoveryServicesAsrRecoveryPoint.**</span><span class="sxs-lookup"><span data-stu-id="2529f-108">The **Get-AzRecoveryServicesAsrRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="2529f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2529f-109">EXAMPLES</span></span>

### <span data-ttu-id="2529f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2529f-110">Example 1</span></span>
```
PS C:\> $RecoveryPoints = Get-AzRecoveryServicesAsrRecoveryPoint -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="2529f-111">Возвращает точки восстановления для указанного элемента, защищенного репликацией ASR.</span><span class="sxs-lookup"><span data-stu-id="2529f-111">Gets recovery points for the specified ASR replication protected item.</span></span>

## <span data-ttu-id="2529f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2529f-112">PARAMETERS</span></span>

### <span data-ttu-id="2529f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2529f-113">-DefaultProfile</span></span>
<span data-ttu-id="2529f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2529f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2529f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2529f-115">-Name</span></span>
<span data-ttu-id="2529f-116">Указывает имя точки восстановления, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="2529f-116">Specifies the name of the recovery point to get.</span></span>

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

### <span data-ttu-id="2529f-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2529f-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="2529f-118">Указывает объект защищенного элемента восстановления сайта Azure, для которого нужно получить список доступных точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="2529f-118">Specifies the Azure Site Recovery Replication Protected Item object for which to get the list of available recovery points.</span></span>

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

### <span data-ttu-id="2529f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2529f-119">CommonParameters</span></span>
<span data-ttu-id="2529f-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2529f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2529f-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2529f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2529f-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2529f-122">INPUTS</span></span>

### <span data-ttu-id="2529f-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2529f-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="2529f-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2529f-124">OUTPUTS</span></span>

### <span data-ttu-id="2529f-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2529f-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint</span></span>

## <span data-ttu-id="2529f-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2529f-126">NOTES</span></span>

## <span data-ttu-id="2529f-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2529f-127">RELATED LINKS</span></span>

[<span data-ttu-id="2529f-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2529f-128">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Edit-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2529f-129">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2529f-129">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2529f-130">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2529f-130">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2529f-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2529f-131">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="2529f-132">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="2529f-132">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
