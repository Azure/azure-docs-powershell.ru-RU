---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: d387774ebf5f269474df959de981568141f90fbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560739"
---
# <span data-ttu-id="1435f-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1435f-101">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="1435f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1435f-102">SYNOPSIS</span></span>
<span data-ttu-id="1435f-103">Задает свойства восстановления, такие как Целевая сеть и размер виртуальной машины, для указанного элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="1435f-103">Sets recovery properties such as target network and virtual machine size for the specified replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1435f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1435f-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1435f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1435f-105">DESCRIPTION</span></span>
<span data-ttu-id="1435f-106">Командлет **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** задает свойства восстановления для элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="1435f-106">The **Set-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet sets the recovery properties for a Replication Protected Item.</span></span>

## <span data-ttu-id="1435f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1435f-107">EXAMPLES</span></span>

### <span data-ttu-id="1435f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1435f-108">Example 1</span></span>
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

<span data-ttu-id="1435f-109">Запускает операцию по обновлению параметров защиты элемента в репликации с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="1435f-109">Starts the operation of updating the replication protect item settings using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1435f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1435f-110">PARAMETERS</span></span>

### <span data-ttu-id="1435f-111">-AzureToAzureUpdateReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="1435f-111">-AzureToAzureUpdateReplicationConfiguration</span></span>
<span data-ttu-id="1435f-112">Определяет конфигурацию relication обновления.</span><span class="sxs-lookup"><span data-stu-id="1435f-112">Specifies the update relication configration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1435f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1435f-113">-DefaultProfile</span></span>
<span data-ttu-id="1435f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1435f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1435f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1435f-115">-InputObject</span></span>
<span data-ttu-id="1435f-116">Входной объект для командлета: объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для обновления.</span><span class="sxs-lookup"><span data-stu-id="1435f-116">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1435f-117">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1435f-117">-LicenseType</span></span>
<span data-ttu-id="1435f-118">Укажите тип лицензии, который будет использоваться для виртуальных машин Windows Server.</span><span class="sxs-lookup"><span data-stu-id="1435f-118">Specifiy the license type selection to be used for Windows Server virtual machines.</span></span> <span data-ttu-id="1435f-119">Если вы правы на использование гибридной возможности использования службы Azure (HUB) для миграции и хотели бы указать, что параметр HUB будет использоваться при сбое для этого защищенного элемента, установите для него тип лицензии WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="1435f-119">If you are entitled to use the Azure Hybrid Use Benefit (HUB) for migrations and would like to specify that the HUB setting be used while failing over this protected item set the license type to be WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1435f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1435f-120">-Name</span></span>
<span data-ttu-id="1435f-121">Указывает имя виртуальной машины восстановления, которая будет создана при отработке отказа.</span><span class="sxs-lookup"><span data-stu-id="1435f-121">Specifies the name of the recovery virtual machine that will be created on failover.</span></span>

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

### <span data-ttu-id="1435f-122">-NicSelectionType</span><span class="sxs-lookup"><span data-stu-id="1435f-122">-NicSelectionType</span></span>
<span data-ttu-id="1435f-123">Задает свойства сетевого адаптера, заданные пользователем или заданные по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1435f-123">Specifies the network interface card (NIC) properties set by user or set by default.</span></span>
<span data-ttu-id="1435f-124">Вы можете указать NotSelected, чтобы вернуться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1435f-124">You can specify NotSelected to go back to the default values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1435f-125">-PrimaryNic</span><span class="sxs-lookup"><span data-stu-id="1435f-125">-PrimaryNic</span></span>
<span data-ttu-id="1435f-126">Задает сетевую карту виртуальной машины, для которой этот командлет задает свойство сетевого восстановления.</span><span class="sxs-lookup"><span data-stu-id="1435f-126">Specifies the NIC of the virtual machine for which this cmdlet sets the recovery network property.</span></span>

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

### <span data-ttu-id="1435f-127">-RecoveryAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1435f-127">-RecoveryAvailabilitySet</span></span>
<span data-ttu-id="1435f-128">Набор доступности для защищенного элемента репликации после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="1435f-128">Availability set for replication protected item after failover.</span></span>

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

