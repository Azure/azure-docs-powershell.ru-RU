---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: e9edfb1654e623b023a075cb462fedfbd9442756
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561595"
---
# <span data-ttu-id="aa1e3-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aa1e3-101">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="aa1e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa1e3-102">SYNOPSIS</span></span>
<span data-ttu-id="aa1e3-103">Создает план восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-103">Creates an ASR recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa1e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa1e3-104">SYNTAX</span></span>

### <span data-ttu-id="aa1e3-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa1e3-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric>
 -RecoveryFabric <ASRFabric> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa1e3-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="aa1e3-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa1e3-107">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="aa1e3-107">ByRPFile</span></span>
```
New-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa1e3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa1e3-108">DESCRIPTION</span></span>
<span data-ttu-id="aa1e3-109">Командлет **New-AzureRmRecoveryServicesAsrRecoveryPlan** создает план восстановления Azure Site Recovery в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-109">The **New-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet creates an Azure Site Recovery recovery plan in the Recovery Services vault.</span></span>

<span data-ttu-id="aa1e3-110">План восстановления позволяет собрать на устройстве виртуальные машины, принадлежащие приложению, чтобы их можно было восстановить вместе.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-110">A recovery plan gathers virtual machines belonging to an application into a unit to allow them to be recovered together.</span></span>

## <span data-ttu-id="aa1e3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa1e3-111">EXAMPLES</span></span>

### <span data-ttu-id="aa1e3-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa1e3-112">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

<span data-ttu-id="aa1e3-113">Запускает операцию создания плана восстановления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-113">Starts the recovery plan creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="aa1e3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa1e3-114">PARAMETERS</span></span>

### <span data-ttu-id="aa1e3-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="aa1e3-115">-Azure</span></span>
<span data-ttu-id="aa1e3-116">Параметр Switch, указывающий, что расположение для восстановления плана восстановления — Azure.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-116">Switch parameter to specify that the recovery location for recovery plan is Azure.</span></span>

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

### <span data-ttu-id="aa1e3-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa1e3-117">-Confirm</span></span>
<span data-ttu-id="aa1e3-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa1e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa1e3-119">-DefaultProfile</span></span>
<span data-ttu-id="aa1e3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="aa1e3-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="aa1e3-121">-FailoverDeploymentModel</span></span>
<span data-ttu-id="aa1e3-122">Указывает модель развертывания для отработки отказа (классический или диспетчер ресурсов) для элементов, защищенных репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-122">Specifies the failover deployment model (Classic or Resource Manager) of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="aa1e3-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa1e3-123">-Name</span></span>
<span data-ttu-id="aa1e3-124">Имя плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-124">Name of the recovery plan.</span></span>

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

### <span data-ttu-id="aa1e3-125">-Path</span><span class="sxs-lookup"><span data-stu-id="aa1e3-125">-Path</span></span>
<span data-ttu-id="aa1e3-126">Задает путь к файлу JSON определения плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-126">Specifies the path to the recovery plan definition json file.</span></span> <span data-ttu-id="aa1e3-127">Чтобы создать план восстановления, можно использовать JSON с определением плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-127">A recovery plan definition json can be used to create the recovery plan.</span></span>

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

### <span data-ttu-id="aa1e3-128">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="aa1e3-128">-PrimaryFabric</span></span>
<span data-ttu-id="aa1e3-129">Задает объект Fabric ASR для основной структуры ASR, защищенной репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-129">Specifies the ASR fabric object for the primary ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="aa1e3-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="aa1e3-130">-RecoveryFabric</span></span>
<span data-ttu-id="aa1e3-131">Указывает объект Fabric ASR для структуры восстановления ASR для элементов, защищенных репликацией, которые будут входить в этот план восстановления.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-131">Specifies the ASR fabric object for the recovery ASR fabric of the replication protected items that will be part of this recovery plan.</span></span>

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

### <span data-ttu-id="aa1e3-132">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="aa1e3-132">-ReplicationProtectedItem</span></span>
<span data-ttu-id="aa1e3-133">Список элементов, защищенных репликацией, которые нужно добавить в первую группу плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-133">The list of replication protected items to add to the first group of the recovery plan.</span></span>

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

### <span data-ttu-id="aa1e3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa1e3-134">-WhatIf</span></span>
<span data-ttu-id="aa1e3-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa1e3-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa1e3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa1e3-137">CommonParameters</span></span>
<span data-ttu-id="aa1e3-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa1e3-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa1e3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa1e3-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa1e3-140">INPUTS</span></span>

### <span data-ttu-id="aa1e3-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem []</span><span class="sxs-lookup"><span data-stu-id="aa1e3-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]</span></span>

## <span data-ttu-id="aa1e3-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa1e3-142">OUTPUTS</span></span>

### <span data-ttu-id="aa1e3-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="aa1e3-143">System.Object</span></span>

## <span data-ttu-id="aa1e3-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa1e3-144">NOTES</span></span>

## <span data-ttu-id="aa1e3-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa1e3-145">RELATED LINKS</span></span>

[<span data-ttu-id="aa1e3-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aa1e3-146">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="aa1e3-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aa1e3-147">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="aa1e3-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="aa1e3-148">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


