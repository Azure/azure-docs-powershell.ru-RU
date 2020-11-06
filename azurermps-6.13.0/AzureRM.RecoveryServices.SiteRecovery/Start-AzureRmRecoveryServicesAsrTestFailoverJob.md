---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrtestfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrTestFailoverJob.md
ms.openlocfilehash: f0350cfa9facfe8fc21e6c039c2fa5838bba8875
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564095"
---
# <span data-ttu-id="a25eb-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="a25eb-101">Start-AzureRmRecoveryServicesAsrTestFailoverJob</span></span>

## <span data-ttu-id="a25eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a25eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a25eb-103">Запускает тестовую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="a25eb-103">Starts a test failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a25eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a25eb-104">SYNTAX</span></span>

### <span data-ttu-id="a25eb-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a25eb-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a25eb-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="a25eb-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a25eb-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="a25eb-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a25eb-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a25eb-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a25eb-109">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="a25eb-109">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a25eb-110">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a25eb-110">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmRecoveryServicesAsrTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-CloudServiceCreationOption <String>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-RecoveryPoint <ASRRecoveryPoint>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a25eb-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a25eb-111">DESCRIPTION</span></span>
<span data-ttu-id="a25eb-112">Командлет **Start-AzureRmRecoveryServicesAsrTestFailoverJob** запускает проверку отработки отказа для защищенного элемента или плана восстановления Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a25eb-112">The **Start-AzureRmRecoveryServicesAsrTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="a25eb-113">Вы можете проверить, завершилось ли задание успешно с помощью командлета Get-AzureRmRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="a25eb-113">You can check whether the job succeeded by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="a25eb-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a25eb-114">EXAMPLES</span></span>

### <span data-ttu-id="a25eb-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a25eb-115">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrTestFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $TestRecoveryNetwork
```

<span data-ttu-id="a25eb-116">Запускает тестовую операцию отработки отказа для плана восстановления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="a25eb-116">Starts the test failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a25eb-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a25eb-117">PARAMETERS</span></span>

### <span data-ttu-id="a25eb-118">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a25eb-118">-AzureVMNetworkId</span></span>
<span data-ttu-id="a25eb-119">Указывает идентификатор виртуальной сети Azure для подключения теста со сбоем для проверки поверх виртуальных машин (-ов).</span><span class="sxs-lookup"><span data-stu-id="a25eb-119">Specifies the Azure virtual network ID to connect the test fail over virtual machine(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25eb-120">-CloudServiceCreationOption</span><span class="sxs-lookup"><span data-stu-id="a25eb-120">-CloudServiceCreationOption</span></span>
<span data-ttu-id="a25eb-121">Указывает, следует ли создавать новую облачную службу или использовать облачную службу восстановления, настроенную для виртуальной машины, для тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="a25eb-121">Specifies whether a new cloud service should be created or the recovery cloud service configured for the VM should be used for the test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, ByRPObject, ByRPObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases:
Accepted values: UseRecoveryCloudService, AutoCreateCloudService

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25eb-122">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="a25eb-122">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="a25eb-123">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="a25eb-123">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="a25eb-124">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="a25eb-124">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="a25eb-125">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="a25eb-125">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="a25eb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a25eb-126">-DefaultProfile</span></span>
<span data-ttu-id="a25eb-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a25eb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a25eb-128">-Направление</span><span class="sxs-lookup"><span data-stu-id="a25eb-128">-Direction</span></span>
<span data-ttu-id="a25eb-129">Указывает направление перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="a25eb-129">Specifies the failover direction.</span></span>
<span data-ttu-id="a25eb-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a25eb-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a25eb-131">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="a25eb-131">PrimaryToRecovery</span></span>
- <span data-ttu-id="a25eb-132">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="a25eb-132">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="a25eb-133">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a25eb-133">-RecoveryPlan</span></span>
<span data-ttu-id="a25eb-134">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="a25eb-134">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a25eb-135">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a25eb-135">-RecoveryPoint</span></span>
<span data-ttu-id="a25eb-136">Задает настраиваемую точку восстановления для проверки отработки отказа, на которую защищенный компьютер.</span><span class="sxs-lookup"><span data-stu-id="a25eb-136">Specifies a custom recovery point to test failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25eb-137">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="a25eb-137">-RecoveryTag</span></span>
<span data-ttu-id="a25eb-138">Указывает тег восстановления для проверки отработки отказа на</span><span class="sxs-lookup"><span data-stu-id="a25eb-138">Specifies the recovery tag to test failover to</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25eb-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a25eb-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a25eb-140">Задает защищенный элемент репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="a25eb-140">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a25eb-141">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="a25eb-141">-VMNetwork</span></span>
<span data-ttu-id="a25eb-142">Указывает сеть виртуальной машины для восстановления сайта для подключения тестовых виртуальных машин для отработки отказа (-ов).</span><span class="sxs-lookup"><span data-stu-id="a25eb-142">Specifies the Site Recovery virtual machine network to connect the test failover virtual machine(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25eb-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a25eb-143">-Confirm</span></span>
<span data-ttu-id="a25eb-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a25eb-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25eb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a25eb-145">-WhatIf</span></span>
<span data-ttu-id="a25eb-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a25eb-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a25eb-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a25eb-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25eb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25eb-148">CommonParameters</span></span>
<span data-ttu-id="a25eb-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a25eb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25eb-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a25eb-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25eb-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a25eb-151">INPUTS</span></span>

### <span data-ttu-id="a25eb-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a25eb-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="a25eb-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a25eb-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a25eb-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a25eb-154">OUTPUTS</span></span>

### <span data-ttu-id="a25eb-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a25eb-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a25eb-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="a25eb-156">NOTES</span></span>

## <span data-ttu-id="a25eb-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a25eb-157">RELATED LINKS</span></span>

[<span data-ttu-id="a25eb-158">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="a25eb-158">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)
