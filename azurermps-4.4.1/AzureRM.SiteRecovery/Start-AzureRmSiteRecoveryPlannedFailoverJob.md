---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: e723aacbfbd1b782a91fdc6aa589bfe15df42cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565119"
---
# <span data-ttu-id="1bded-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="1bded-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="1bded-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1bded-102">SYNOPSIS</span></span>
<span data-ttu-id="1bded-103">Запускает плановую операцию отработки отказа для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="1bded-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bded-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1bded-104">SYNTAX</span></span>

### <span data-ttu-id="1bded-105">ByPEObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1bded-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bded-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="1bded-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bded-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="1bded-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bded-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bded-108">DESCRIPTION</span></span>
<span data-ttu-id="1bded-109">Командлет **Start-AzureRmSiteRecoveryPlannedFailoverJob** запускает плановую отработку отказа для сущности или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1bded-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="1bded-110">С помощью командлета Get-AzureRmSiteRecoveryJob можно проверить, успешно ли прошло задание.</span><span class="sxs-lookup"><span data-stu-id="1bded-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="1bded-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1bded-111">EXAMPLES</span></span>

## <span data-ttu-id="1bded-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1bded-112">PARAMETERS</span></span>

### <span data-ttu-id="1bded-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="1bded-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="1bded-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1bded-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1bded-115">Кнопки</span><span class="sxs-lookup"><span data-stu-id="1bded-115">Yes</span></span>
- <span data-ttu-id="1bded-116">Нет</span><span class="sxs-lookup"><span data-stu-id="1bded-116">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bded-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1bded-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="1bded-118">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="1bded-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="1bded-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="1bded-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="1bded-120">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="1bded-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="1bded-121">-Направление</span><span class="sxs-lookup"><span data-stu-id="1bded-121">-Direction</span></span>
<span data-ttu-id="1bded-122">Указывает направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="1bded-122">Specifies the direction of the failover.</span></span>
<span data-ttu-id="1bded-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1bded-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1bded-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="1bded-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="1bded-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="1bded-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="1bded-126">-OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="1bded-126">-Optimize</span></span>
<span data-ttu-id="1bded-127">Указывает, для чего нужно оптимизировать.</span><span class="sxs-lookup"><span data-stu-id="1bded-127">Specifies what to optimize for.</span></span>
<span data-ttu-id="1bded-128">Этот параметр применяется в том случае, если отработка отказа выполняется с сайта Azure на локальном сайте, для которого требуется значительная синхронизация данных.</span><span class="sxs-lookup"><span data-stu-id="1bded-128">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="1bded-129">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="1bded-129">Valid values are:</span></span>

- <span data-ttu-id="1bded-130">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="1bded-130">ForDowntime</span></span>
- <span data-ttu-id="1bded-131">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="1bded-131">ForSynchronization</span></span>

<span data-ttu-id="1bded-132">Если указан **ForDowntime** , это указывает на то, что данные синхронизируются перед переходом на другой ресурс для минимизации простоев.</span><span class="sxs-lookup"><span data-stu-id="1bded-132">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="1bded-133">Синхронизация выполняется без выключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1bded-133">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="1bded-134">После завершения синхронизации задание будет приостановлено.</span><span class="sxs-lookup"><span data-stu-id="1bded-134">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="1bded-135">Возобновите задачу, чтобы выполнить дополнительную операцию синхронизации, которая завершает работу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1bded-135">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="1bded-136">Если указан **ForSynchronization** , это указывает на то, что данные синхронизируются во время отработки отказа, поэтому синхронизация данных свернута.</span><span class="sxs-lookup"><span data-stu-id="1bded-136">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="1bded-137">Если этот параметр включен, виртуальная машина немедленно завершает работу.</span><span class="sxs-lookup"><span data-stu-id="1bded-137">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="1bded-138">Синхронизация начинается после завершения работы, чтобы завершить операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="1bded-138">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bded-139">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1bded-139">-ProtectionEntity</span></span>
<span data-ttu-id="1bded-140">Указывает объект сущности для защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="1bded-140">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="1bded-141">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1bded-141">-RecoveryPlan</span></span>
<span data-ttu-id="1bded-142">Указывает объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="1bded-142">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="1bded-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1bded-143">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="1bded-144">-Сервер</span><span class="sxs-lookup"><span data-stu-id="1bded-144">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bded-145">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1bded-145">-ServicesProvider</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bded-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bded-146">-DefaultProfile</span></span>
<span data-ttu-id="1bded-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1bded-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bded-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bded-148">CommonParameters</span></span>
<span data-ttu-id="1bded-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1bded-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bded-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bded-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bded-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1bded-151">INPUTS</span></span>

### <span data-ttu-id="1bded-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="1bded-152">ASRProtectionEntity</span></span>
<span data-ttu-id="1bded-153">Параметр "ProtectionEntity" принимает значение типа "ASRProtectionEntity" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1bded-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="1bded-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1bded-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="1bded-155">Параметр "RecoveryPlan" принимает значение типа "ASRRecoveryPlan" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1bded-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="1bded-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1bded-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="1bded-157">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="1bded-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="1bded-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bded-158">OUTPUTS</span></span>

### <span data-ttu-id="1bded-159">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1bded-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1bded-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="1bded-160">NOTES</span></span>

## <span data-ttu-id="1bded-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bded-161">RELATED LINKS</span></span>

