---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: 1776ec34517d613daf805fac97ecda93c1afe542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557124"
---
# <span data-ttu-id="79398-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="79398-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="79398-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79398-102">SYNOPSIS</span></span>
<span data-ttu-id="79398-103">Запускает внеплановая отработка отказа для объекта защиты восстановления сайта или плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="79398-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79398-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79398-104">SYNTAX</span></span>

### <span data-ttu-id="79398-105">ByPEObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79398-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79398-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="79398-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79398-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="79398-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79398-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79398-108">DESCRIPTION</span></span>
<span data-ttu-id="79398-109">Командлет **Start-AzureRmSiteRecoveryUnplannedFailoverJob** запускает внеплановую отработку отказа для сущности или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="79398-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="79398-110">С помощью командлета Get-AzureRmSiteRecoveryJob можно проверить, успешно ли прошло задание.</span><span class="sxs-lookup"><span data-stu-id="79398-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="79398-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79398-111">EXAMPLES</span></span>

## <span data-ttu-id="79398-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79398-112">PARAMETERS</span></span>

### <span data-ttu-id="79398-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="79398-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="79398-114">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="79398-114">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="79398-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="79398-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="79398-116">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="79398-116">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="79398-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79398-117">-DefaultProfile</span></span>
<span data-ttu-id="79398-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79398-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79398-119">-Направление</span><span class="sxs-lookup"><span data-stu-id="79398-119">-Direction</span></span>
<span data-ttu-id="79398-120">Указывает направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="79398-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="79398-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="79398-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79398-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="79398-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="79398-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="79398-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="79398-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="79398-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="79398-125">Указывает на то, что действие может выполнять операции с исходным сайтом.</span><span class="sxs-lookup"><span data-stu-id="79398-125">Indicates that the action can perform source site operations.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79398-126">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="79398-126">-ProtectionEntity</span></span>
<span data-ttu-id="79398-127">Указывает объект сущности для защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="79398-127">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="79398-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="79398-128">-RecoveryPlan</span></span>
<span data-ttu-id="79398-129">Указывает объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="79398-129">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="79398-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="79398-130">-ReplicationProtectedItem</span></span>
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

### <span data-ttu-id="79398-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79398-131">CommonParameters</span></span>
<span data-ttu-id="79398-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79398-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79398-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79398-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79398-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79398-134">INPUTS</span></span>

### <span data-ttu-id="79398-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="79398-135">ASRProtectionEntity</span></span>
<span data-ttu-id="79398-136">Параметр "ProtectionEntity" принимает значение типа "ASRProtectionEntity" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="79398-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="79398-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="79398-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="79398-138">Параметр "RecoveryPlan" принимает значение типа "ASRRecoveryPlan" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="79398-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="79398-139">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="79398-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="79398-140">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="79398-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="79398-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79398-141">OUTPUTS</span></span>

### <span data-ttu-id="79398-142">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="79398-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="79398-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="79398-143">NOTES</span></span>

## <span data-ttu-id="79398-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79398-144">RELATED LINKS</span></span>

[<span data-ttu-id="79398-145">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="79398-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)


