---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: a0a6ee7f0430453aef343ba971126cd9aff63f6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559492"
---
# <span data-ttu-id="73312-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="73312-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="73312-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73312-102">SYNOPSIS</span></span>
<span data-ttu-id="73312-103">Запускает внеплановая отработка отказа для объекта защиты восстановления сайта или плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="73312-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73312-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73312-104">SYNTAX</span></span>

### <span data-ttu-id="73312-105">ByPEObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73312-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73312-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="73312-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73312-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="73312-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73312-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73312-108">DESCRIPTION</span></span>
<span data-ttu-id="73312-109">Командлет **Start-AzureRmSiteRecoveryUnplannedFailoverJob** запускает внеплановую отработку отказа для сущности или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="73312-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="73312-110">С помощью командлета Get-AzureRmSiteRecoveryJob можно проверить, успешно ли прошло задание.</span><span class="sxs-lookup"><span data-stu-id="73312-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="73312-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73312-111">EXAMPLES</span></span>

## <span data-ttu-id="73312-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73312-112">PARAMETERS</span></span>

### <span data-ttu-id="73312-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="73312-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="73312-114">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="73312-114">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="73312-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="73312-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="73312-116">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="73312-116">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="73312-117">-Направление</span><span class="sxs-lookup"><span data-stu-id="73312-117">-Direction</span></span>
<span data-ttu-id="73312-118">Указывает направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="73312-118">Specifies the direction of the failover.</span></span>
<span data-ttu-id="73312-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="73312-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="73312-120">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="73312-120">PrimaryToRecovery</span></span>
- <span data-ttu-id="73312-121">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="73312-121">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73312-122">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="73312-122">-PerformSourceSideActions</span></span>
<span data-ttu-id="73312-123">Указывает на то, что действие может выполнять операции с исходным сайтом.</span><span class="sxs-lookup"><span data-stu-id="73312-123">Indicates that the action can perform source site operations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73312-124">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="73312-124">-ProtectionEntity</span></span>
<span data-ttu-id="73312-125">Указывает объект сущности для защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="73312-125">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="73312-126">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73312-126">-RecoveryPlan</span></span>
<span data-ttu-id="73312-127">Указывает объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="73312-127">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="73312-128">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="73312-128">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="73312-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73312-129">-DefaultProfile</span></span>
<span data-ttu-id="73312-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73312-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73312-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73312-131">CommonParameters</span></span>
<span data-ttu-id="73312-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73312-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73312-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73312-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73312-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73312-134">INPUTS</span></span>

### <span data-ttu-id="73312-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="73312-135">ASRProtectionEntity</span></span>
<span data-ttu-id="73312-136">Параметр "ProtectionEntity" принимает значение типа "ASRProtectionEntity" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="73312-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="73312-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="73312-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="73312-138">Параметр "RecoveryPlan" принимает значение типа "ASRRecoveryPlan" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="73312-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="73312-139">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="73312-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="73312-140">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="73312-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="73312-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73312-141">OUTPUTS</span></span>

### <span data-ttu-id="73312-142">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="73312-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="73312-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="73312-143">NOTES</span></span>

## <span data-ttu-id="73312-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73312-144">RELATED LINKS</span></span>

[<span data-ttu-id="73312-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="73312-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)


