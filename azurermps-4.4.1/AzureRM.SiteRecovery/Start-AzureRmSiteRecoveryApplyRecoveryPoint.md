---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: d77ed7723ef9875413c551912563b4ee2f4ae306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562083"
---
# <span data-ttu-id="77189-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="77189-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="77189-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77189-102">SYNOPSIS</span></span>
<span data-ttu-id="77189-103">Изменяет точку восстановления для отработки отказа для защищенного элемента, прежде чем фиксировать операцию перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="77189-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77189-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77189-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77189-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77189-105">DESCRIPTION</span></span>
<span data-ttu-id="77189-106">**Start-AzureRmSiteRecoveryApplyRecoveryPoint** изменяет точку восстановления для отработки отказа для защищенного элемента, прежде чем она зафиксирует операцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="77189-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="77189-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77189-107">EXAMPLES</span></span>

## <span data-ttu-id="77189-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77189-108">PARAMETERS</span></span>

### <span data-ttu-id="77189-109">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="77189-109">-DataEncryptionPrimaryCertFile</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77189-110">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="77189-110">-DataEncryptionSecondaryCertFile</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77189-111">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="77189-111">-RecoveryPoint</span></span>
<span data-ttu-id="77189-112">Указывает объект точки восстановления, измененный этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="77189-112">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77189-113">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="77189-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="77189-114">Указывает объект защищенного элемента репликации.</span><span class="sxs-lookup"><span data-stu-id="77189-114">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77189-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77189-115">-DefaultProfile</span></span>
<span data-ttu-id="77189-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77189-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77189-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77189-117">CommonParameters</span></span>
<span data-ttu-id="77189-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77189-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77189-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77189-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77189-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77189-120">INPUTS</span></span>

### <span data-ttu-id="77189-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="77189-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="77189-122">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="77189-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="77189-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77189-123">OUTPUTS</span></span>

### <span data-ttu-id="77189-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="77189-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="77189-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="77189-125">NOTES</span></span>

## <span data-ttu-id="77189-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77189-126">RELATED LINKS</span></span>

[<span data-ttu-id="77189-127">Командлеты Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="77189-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
