---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 59a5cbde2bde2c2cbe5834f73199c7b86791d247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732424"
---
# <span data-ttu-id="50860-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="50860-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="50860-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50860-102">SYNOPSIS</span></span>
<span data-ttu-id="50860-103">Создает план восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="50860-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50860-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50860-104">SYNTAX</span></span>

### <span data-ttu-id="50860-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50860-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50860-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="50860-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50860-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="50860-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50860-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50860-108">DESCRIPTION</span></span>
<span data-ttu-id="50860-109">Командлет **New-AzureRmRecoveryServicesAsrRecoveryPlan** создает план восстановления Azure Site Recovery в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="50860-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="50860-110">План восстановления позволяет собрать на устройстве виртуальные машины, принадлежащие приложению, чтобы их можно было восстановить вместе.</span><span class="sxs-lookup"><span data-stu-id="50860-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="50860-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50860-111">EXAMPLES</span></span>

### <span data-ttu-id="50860-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50860-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="50860-113">Запускает операцию создания плана восстановления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="50860-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="50860-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50860-114">PARAMETERS</span></span>

### <span data-ttu-id="50860-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="50860-115">-Azure</span></span>
<span data-ttu-id="50860-116">Параметр Switch, указывающий, что расположение для восстановления плана восстановления — Azure.</span><span class="sxs-lookup"><span data-stu-id="50860-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50860-117">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="50860-117">-FailoverDeploymentModel</span></span>
<span data-ttu-id="50860-118">Указывает модель развертывания для отработки отказа (классический или диспетчер ресурсов) для элементов, защищенных репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="50860-118">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50860-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="50860-119">-Name</span></span>
<span data-ttu-id="50860-120">Имя плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="50860-120">Name of the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50860-121">-Path</span><span class="sxs-lookup"><span data-stu-id="50860-121">-Path</span></span>
<span data-ttu-id="50860-122">Задает путь к файлу JSON определения плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="50860-122">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="50860-123">Чтобы создать план восстановления, можно использовать JSON с определением плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="50860-123">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50860-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="50860-124">-PrimaryFabric</span></span>
<span data-ttu-id="50860-125">Задает объект Fabric ASR для основной структуры ASR, защищенной репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="50860-125">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50860-126">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="50860-126">-RecoveryFabric</span></span>
<span data-ttu-id="50860-127">Указывает объект Fabric ASR для структуры восстановления ASR для элементов, защищенных репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="50860-127">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50860-128">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="50860-128">-ReplicationProtectedItem</span></span>
<span data-ttu-id="50860-129">Список элементов, защищенных репликацией, которые нужно добавить в первую группу плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="50860-129">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50860-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50860-130">-Confirm</span></span>
<span data-ttu-id="50860-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="50860-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50860-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50860-132">-WhatIf</span></span>
<span data-ttu-id="50860-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="50860-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50860-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="50860-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50860-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50860-135">CommonParameters</span></span>
<span data-ttu-id="50860-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50860-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50860-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50860-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50860-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50860-138">INPUTS</span></span>

### <span data-ttu-id="50860-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="50860-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="50860-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50860-140">OUTPUTS</span></span>

### <span data-ttu-id="50860-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="50860-141">System.Object</span></span>

## <span data-ttu-id="50860-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="50860-142">NOTES</span></span>

## <span data-ttu-id="50860-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50860-143">RELATED LINKS</span></span>

[<span data-ttu-id="50860-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="50860-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="50860-145">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="50860-145">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="50860-146">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="50860-146">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


