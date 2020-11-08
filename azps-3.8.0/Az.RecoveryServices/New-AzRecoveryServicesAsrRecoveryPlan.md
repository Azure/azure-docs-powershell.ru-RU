---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 851f9d52b3247fed0755b4567e3c463b1202c34b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074688"
---
# <span data-ttu-id="cfc92-101">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cfc92-101">New-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="cfc92-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfc92-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc92-103">Создает план восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="cfc92-103">Creates an ASR recovery plan.</span></span>

## <span data-ttu-id="cfc92-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfc92-104">SYNTAX</span></span>

### <span data-ttu-id="cfc92-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cfc92-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfc92-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="cfc92-106">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfc92-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="cfc92-107">ByRPFile</span></span>
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfc92-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfc92-108">DESCRIPTION</span></span>
<span data-ttu-id="cfc92-109">Командлет **New-AzRecoveryServicesAsrRecoveryPlan** создает восстановление сайта Azure, план восстановления в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfc92-109">The **New-AzRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery, recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="cfc92-110">План восстановления позволяет собрать на устройстве виртуальные машины, принадлежащие приложению, чтобы их можно было восстановить вместе.</span><span class="sxs-lookup"><span data-stu-id="cfc92-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="cfc92-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfc92-111">EXAMPLES</span></span>

### <span data-ttu-id="cfc92-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cfc92-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="cfc92-113">Запускает операцию создания плана восстановления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="cfc92-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cfc92-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfc92-114">PARAMETERS</span></span>

### <span data-ttu-id="cfc92-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="cfc92-115">-Azure</span></span>
<span data-ttu-id="cfc92-116">Параметр Switch задает сценарий для восстановления с помощью Azure для Azure, создание плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfc92-116">Switch parameter specifies the scenario for azure to azure disaster recovery, recovery plan creation.</span></span>

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

### <span data-ttu-id="cfc92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc92-117">-DefaultProfile</span></span>
<span data-ttu-id="cfc92-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfc92-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cfc92-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="cfc92-119">-FailoverDeploymentModel</span></span>
<span data-ttu-id="cfc92-120">Указывает модель развертывания для отработки отказа (классический или диспетчер ресурсов) для элементов, защищенных репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfc92-120">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="cfc92-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cfc92-121">-Name</span></span>
<span data-ttu-id="cfc92-122">Имя плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfc92-122">Name of the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc92-123">-Path</span><span class="sxs-lookup"><span data-stu-id="cfc92-123">-Path</span></span>
<span data-ttu-id="cfc92-124">Задает путь к файлу JSON определения плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfc92-124">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="cfc92-125">Чтобы создать план восстановления, можно использовать JSON с определением плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfc92-125">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="cfc92-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="cfc92-126">-PrimaryFabric</span></span>
<span data-ttu-id="cfc92-127">Задает объект Fabric ASR для основной структуры ASR, защищенной репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfc92-127">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfc92-128">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="cfc92-128">-RecoveryFabric</span></span>
<span data-ttu-id="cfc92-129">Указывает объект Fabric ASR для структуры восстановления ASR для элементов, защищенных репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfc92-129">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="cfc92-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cfc92-130">-ReplicationProtectedItem</span></span>
<span data-ttu-id="cfc92-131">Список элементов, защищенных репликацией, которые нужно добавить в первую группу плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfc92-131">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="cfc92-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfc92-132">-Confirm</span></span>
<span data-ttu-id="cfc92-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cfc92-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfc92-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfc92-134">-WhatIf</span></span>
<span data-ttu-id="cfc92-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cfc92-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfc92-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cfc92-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfc92-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc92-137">CommonParameters</span></span>
<span data-ttu-id="cfc92-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfc92-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc92-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cfc92-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc92-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfc92-140">INPUTS</span></span>

### <span data-ttu-id="cfc92-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="cfc92-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="cfc92-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfc92-142">OUTPUTS</span></span>

### <span data-ttu-id="cfc92-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cfc92-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cfc92-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfc92-144">NOTES</span></span>

## <span data-ttu-id="cfc92-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfc92-145">RELATED LINKS</span></span>

[<span data-ttu-id="cfc92-146">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cfc92-146">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="cfc92-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cfc92-147">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="cfc92-148">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cfc92-148">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


