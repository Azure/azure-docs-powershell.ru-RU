---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint.md
ms.openlocfilehash: 2afdc351c50e42ec5b2f67208d2be2af9f024813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557240"
---
# <span data-ttu-id="48c9b-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="48c9b-101">Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint</span></span>

## <span data-ttu-id="48c9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="48c9b-103">Изменяет точку восстановления для отработки отказа для защищенного элемента, прежде чем фиксировать операцию перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="48c9b-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48c9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48c9b-104">SYNTAX</span></span>

```
Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48c9b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48c9b-105">DESCRIPTION</span></span>
<span data-ttu-id="48c9b-106">**Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** изменяет точку восстановления для отработки отказа для защищенного элемента, прежде чем она зафиксирует операцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="48c9b-106">The **Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint** changes the recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="48c9b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48c9b-107">EXAMPLES</span></span>

### <span data-ttu-id="48c9b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="48c9b-108">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint -RecoveryPoint $RecoveryPoint -ReplicationProtectedItem $RPI
```

<span data-ttu-id="48c9b-109">Начинает применять указанную точку восстановления к элементу, защищенному репликацией, и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="48c9b-109">Starts applying the specified recovery point to the replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="48c9b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48c9b-110">PARAMETERS</span></span>

### <span data-ttu-id="48c9b-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48c9b-111">-Confirm</span></span>
<span data-ttu-id="48c9b-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48c9b-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48c9b-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="48c9b-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="48c9b-114">Задает основной файл сертификата при использовании шифрования данных.</span><span class="sxs-lookup"><span data-stu-id="48c9b-114">Specifies the primary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="48c9b-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="48c9b-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="48c9b-116">Указывает вторичный файл сертификата, если используется шифрование данных.</span><span class="sxs-lookup"><span data-stu-id="48c9b-116">Specifies the secondary certificate file if data encryption is being used.</span></span>

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

### <span data-ttu-id="48c9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c9b-117">-DefaultProfile</span></span>
<span data-ttu-id="48c9b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48c9b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="48c9b-119">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="48c9b-119">-RecoveryPoint</span></span>
<span data-ttu-id="48c9b-120">Указывает объект точки восстановления, соответствующий применяемой точке восстановления.</span><span class="sxs-lookup"><span data-stu-id="48c9b-120">Specifies the recovery point object corresponding to the recovery point to be applied.</span></span>

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

### <span data-ttu-id="48c9b-121">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="48c9b-121">-ReplicationProtectedItem</span></span>
<span data-ttu-id="48c9b-122">Указывает объект защищенного элемента репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="48c9b-122">Specifies the ASR replication protected item object.</span></span>

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

### <span data-ttu-id="48c9b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48c9b-123">-WhatIf</span></span>
<span data-ttu-id="48c9b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48c9b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48c9b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48c9b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48c9b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c9b-126">CommonParameters</span></span>
<span data-ttu-id="48c9b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48c9b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c9b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48c9b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c9b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48c9b-129">INPUTS</span></span>

### <span data-ttu-id="48c9b-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="48c9b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="48c9b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48c9b-131">OUTPUTS</span></span>

### <span data-ttu-id="48c9b-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="48c9b-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="48c9b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="48c9b-133">NOTES</span></span>

## <span data-ttu-id="48c9b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48c9b-134">RELATED LINKS</span></span>

[<span data-ttu-id="48c9b-135">Командлеты Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="48c9b-135">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