### <span data-ttu-id="1435f-129">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1435f-129">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="1435f-130">Указывает учетную запись хранения для диагностики загрузки для восстановления ВМ Azure.</span><span class="sxs-lookup"><span data-stu-id="1435f-130">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="1435f-131">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="1435f-131">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="1435f-132">Идентификатор ресурса облачной службы восстановления, на которую следует отработка отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1435f-132">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="1435f-133">-RecoveryNetworkId</span><span class="sxs-lookup"><span data-stu-id="1435f-133">-RecoveryNetworkId</span></span>
<span data-ttu-id="1435f-134">Указывает идентификатор виртуальной сети Azure, для которой должен быть выполнен отказ для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="1435f-134">Specifies the ID of the Azure virtual network to which the protected item should be failed over.</span></span>

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

### <span data-ttu-id="1435f-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="1435f-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="1435f-136">Статический IP-адрес, который должен быть назначен основной NIC при восстановлении.</span><span class="sxs-lookup"><span data-stu-id="1435f-136">Specifies the static IP address that should be assigned to primary NIC on recovery.</span></span>

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

### <span data-ttu-id="1435f-137">-RecoveryNicSubnetName</span><span class="sxs-lookup"><span data-stu-id="1435f-137">-RecoveryNicSubnetName</span></span>
<span data-ttu-id="1435f-138">Указывает имя подсети в виртуальной сети восстановления Azure, к которому следует подключить этот сетевой адаптер защищенного элемента при отработке отказа.</span><span class="sxs-lookup"><span data-stu-id="1435f-138">Specifies the name of the subnet on the recovery Azure virtual network to which this NIC of the protected item should be connected to on failover.</span></span>

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

### <span data-ttu-id="1435f-139">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="1435f-139">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="1435f-140">Идентификатор группы ресурсов Azure в области восстановления, в которой защищенный элемент будет восстанавливаться при переходе на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="1435f-140">The ID of the Azure resource group in the recovery region in which the protected item will be recovered on failover.</span></span>

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

### <span data-ttu-id="1435f-141">-Size</span><span class="sxs-lookup"><span data-stu-id="1435f-141">-Size</span></span>
<span data-ttu-id="1435f-142">Указывает размер виртуальной машины для восстановления.</span><span class="sxs-lookup"><span data-stu-id="1435f-142">Specifies the recovery virtual machine size.</span></span>
<span data-ttu-id="1435f-143">Значение должно быть из набора размеров, поддерживаемых виртуальными машинами Azure.</span><span class="sxs-lookup"><span data-stu-id="1435f-143">The value should be from the set of sizes supported by Azure virtual machines.</span></span>

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

### <span data-ttu-id="1435f-144">-UseManagedDisk</span><span class="sxs-lookup"><span data-stu-id="1435f-144">-UseManagedDisk</span></span>
<span data-ttu-id="1435f-145">Указывает, должны ли виртуальные машины Azure, созданные на отработке отказа, использовать управляемые диски.</span><span class="sxs-lookup"><span data-stu-id="1435f-145">Specifies if the Azure virtual machine that is created on failover should use managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1435f-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1435f-146">-Confirm</span></span>
<span data-ttu-id="1435f-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1435f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1435f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1435f-148">-WhatIf</span></span>
<span data-ttu-id="1435f-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1435f-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1435f-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1435f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1435f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1435f-151">CommonParameters</span></span>
<span data-ttu-id="1435f-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1435f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1435f-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1435f-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1435f-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1435f-154">INPUTS</span></span>

### <span data-ttu-id="1435f-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1435f-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1435f-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1435f-156">OUTPUTS</span></span>

### <span data-ttu-id="1435f-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1435f-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1435f-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="1435f-158">NOTES</span></span>

## <span data-ttu-id="1435f-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1435f-159">RELATED LINKS</span></span>

[<span data-ttu-id="1435f-160">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1435f-160">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="1435f-161">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1435f-161">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="1435f-162">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1435f-162">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
