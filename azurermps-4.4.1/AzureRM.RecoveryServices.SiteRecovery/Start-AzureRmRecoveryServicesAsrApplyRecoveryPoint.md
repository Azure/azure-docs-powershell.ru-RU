---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 50015893c3bbd45196e4dde24088fe3ce8b595c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734252"
---
# <span data-ttu-id="ea857-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ea857-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="ea857-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea857-102">SYNOPSIS</span></span>
<span data-ttu-id="ea857-103">Изменяет точку восстановления для отработки отказа для защищенного элемента, прежде чем фиксировать операцию перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="ea857-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea857-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea857-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea857-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea857-105">DESCRIPTION</span></span>
<span data-ttu-id="ea857-106">**Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** изменяет точку восстановления для отработки отказа для защищенного элемента, прежде чем она зафиксирует операцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="ea857-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="ea857-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea857-107">EXAMPLES</span></span>

### <span data-ttu-id="ea857-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea857-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="ea857-109">Начинает применять указанную точку восстановления к элементу, защищенному репликацией, и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="ea857-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ea857-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea857-110">PARAMETERS</span></span>

### <span data-ttu-id="ea857-111">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ea857-111">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="ea857-112">Задает основной файл сертификата при использовании шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="ea857-112">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="ea857-113">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="ea857-113">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="ea857-114">Указывает вторичный файл сертификата, если используется шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="ea857-114">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="ea857-115">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="ea857-115">-RecoveryPoint</span></span>
<span data-ttu-id="ea857-116">Указывает объект точки восстановления, соответствующий применяемой точке восстановления.</span><span class="sxs-lookup"><span data-stu-id="ea857-116">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="ea857-117">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ea857-117">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ea857-118">Указывает объект защищенного элемента репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="ea857-118">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="ea857-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea857-119">-Confirm</span></span>
<span data-ttu-id="ea857-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea857-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea857-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea857-121">-WhatIf</span></span>
<span data-ttu-id="ea857-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea857-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea857-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea857-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea857-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea857-124">CommonParameters</span></span>
<span data-ttu-id="ea857-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea857-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea857-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea857-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea857-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea857-127">INPUTS</span></span>

### <span data-ttu-id="ea857-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ea857-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ea857-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea857-129">OUTPUTS</span></span>

### <span data-ttu-id="ea857-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ea857-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ea857-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea857-131">NOTES</span></span>

## <span data-ttu-id="ea857-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea857-132">RELATED LINKS</span></span>

[<span data-ttu-id="ea857-133">Командлеты Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="ea857-133">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
