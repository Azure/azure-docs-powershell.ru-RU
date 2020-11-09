---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244263"
---
# <span data-ttu-id="a26ee-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="a26ee-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="a26ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a26ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a26ee-103">Создание конфигурации сетевого адаптера ASR, содержащей сведения о конфигурации, связанные с отработкой отказа и тестированием.</span><span class="sxs-lookup"><span data-stu-id="a26ee-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="a26ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a26ee-104">SYNTAX</span></span>

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

## <span data-ttu-id="a26ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a26ee-105">DESCRIPTION</span></span>
<span data-ttu-id="a26ee-106">Командлет **New-AzRecoveryServicesAsrVMNicConfig** создает объект конфигурации сетевого адаптера ASR, содержащий сведения об отработке отказа и тест, связанные с отработкой отказа.</span><span class="sxs-lookup"><span data-stu-id="a26ee-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="a26ee-107">В случае если любая информация не передается, соответствующие значения выбираются из элемента, защищенного репликацией, чтобы избежать их обновления до значения NULL.</span><span class="sxs-lookup"><span data-stu-id="a26ee-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="a26ee-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a26ee-108">EXAMPLES</span></span>

### <span data-ttu-id="a26ee-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a26ee-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="a26ee-110">Создает объект ASRVmNicConfig с сетевыми параметрами faiover, настроенными для сетевого адаптера, и тестами.</span><span class="sxs-lookup"><span data-stu-id="a26ee-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="a26ee-111">Любое свойство, не переданное выше, извлекается из переданного защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="a26ee-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="a26ee-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a26ee-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="a26ee-113">Создает объект ASRVmNicConfig с параметрами "проверить сетевые faiover", настроенными для переименования NIC.</span><span class="sxs-lookup"><span data-stu-id="a26ee-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="a26ee-114">Любое свойство, не переданное выше, извлекается из переданного защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="a26ee-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="a26ee-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a26ee-115">Example 3</span></span>

<span data-ttu-id="a26ee-116">Создание конфигурации сетевого адаптера ASR, содержащей сведения о конфигурации, связанные с отработкой отказа и тестированием.</span><span class="sxs-lookup"><span data-stu-id="a26ee-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="a26ee-117">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="a26ee-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="a26ee-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a26ee-118">PARAMETERS</span></span>

### <span data-ttu-id="a26ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a26ee-119">-DefaultProfile</span></span>
<span data-ttu-id="a26ee-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a26ee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a26ee-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="a26ee-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="a26ee-122">Указывает, включена ли сеть ускорения для восстановления сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="a26ee-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="a26ee-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="a26ee-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="a26ee-124">Указывает, включена ли сеть ускоренной проверки поработки отказа для тестового сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="a26ee-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="a26ee-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="a26ee-125">-NicId</span></span>
<span data-ttu-id="a26ee-126">Укажите GUID сетевого адаптера ASR.</span><span class="sxs-lookup"><span data-stu-id="a26ee-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="a26ee-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a26ee-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="a26ee-128">Указывает идентификаторы пулов серверных адресов для сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="a26ee-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="a26ee-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a26ee-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="a26ee-130">Указывает идентификатор NSG, связанного с сетевым адаптером восстановления.</span><span class="sxs-lookup"><span data-stu-id="a26ee-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="a26ee-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="a26ee-131">-RecoveryNicName</span></span>
<span data-ttu-id="a26ee-132">Указывает имя сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="a26ee-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="a26ee-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a26ee-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="a26ee-134">Указывает имя группы ресурсов сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="a26ee-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="a26ee-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="a26ee-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="a26ee-136">Указывает IP-адрес сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="a26ee-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="a26ee-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="a26ee-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="a26ee-138">Указывает идентификатор общедоступного IP-адреса, связанного с сетевым адаптером восстановления.</span><span class="sxs-lookup"><span data-stu-id="a26ee-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="a26ee-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a26ee-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="a26ee-140">Указывает идентификатор виртуальной сети восстановления.</span><span class="sxs-lookup"><span data-stu-id="a26ee-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="a26ee-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="a26ee-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="a26ee-142">Указывает имя подсети восстановления.</span><span class="sxs-lookup"><span data-stu-id="a26ee-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="a26ee-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a26ee-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a26ee-144">Укажите элемент, защищенный репликацией ASR.</span><span class="sxs-lookup"><span data-stu-id="a26ee-144">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="a26ee-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="a26ee-145">-ReuseExistingNic</span></span>
<span data-ttu-id="a26ee-146">Указывает, можно ли использовать существующую сетевую карту во время отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="a26ee-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="a26ee-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a26ee-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="a26ee-148">Указывает идентификаторы пулов серверных адресов для сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="a26ee-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="a26ee-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="a26ee-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="a26ee-150">Указывает идентификатор NSG, связанного с сетевым адаптером тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="a26ee-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="a26ee-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="a26ee-151">-TfoNicName</span></span>
<span data-ttu-id="a26ee-152">Указывает имя сетевого адаптера тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="a26ee-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="a26ee-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a26ee-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="a26ee-154">Указывает имя группы ресурсов "сетевая карта для проверки отработки отказа".</span><span class="sxs-lookup"><span data-stu-id="a26ee-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="a26ee-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="a26ee-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="a26ee-156">Указывает IP-адрес тестового сетевого адаптера для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="a26ee-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="a26ee-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="a26ee-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="a26ee-158">Указывает идентификатор общедоступного IP-адреса, связанного с сетевой адаптером тестового отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="a26ee-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="a26ee-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="a26ee-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="a26ee-160">Указывает, можно ли использовать существующую сетевую карту во время тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="a26ee-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="a26ee-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="a26ee-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="a26ee-162">Указывает идентификатор тестовой виртуальной сети для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="a26ee-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="a26ee-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="a26ee-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="a26ee-164">Указывает имя подсети тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="a26ee-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="a26ee-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a26ee-165">-Confirm</span></span>
<span data-ttu-id="a26ee-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a26ee-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a26ee-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a26ee-167">-WhatIf</span></span>
<span data-ttu-id="a26ee-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a26ee-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a26ee-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a26ee-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a26ee-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a26ee-170">CommonParameters</span></span>
<span data-ttu-id="a26ee-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a26ee-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a26ee-172">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a26ee-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a26ee-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a26ee-173">INPUTS</span></span>

### <span data-ttu-id="a26ee-174">Ничего</span><span class="sxs-lookup"><span data-stu-id="a26ee-174">None</span></span>

## <span data-ttu-id="a26ee-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a26ee-175">OUTPUTS</span></span>

### <span data-ttu-id="a26ee-176">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="a26ee-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="a26ee-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="a26ee-177">NOTES</span></span>

## <span data-ttu-id="a26ee-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a26ee-178">RELATED LINKS</span></span>