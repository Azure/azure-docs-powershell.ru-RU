---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoverytestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 236ba6a3cbf65786af7d17e587ef5de0af86a296
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558795"
---
# <span data-ttu-id="78b4c-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="78b4c-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="78b4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78b4c-102">SYNOPSIS</span></span>
<span data-ttu-id="78b4c-103">Запуск тестовой отработки отказа для объекта защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="78b4c-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78b4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78b4c-104">SYNTAX</span></span>

### <span data-ttu-id="78b4c-105">ByPEObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78b4c-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78b4c-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="78b4c-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78b4c-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="78b4c-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78b4c-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="78b4c-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78b4c-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="78b4c-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78b4c-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="78b4c-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78b4c-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="78b4c-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78b4c-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="78b4c-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78b4c-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="78b4c-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78b4c-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78b4c-114">DESCRIPTION</span></span>
<span data-ttu-id="78b4c-115">Командлет **Start-AzureRmSiteRecoveryTestFailoverJob** запускает проверку отработки отказа для сущности или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="78b4c-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="78b4c-116">Вы можете проверить, завершилось ли задание успешно с помощью командлета Get-AzureRmSiteRecoveryJob.</span><span class="sxs-lookup"><span data-stu-id="78b4c-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="78b4c-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78b4c-117">EXAMPLES</span></span>

## <span data-ttu-id="78b4c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78b4c-118">PARAMETERS</span></span>

### <span data-ttu-id="78b4c-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="78b4c-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="78b4c-120">Указывает идентификатор виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="78b4c-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b4c-121">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="78b4c-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="78b4c-122">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="78b4c-122">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="78b4c-123">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="78b4c-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="78b4c-124">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="78b4c-124">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="78b4c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b4c-125">-DefaultProfile</span></span>
<span data-ttu-id="78b4c-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78b4c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78b4c-127">-Направление</span><span class="sxs-lookup"><span data-stu-id="78b4c-127">-Direction</span></span>
<span data-ttu-id="78b4c-128">Указывает направление перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="78b4c-128">Specifies the failover direction.</span></span>
<span data-ttu-id="78b4c-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="78b4c-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78b4c-130">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="78b4c-130">PrimaryToRecovery</span></span>
- <span data-ttu-id="78b4c-131">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="78b4c-131">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="78b4c-132">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="78b4c-132">-ProtectionEntity</span></span>
<span data-ttu-id="78b4c-133">Указывает объект сущности для защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="78b4c-133">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78b4c-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="78b4c-134">-RecoveryPlan</span></span>
<span data-ttu-id="78b4c-135">Указывает объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="78b4c-135">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78b4c-136">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="78b4c-136">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78b4c-137">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="78b4c-137">-VMNetwork</span></span>
<span data-ttu-id="78b4c-138">Указывает сеть виртуальной машины для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="78b4c-138">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78b4c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b4c-139">CommonParameters</span></span>
<span data-ttu-id="78b4c-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78b4c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b4c-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78b4c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b4c-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78b4c-142">INPUTS</span></span>

### <span data-ttu-id="78b4c-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="78b4c-143">ASRProtectionEntity</span></span>
<span data-ttu-id="78b4c-144">Параметр "ProtectionEntity" принимает значение типа "ASRProtectionEntity" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="78b4c-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="78b4c-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="78b4c-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="78b4c-146">Параметр "RecoveryPlan" принимает значение типа "ASRRecoveryPlan" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="78b4c-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="78b4c-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="78b4c-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="78b4c-148">Параметр "ReplicationProtectedItem" принимает значение типа "ASRReplicationProtectedItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="78b4c-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="78b4c-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78b4c-149">OUTPUTS</span></span>

### <span data-ttu-id="78b4c-150">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="78b4c-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="78b4c-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="78b4c-151">NOTES</span></span>

## <span data-ttu-id="78b4c-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78b4c-152">RELATED LINKS</span></span>

[<span data-ttu-id="78b4c-153">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="78b4c-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
