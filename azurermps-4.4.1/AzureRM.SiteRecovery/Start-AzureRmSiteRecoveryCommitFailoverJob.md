---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 9FF78BE6-FF24-47E9-9F36-48E426097F45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryCommitFailoverJob.md
ms.openlocfilehash: 08e864c3d95c4d077e4d9e1227a0ec606508c193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562080"
---
# <span data-ttu-id="699dc-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="699dc-101">Start-AzureRmSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="699dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="699dc-102">SYNOPSIS</span></span>
<span data-ttu-id="699dc-103">Запускает действие фиксации отработки отказа для объекта восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="699dc-103">Starts the commit failover action for a Site Recovery object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="699dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="699dc-104">SYNTAX</span></span>

### <span data-ttu-id="699dc-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="699dc-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="699dc-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="699dc-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="699dc-107">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="699dc-107">ByPEObject</span></span>
```
Start-AzureRmSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="699dc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="699dc-108">DESCRIPTION</span></span>
<span data-ttu-id="699dc-109">Командлет **Start-AzureRmSiteRecoveryCommitFailoverJob** запускает процесс фиксации отработки отказа для объекта Azure Site Recovery после операции отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="699dc-109">The **Start-AzureRmSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="699dc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="699dc-110">EXAMPLES</span></span>

## <span data-ttu-id="699dc-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="699dc-111">PARAMETERS</span></span>

### <span data-ttu-id="699dc-112">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="699dc-112">-ProtectionEntity</span></span>
<span data-ttu-id="699dc-113">Указывает объект сущности для защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="699dc-113">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="699dc-114">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="699dc-114">-RecoveryPlan</span></span>
<span data-ttu-id="699dc-115">Указывает объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="699dc-115">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="699dc-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="699dc-116">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="699dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699dc-117">-DefaultProfile</span></span>
<span data-ttu-id="699dc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="699dc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="699dc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699dc-119">CommonParameters</span></span>
<span data-ttu-id="699dc-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="699dc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699dc-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="699dc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699dc-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="699dc-122">INPUTS</span></span>

### <span data-ttu-id="699dc-123">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="699dc-123">ASRProtectionEntity</span></span>
<span data-ttu-id="699dc-124">Параметр "ProtectionEntity" принимает значение типа "ASRProtectionEntity" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="699dc-124">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="699dc-125">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="699dc-125">ASRRecoveryPlan</span></span>
<span data-ttu-id="699dc-126">Параметр "RecoveryPlan" принимает значение типа "ASRRecoveryPlan" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="699dc-126">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="699dc-127">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="699dc-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="699dc-128">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="699dc-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="699dc-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="699dc-129">OUTPUTS</span></span>

### <span data-ttu-id="699dc-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="699dc-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="699dc-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="699dc-131">NOTES</span></span>

## <span data-ttu-id="699dc-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="699dc-132">RELATED LINKS</span></span>

