---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247042"
---
# <span data-ttu-id="09729-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="09729-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="09729-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09729-102">SYNOPSIS</span></span>
<span data-ttu-id="09729-103">Создание конфигурации сетевого адаптера ASR, содержащей сведения о конфигурации, связанные с отработкой отказа и тестированием.</span><span class="sxs-lookup"><span data-stu-id="09729-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="09729-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09729-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryNicName <String>] [-RecoveryNicResourceGroupName <String>]
 [-ReuseExistingNic] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoNicName <String>] [-TfoNicResourceGroupName <String>] [-TfoReuseExistingNic] [-TfoVMSubnetName <String>]
 [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo] [-TfoNicStaticIPAddress <String>]
 [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09729-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09729-105">DESCRIPTION</span></span>
<span data-ttu-id="09729-106">Командлет **New-AzRecoveryServicesAsrVMNicConfig** создает объект конфигурации сетевого адаптера ASR, содержащий сведения об отработке отказа и тест, связанные с отработкой отказа.</span><span class="sxs-lookup"><span data-stu-id="09729-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="09729-107">В случае если любая информация не передается, соответствующие значения выбираются из элемента, защищенного репликацией, чтобы избежать их обновления до значения NULL.</span><span class="sxs-lookup"><span data-stu-id="09729-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="09729-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09729-108">EXAMPLES</span></span>

### <span data-ttu-id="09729-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="09729-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="09729-110">Создает объект ASRVmNicConfig с сетевыми параметрами faiover, настроенными для сетевого адаптера, и тестами.</span><span class="sxs-lookup"><span data-stu-id="09729-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="09729-111">Любое свойство, не переданное выше, извлекается из переданного защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="09729-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="09729-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="09729-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="09729-113">Создает объект ASRVmNicConfig с параметрами "проверить сетевые faiover", настроенными для переименования NIC.</span><span class="sxs-lookup"><span data-stu-id="09729-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="09729-114">Любое свойство, не переданное выше, извлекается из переданного защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="09729-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="09729-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="09729-115">Example 3</span></span>

<span data-ttu-id="09729-116">Создание конфигурации сетевого адаптера ASR, содержащей сведения о конфигурации, связанные с отработкой отказа и тестированием.</span><span class="sxs-lookup"><span data-stu-id="09729-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="09729-117">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="09729-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="09729-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09729-118">PARAMETERS</span></span>

### <span data-ttu-id="09729-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09729-119">-DefaultProfile</span></span>
<span data-ttu-id="09729-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09729-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09729-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="09729-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="09729-122">Указывает, включена ли сеть ускорения для восстановления сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="09729-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09729-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="09729-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="09729-124">Указывает, включена ли сеть ускоренной проверки поработки отказа для тестового сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="09729-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09729-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="09729-125">-NicId</span></span>
<span data-ttu-id="09729-126">Укажите GUID сетевого адаптера ASR.</span><span class="sxs-lookup"><span data-stu-id="09729-126">Specify the ASR NIC GUID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09729-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="09729-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="09729-128">Указывает идентификаторы пулов серверных адресов для сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="09729-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09729-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="09729-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="09729-130">Указывает идентификатор NSG, связанного с сетевым адаптером восстановления.</span><span class="sxs-lookup"><span data-stu-id="09729-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="09729-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="09729-131">-RecoveryNicName</span></span>
<span data-ttu-id="09729-132">Указывает имя сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="09729-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="09729-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09729-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="09729-134">Указывает имя группы ресурсов сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="09729-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="09729-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="09729-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="09729-136">Указывает IP-адрес сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="09729-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="09729-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="09729-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="09729-138">Указывает идентификатор общедоступного IP-адреса, связанного с сетевым адаптером восстановления.</span><span class="sxs-lookup"><span data-stu-id="09729-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="09729-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="09729-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="09729-140">Указывает идентификатор виртуальной сети восстановления.</span><span class="sxs-lookup"><span data-stu-id="09729-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="09729-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="09729-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="09729-142">Указывает имя подсети восстановления.</span><span class="sxs-lookup"><span data-stu-id="09729-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="09729-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="09729-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="09729-144">Укажите элемент, защищенный репликацией ASR.</span><span class="sxs-lookup"><span data-stu-id="09729-144">Specify the ASR Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09729-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="09729-145">-ReuseExistingNic</span></span>
<span data-ttu-id="09729-146">Указывает, можно ли использовать существующую сетевую карту во время отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="09729-146">Specifies whether an existing NIC can be used during failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09729-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="09729-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="09729-148">Указывает идентификаторы пулов серверных адресов для сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="09729-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09729-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="09729-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="09729-150">Указывает идентификатор NSG, связанного с сетевым адаптером тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="09729-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="09729-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="09729-151">-TfoNicName</span></span>
<span data-ttu-id="09729-152">Указывает имя сетевого адаптера тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="09729-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="09729-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09729-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="09729-154">Указывает имя группы ресурсов "сетевая карта для проверки отработки отказа".</span><span class="sxs-lookup"><span data-stu-id="09729-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="09729-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="09729-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="09729-156">Указывает IP-адрес тестового сетевого адаптера для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="09729-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="09729-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="09729-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="09729-158">Указывает идентификатор общедоступного IP-адреса, связанного с сетевой адаптером тестового отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="09729-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="09729-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="09729-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="09729-160">Указывает, можно ли использовать существующую сетевую карту во время тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="09729-160">Specifies whether an existing NIC can be used during test failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09729-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="09729-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="09729-162">Указывает идентификатор тестовой виртуальной сети для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="09729-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="09729-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="09729-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="09729-164">Указывает имя подсети тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="09729-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="09729-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09729-165">-Confirm</span></span>
<span data-ttu-id="09729-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="09729-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09729-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09729-167">-WhatIf</span></span>
<span data-ttu-id="09729-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="09729-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09729-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="09729-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09729-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09729-170">CommonParameters</span></span>
<span data-ttu-id="09729-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09729-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09729-172">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09729-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09729-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09729-173">INPUTS</span></span>

### <span data-ttu-id="09729-174">Ничего</span><span class="sxs-lookup"><span data-stu-id="09729-174">None</span></span>

## <span data-ttu-id="09729-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09729-175">OUTPUTS</span></span>

### <span data-ttu-id="09729-176">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="09729-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="09729-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="09729-177">NOTES</span></span>

## <span data-ttu-id="09729-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09729-178">RELATED LINKS</span></span>
