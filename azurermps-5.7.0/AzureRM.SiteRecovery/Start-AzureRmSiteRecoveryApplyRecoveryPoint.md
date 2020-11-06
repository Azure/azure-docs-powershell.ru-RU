---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: 97ebacf9f5c51778122bfb8e8157692b7f1dfd03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567877"
---
# <span data-ttu-id="cbbaf-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="cbbaf-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="cbbaf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cbbaf-102">SYNOPSIS</span></span>
<span data-ttu-id="cbbaf-103">Изменяет точку восстановления для отработки отказа для защищенного элемента, прежде чем фиксировать операцию перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="cbbaf-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbbaf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cbbaf-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbbaf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbbaf-105">DESCRIPTION</span></span>
<span data-ttu-id="cbbaf-106">**Start-AzureRmSiteRecoveryApplyRecoveryPoint** изменяет точку восстановления для отработки отказа для защищенного элемента, прежде чем она зафиксирует операцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="cbbaf-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="cbbaf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cbbaf-107">EXAMPLES</span></span>

## <span data-ttu-id="cbbaf-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cbbaf-108">PARAMETERS</span></span>

### <span data-ttu-id="cbbaf-109">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="cbbaf-109">-DataEncryptionPrimaryCertFile</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbaf-110">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="cbbaf-110">-DataEncryptionSecondaryCertFile</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbaf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbbaf-111">-DefaultProfile</span></span>
<span data-ttu-id="cbbaf-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cbbaf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbaf-113">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="cbbaf-113">-RecoveryPoint</span></span>
<span data-ttu-id="cbbaf-114">Указывает объект точки восстановления, измененный этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="cbbaf-114">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbbaf-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cbbaf-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="cbbaf-116">Указывает объект защищенного элемента репликации.</span><span class="sxs-lookup"><span data-stu-id="cbbaf-116">Specifies the Replication Protected Item object.</span></span>

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

### <span data-ttu-id="cbbaf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbbaf-117">CommonParameters</span></span>
<span data-ttu-id="cbbaf-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cbbaf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbbaf-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbbaf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbbaf-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cbbaf-120">INPUTS</span></span>

### <span data-ttu-id="cbbaf-121">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cbbaf-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="cbbaf-122">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cbbaf-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="cbbaf-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbbaf-123">OUTPUTS</span></span>

### <span data-ttu-id="cbbaf-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cbbaf-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cbbaf-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="cbbaf-125">NOTES</span></span>

## <span data-ttu-id="cbbaf-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbbaf-126">RELATED LINKS</span></span>

[<span data-ttu-id="cbbaf-127">Командлеты Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="cbbaf-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
