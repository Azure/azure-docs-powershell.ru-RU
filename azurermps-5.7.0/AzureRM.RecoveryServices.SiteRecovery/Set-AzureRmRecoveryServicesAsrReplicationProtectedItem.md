---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: a3ae73e9831202418d35481270a1d04b1cb09a59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563391"
---
# <span data-ttu-id="e46f9-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e46f9-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="e46f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e46f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e46f9-103">Задает свойства восстановления, такие как Целевая сеть и размер виртуальной машины, для указанного элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="e46f9-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e46f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e46f9-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e46f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e46f9-105">DESCRIPTION</span></span>
<span data-ttu-id="e46f9-106">Командлет **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** задает свойства восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="e46f9-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="e46f9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e46f9-107">EXAMPLES</span></span>

### <span data-ttu-id="e46f9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e46f9-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="e46f9-109">Запускает операцию по обновлению параметров защиты элемента в репликации с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="e46f9-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e46f9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e46f9-110">PARAMETERS</span></span>

### <span data-ttu-id="e46f9-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e46f9-111">-Confirm</span></span>
<span data-ttu-id="e46f9-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e46f9-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e46f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46f9-113">-DefaultProfile</span></span>
<span data-ttu-id="e46f9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e46f9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="e46f9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e46f9-115">-InputObject</span></span>
<span data-ttu-id="e46f9-116">Входной объект для командлета: объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для обновления.</span><span class="sxs-lookup"><span data-stu-id="e46f9-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e46f9-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e46f9-117">-LicenseType</span></span>
<span data-ttu-id="e46f9-118">Укажите тип лицензии, который будет использоваться для виртуальных машин Windows Server.</span><span class="sxs-lookup"><span data-stu-id="e46f9-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="e46f9-119">Если вы правы на использование гибридной возможности использования службы Azure (HUB) для миграции и хотели бы указать, что параметр HUB будет использоваться при сбое для этого защищенного элемента, установите для него тип лицензии WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="e46f9-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46f9-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e46f9-120">-Name</span></span>
<span data-ttu-id="e46f9-121">Указывает имя виртуальной машины восстановления, которая будет создана при отработке отказа.</span><span class="sxs-lookup"><span data-stu-id="e46f9-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="e46f9-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="e46f9-122">-NicSelectionType</span></span>
<span data-ttu-id="e46f9-123">Задает свойства сетевого адаптера, заданные пользователем или заданные по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e46f9-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="e46f9-124">Вы можете указать NotSelected, чтобы вернуться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e46f9-124">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46f9-125">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="e46f9-125">-PrimaryNic</span></span>
<span data-ttu-id="e46f9-126">Задает сетевую карту виртуальной машины, для которой этот командлет задает свойство сетевого восстановления.</span><span class="sxs-lookup"><span data-stu-id="e46f9-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="e46f9-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e46f9-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="e46f9-128">Набор доступности для защищенного элемента репликации после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="e46f9-128">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="e46f9-129">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="e46f9-129">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="e46f9-130">Идентификатор ресурса облачной службы восстановления, на которую следует отработка отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e46f9-130">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="e46f9-131">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="e46f9-131">-RecoveryNetworkId</span></span>
<span data-ttu-id="e46f9-132">Указывает идентификатор виртуальной сети Azure, для которой должен быть выполнен отказ для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="e46f9-132">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="e46f9-133">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="e46f9-133">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="e46f9-134">Статический IP-адрес, который должен быть назначен основной NIC при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="e46f9-134">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="e46f9-135">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="e46f9-135">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="e46f9-136">Указывает имя подсети в виртуальной сети восстановления Azure, к которому следует подключить этот сетевой адаптер защищенного элемента при отработке отказа.</span><span class="sxs-lookup"><span data-stu-id="e46f9-136">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="e46f9-137">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="e46f9-137">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="e46f9-138">Идентификатор группы ресурсов Azure в области восстановления, в которой защищенный элемент будет восстанавливаться при переходе на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="e46f9-138">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="e46f9-139">-Size</span><span class="sxs-lookup"><span data-stu-id="e46f9-139">-Size</span></span>
<span data-ttu-id="e46f9-140">Указывает размер виртуальной машины для восстановления.</span><span class="sxs-lookup"><span data-stu-id="e46f9-140">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="e46f9-141">Значение должно быть из набора размеров, поддерживаемых виртуальными машинами Azure.</span><span class="sxs-lookup"><span data-stu-id="e46f9-141">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="e46f9-142">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="e46f9-142">-UseManagedDisk</span></span>
<span data-ttu-id="e46f9-143">Указывает, должны ли виртуальные машины Azure, созданные на отработке отказа, использовать управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="e46f9-143">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46f9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e46f9-144">-WhatIf</span></span>
<span data-ttu-id="e46f9-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e46f9-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e46f9-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e46f9-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e46f9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46f9-147">CommonParameters</span></span>
<span data-ttu-id="e46f9-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e46f9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46f9-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e46f9-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46f9-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e46f9-150">INPUTS</span></span>

### <span data-ttu-id="e46f9-151">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e46f9-151">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e46f9-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e46f9-152">OUTPUTS</span></span>

### <span data-ttu-id="e46f9-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e46f9-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e46f9-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="e46f9-154">NOTES</span></span>

## <span data-ttu-id="e46f9-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e46f9-155">RELATED LINKS</span></span>

[<span data-ttu-id="e46f9-156">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e46f9-156">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="e46f9-157">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e46f9-157">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="e46f9-158">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e46f9-158">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
