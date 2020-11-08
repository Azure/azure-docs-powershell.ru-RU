---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078071"
---
# <span data-ttu-id="24e79-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="24e79-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="24e79-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24e79-102">SYNOPSIS</span></span>
<span data-ttu-id="24e79-103">Создает план восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="24e79-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="24e79-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24e79-104">SYNTAX</span></span>

### <span data-ttu-id="24e79-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24e79-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24e79-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="24e79-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24e79-107">AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="24e79-107">AzureZoneToZone</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24e79-108">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="24e79-108">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24e79-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24e79-109">DESCRIPTION</span></span>
<span data-ttu-id="24e79-110">Командлет **New-AzRecoveryServicesAsrRecoveryPlan** создает восстановление сайта Azure, план восстановления в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="24e79-110">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="24e79-111">План восстановления позволяет собрать на устройстве виртуальные машины, принадлежащие приложению, чтобы их можно было восстановить вместе.</span><span class="sxs-lookup"><span data-stu-id="24e79-111">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="24e79-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24e79-112">EXAMPLES</span></span>

### <span data-ttu-id="24e79-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="24e79-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="24e79-114">Запускает операцию создания плана восстановления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="24e79-114">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="24e79-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="24e79-115">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

<span data-ttu-id="24e79-116">Запускает операцию создания плана восстановления для зоны Azure с реплицированными элементами зоны и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="24e79-116">Starts the recovery plan creation operation for Azure zone to zone replicated items and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="24e79-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24e79-117">PARAMETERS</span></span>

### <span data-ttu-id="24e79-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="24e79-118">-Azure</span></span>
<span data-ttu-id="24e79-119">Параметр Switch задает сценарий для восстановления с помощью Azure для Azure, создание плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="24e79-119">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e79-120">-AzureZoneToZone</span><span class="sxs-lookup"><span data-stu-id="24e79-120">-AzureZoneToZone</span></span>
<span data-ttu-id="24e79-121">Параметр Switch указывает на необходимость создания реплицируемого элемента в зоне Azure для зоны.</span><span class="sxs-lookup"><span data-stu-id="24e79-121">Switch parameter specifies creating the replicated item in azure zone to zone scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e79-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e79-122">-DefaultProfile</span></span>
<span data-ttu-id="24e79-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24e79-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e79-124">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="24e79-124">-FailoverDeploymentModel</span></span>
<span data-ttu-id="24e79-125">Указывает модель развертывания для отработки отказа (классический или диспетчер ресурсов) для элементов, защищенных репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="24e79-125">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e79-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="24e79-126">-Name</span></span>
<span data-ttu-id="24e79-127">Имя плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="24e79-127">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e79-128">-Path</span><span class="sxs-lookup"><span data-stu-id="24e79-128">-Path</span></span>
<span data-ttu-id="24e79-129">Задает путь к файлу JSON определения плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="24e79-129">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="24e79-130">Чтобы создать план восстановления, можно использовать JSON с определением плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="24e79-130">A recovery plan definition json can be used to create the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e79-131">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="24e79-131">-PrimaryFabric</span></span>
<span data-ttu-id="24e79-132">Задает объект Fabric ASR для основной структуры ASR, защищенной репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="24e79-132">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e79-133">-PrimaryZone</span><span class="sxs-lookup"><span data-stu-id="24e79-133">-PrimaryZone</span></span>
<span data-ttu-id="24e79-134">Указывает основную зону availabilty для элементов, защищенных репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="24e79-134">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e79-135">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="24e79-135">-RecoveryFabric</span></span>
<span data-ttu-id="24e79-136">Указывает объект Fabric ASR для структуры восстановления ASR для элементов, защищенных репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="24e79-136">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e79-137">-RecoveryZone</span><span class="sxs-lookup"><span data-stu-id="24e79-137">-RecoveryZone</span></span>
<span data-ttu-id="24e79-138">Указывает основную зону availabilty для элементов, защищенных репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="24e79-138">Specifies the primary Availabilty zone of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e79-139">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="24e79-139">-ReplicationProtectedItem</span></span>
<span data-ttu-id="24e79-140">Список элементов, защищенных репликацией, которые нужно добавить в первую группу плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="24e79-140">The list of replication protected items to add to the first group of the recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24e79-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24e79-141">-Confirm</span></span>
<span data-ttu-id="24e79-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24e79-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e79-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e79-143">-WhatIf</span></span>
<span data-ttu-id="24e79-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24e79-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24e79-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24e79-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e79-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e79-146">CommonParameters</span></span>
<span data-ttu-id="24e79-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24e79-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e79-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24e79-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e79-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24e79-149">INPUTS</span></span>

### <span data-ttu-id="24e79-150">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="24e79-150">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="24e79-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24e79-151">OUTPUTS</span></span>

### <span data-ttu-id="24e79-152">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="24e79-152">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="24e79-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="24e79-153">NOTES</span></span>

## <span data-ttu-id="24e79-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24e79-154">RELATED LINKS</span></span>

[<span data-ttu-id="24e79-155">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="24e79-155">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="24e79-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="24e79-156">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="24e79-157">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="24e79-157">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


