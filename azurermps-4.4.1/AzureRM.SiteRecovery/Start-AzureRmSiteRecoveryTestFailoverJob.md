---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 330af3701741cbc83573afbbe7e283fdee294cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568288"
---
# <span data-ttu-id="c61c9-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="c61c9-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="c61c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c61c9-102">SYNOPSIS</span></span>
<span data-ttu-id="c61c9-103">Запуск тестовой отработки отказа для объекта защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="c61c9-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c61c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c61c9-104">SYNTAX</span></span>

### <span data-ttu-id="c61c9-105">ByPEObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c61c9-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c61c9-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c61c9-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c61c9-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="c61c9-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c61c9-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="c61c9-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c61c9-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="c61c9-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c61c9-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="c61c9-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c61c9-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="c61c9-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c61c9-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="c61c9-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c61c9-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="c61c9-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c61c9-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c61c9-114">DESCRIPTION</span></span>
<span data-ttu-id="c61c9-115">Командлет **Start-AzureRmSiteRecoveryTestFailoverJob** запускает проверку отработки отказа для сущности или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c61c9-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="c61c9-116">Вы можете проверить, завершилось ли задание успешно с помощью командлета Get-AzureRmSiteRecoveryJob.</span><span class="sxs-lookup"><span data-stu-id="c61c9-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="c61c9-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c61c9-117">EXAMPLES</span></span>

## <span data-ttu-id="c61c9-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c61c9-118">PARAMETERS</span></span>

### <span data-ttu-id="c61c9-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="c61c9-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="c61c9-120">Указывает идентификатор виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="c61c9-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61c9-121">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="c61c9-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="c61c9-122">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="c61c9-122">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="c61c9-123">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="c61c9-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="c61c9-124">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="c61c9-124">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="c61c9-125">-Направление</span><span class="sxs-lookup"><span data-stu-id="c61c9-125">-Direction</span></span>
<span data-ttu-id="c61c9-126">Указывает направление перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="c61c9-126">Specifies the failover direction.</span></span>
<span data-ttu-id="c61c9-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c61c9-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c61c9-128">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="c61c9-128">PrimaryToRecovery</span></span>
- <span data-ttu-id="c61c9-129">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="c61c9-129">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="c61c9-130">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c61c9-130">-ProtectionEntity</span></span>
<span data-ttu-id="c61c9-131">Указывает объект сущности для защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="c61c9-131">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c61c9-132">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c61c9-132">-RecoveryPlan</span></span>
<span data-ttu-id="c61c9-133">Указывает объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="c61c9-133">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c61c9-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c61c9-134">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c61c9-135">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="c61c9-135">-VMNetwork</span></span>
<span data-ttu-id="c61c9-136">Указывает сеть виртуальной машины для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="c61c9-136">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61c9-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c61c9-137">-DefaultProfile</span></span>
<span data-ttu-id="c61c9-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c61c9-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c61c9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61c9-139">CommonParameters</span></span>
<span data-ttu-id="c61c9-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c61c9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61c9-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c61c9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61c9-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c61c9-142">INPUTS</span></span>

### <span data-ttu-id="c61c9-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c61c9-143">ASRProtectionEntity</span></span>
<span data-ttu-id="c61c9-144">Параметр "ProtectionEntity" принимает значение типа "ASRProtectionEntity" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c61c9-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="c61c9-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c61c9-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="c61c9-146">Параметр "RecoveryPlan" принимает значение типа "ASRRecoveryPlan" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c61c9-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="c61c9-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c61c9-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="c61c9-148">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c61c9-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="c61c9-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c61c9-149">OUTPUTS</span></span>

### <span data-ttu-id="c61c9-150">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c61c9-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c61c9-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="c61c9-151">NOTES</span></span>

## <span data-ttu-id="c61c9-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c61c9-152">RELATED LINKS</span></span>

[<span data-ttu-id="c61c9-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="c61c9-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
