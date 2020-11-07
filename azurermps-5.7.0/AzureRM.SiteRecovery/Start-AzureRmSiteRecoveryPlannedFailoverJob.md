---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: f5bf4372c1140402cb56ca875b5532387dd06704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733955"
---
# <span data-ttu-id="8abbb-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="8abbb-101">Start-AzureRmSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="8abbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8abbb-102">SYNOPSIS</span></span>
<span data-ttu-id="8abbb-103">Запускает плановую операцию отработки отказа для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="8abbb-103">Starts a Site Recovery planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8abbb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8abbb-104">SYNTAX</span></span>

### <span data-ttu-id="8abbb-105">ByPEObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8abbb-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8abbb-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="8abbb-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8abbb-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="8abbb-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8abbb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8abbb-108">DESCRIPTION</span></span>
<span data-ttu-id="8abbb-109">Командлет **Start-AzureRmSiteRecoveryPlannedFailoverJob** запускает плановую отработку отказа для сущности или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8abbb-109">The **Start-AzureRmSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="8abbb-110">С помощью командлета Get-AzureRmSiteRecoveryJob можно проверить, успешно ли прошло задание.</span><span class="sxs-lookup"><span data-stu-id="8abbb-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="8abbb-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8abbb-111">EXAMPLES</span></span>

## <span data-ttu-id="8abbb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8abbb-112">PARAMETERS</span></span>

### <span data-ttu-id="8abbb-113">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="8abbb-113">-CreateVmIfNotFound</span></span>
<span data-ttu-id="8abbb-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8abbb-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8abbb-115">Кнопки</span><span class="sxs-lookup"><span data-stu-id="8abbb-115">Yes</span></span>
- <span data-ttu-id="8abbb-116">Нет</span><span class="sxs-lookup"><span data-stu-id="8abbb-116">No</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8abbb-117">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8abbb-117">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="8abbb-118">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="8abbb-118">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="8abbb-119">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8abbb-119">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="8abbb-120">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="8abbb-120">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="8abbb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8abbb-121">-DefaultProfile</span></span>
<span data-ttu-id="8abbb-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8abbb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8abbb-123">-Направление</span><span class="sxs-lookup"><span data-stu-id="8abbb-123">-Direction</span></span>
<span data-ttu-id="8abbb-124">Указывает направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="8abbb-124">Specifies the direction of the failover.</span></span>
<span data-ttu-id="8abbb-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8abbb-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8abbb-126">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="8abbb-126">PrimaryToRecovery</span></span>
- <span data-ttu-id="8abbb-127">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="8abbb-127">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8abbb-128">-OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="8abbb-128">-Optimize</span></span>
<span data-ttu-id="8abbb-129">Указывает, для чего нужно оптимизировать.</span><span class="sxs-lookup"><span data-stu-id="8abbb-129">Specifies what to optimize for.</span></span>
<span data-ttu-id="8abbb-130">Этот параметр применяется в том случае, если отработка отказа выполняется с сайта Azure на локальном сайте, для которого требуется значительная синхронизация данных.</span><span class="sxs-lookup"><span data-stu-id="8abbb-130">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="8abbb-131">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="8abbb-131">Valid values are:</span></span>

- <span data-ttu-id="8abbb-132">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="8abbb-132">ForDowntime</span></span>
- <span data-ttu-id="8abbb-133">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="8abbb-133">ForSynchronization</span></span>

<span data-ttu-id="8abbb-134">Если указан **ForDowntime** , это указывает на то, что данные синхронизируются перед переходом на другой ресурс для минимизации простоев.</span><span class="sxs-lookup"><span data-stu-id="8abbb-134">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="8abbb-135">Синхронизация выполняется без выключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8abbb-135">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="8abbb-136">После завершения синхронизации задание будет приостановлено.</span><span class="sxs-lookup"><span data-stu-id="8abbb-136">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="8abbb-137">Возобновите задачу, чтобы выполнить дополнительную операцию синхронизации, которая завершает работу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8abbb-137">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="8abbb-138">Если указан **ForSynchronization** , это указывает на то, что данные синхронизируются во время отработки отказа, поэтому синхронизация данных свернута.</span><span class="sxs-lookup"><span data-stu-id="8abbb-138">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="8abbb-139">Если этот параметр включен, виртуальная машина немедленно завершает работу.</span><span class="sxs-lookup"><span data-stu-id="8abbb-139">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="8abbb-140">Синхронизация начинается после завершения работы, чтобы завершить операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="8abbb-140">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8abbb-141">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="8abbb-141">-ProtectionEntity</span></span>
<span data-ttu-id="8abbb-142">Указывает объект сущности для защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="8abbb-142">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8abbb-143">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8abbb-143">-RecoveryPlan</span></span>
<span data-ttu-id="8abbb-144">Указывает объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="8abbb-144">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8abbb-145">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8abbb-145">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8abbb-146">-Сервер</span><span class="sxs-lookup"><span data-stu-id="8abbb-146">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8abbb-147">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8abbb-147">-ServicesProvider</span></span>
```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8abbb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8abbb-148">CommonParameters</span></span>
<span data-ttu-id="8abbb-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8abbb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8abbb-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8abbb-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8abbb-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8abbb-151">INPUTS</span></span>

### <span data-ttu-id="8abbb-152">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="8abbb-152">ASRProtectionEntity</span></span>
<span data-ttu-id="8abbb-153">Параметр "ProtectionEntity" принимает значение типа "ASRProtectionEntity" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8abbb-153">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="8abbb-154">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8abbb-154">ASRRecoveryPlan</span></span>
<span data-ttu-id="8abbb-155">Параметр "RecoveryPlan" принимает значение типа "ASRRecoveryPlan" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8abbb-155">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="8abbb-156">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8abbb-156">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="8abbb-157">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8abbb-157">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="8abbb-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8abbb-158">OUTPUTS</span></span>

### <span data-ttu-id="8abbb-159">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8abbb-159">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8abbb-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="8abbb-160">NOTES</span></span>

## <span data-ttu-id="8abbb-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8abbb-161">RELATED LINKS</span></span>

