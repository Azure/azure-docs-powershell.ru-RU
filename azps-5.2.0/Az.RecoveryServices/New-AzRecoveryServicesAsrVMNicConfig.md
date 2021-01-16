---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: 658a0cfa66abd71a63edc67ab2615713ac815bcd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410516"
---
# <span data-ttu-id="34524-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="34524-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="34524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34524-102">SYNOPSIS</span></span>
<span data-ttu-id="34524-103">Создает конфигурацию ASR NIC, которая содержит сведения о конфигурации от сбойов и тестирования.</span><span class="sxs-lookup"><span data-stu-id="34524-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="34524-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="34524-104">SYNTAX</span></span>

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

## <span data-ttu-id="34524-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34524-105">DESCRIPTION</span></span>
<span data-ttu-id="34524-106">**Cmdlet New-AzRecoveryServicesAsrVMNicConfig** создает объект config ASR NIC, содержащий сведения о отрезоке и проверке отседания.</span><span class="sxs-lookup"><span data-stu-id="34524-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="34524-107">Если какие-либо сведения не передаются, соответствующие значения выбираются из элемента, защищенного репликацией, чтобы эти значения не обновлялись до значения NULL.</span><span class="sxs-lookup"><span data-stu-id="34524-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="34524-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="34524-108">EXAMPLES</span></span>

### <span data-ttu-id="34524-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34524-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="34524-110">Создание объекта ASRVmNicConfig с отладкой и проверкой сетевых параметров faiover, настроенными для NIC.</span><span class="sxs-lookup"><span data-stu-id="34524-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="34524-111">Все свойства, которые не были переданы выше, извлекаются из защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="34524-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

### <span data-ttu-id="34524-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="34524-112">Example 2</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -TfoNicName $TfoNicName -TfoNicResourceGroupName $TfoNicRgName -TfoReuseExistingNic
```

<span data-ttu-id="34524-113">Создание объекта ASRVmNicConfig с тестовым параметром сети faiover, настроенным для переименования NIC.</span><span class="sxs-lookup"><span data-stu-id="34524-113">Creates an ASRVmNicConfig object with the test faiover networking settings configured for the NIC renaming.</span></span> <span data-ttu-id="34524-114">Все свойства, которые не были переданы выше, извлекаются из защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="34524-114">Any property that's not passed above is fetched from the protected item passed.</span></span>


### <span data-ttu-id="34524-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="34524-115">Example 3</span></span>

<span data-ttu-id="34524-116">Создает конфигурацию ASR NIC, которая содержит сведения о конфигурации от сбойов и тестирования.</span><span class="sxs-lookup"><span data-stu-id="34524-116">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span> <span data-ttu-id="34524-117">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="34524-117">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -RecoveryNetworkSecurityGroupId <String> -RecoveryNicStaticIPAddress '10.0.0.1' -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -ReplicationProtectedItem $Rpi -TfoNetworkSecurityGroupId <String> -TfoNicStaticIPAddress <String> -TfoVMNetworkId <String> -TfoVMSubnetName <String>
```

## <span data-ttu-id="34524-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34524-118">PARAMETERS</span></span>

### <span data-ttu-id="34524-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34524-119">-DefaultProfile</span></span>
<span data-ttu-id="34524-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34524-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34524-121">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="34524-121">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="34524-122">Указывает, включено ли ускорение сети при восстановлении NIC.</span><span class="sxs-lookup"><span data-stu-id="34524-122">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="34524-123">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="34524-123">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="34524-124">Указывает, включено ли ускорение сети при проверке отключки NIC.</span><span class="sxs-lookup"><span data-stu-id="34524-124">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="34524-125">-NicId</span><span class="sxs-lookup"><span data-stu-id="34524-125">-NicId</span></span>
<span data-ttu-id="34524-126">Укажите GUID ASR NIC.</span><span class="sxs-lookup"><span data-stu-id="34524-126">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="34524-127">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="34524-127">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="34524-128">Определяет IDs of backend address pools for the recovery NIC .ids of backend address pools for the recovery NIC.</span><span class="sxs-lookup"><span data-stu-id="34524-128">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="34524-129">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="34524-129">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="34524-130">Определяет ID NSG, связанный с NIC восстановления.</span><span class="sxs-lookup"><span data-stu-id="34524-130">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="34524-131">-RecoveryNicName</span><span class="sxs-lookup"><span data-stu-id="34524-131">-RecoveryNicName</span></span>
<span data-ttu-id="34524-132">Указывает имя NIC восстановления.</span><span class="sxs-lookup"><span data-stu-id="34524-132">Specifies the name of the recovery NIC.</span></span>

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

### <span data-ttu-id="34524-133">-RecoveryNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34524-133">-RecoveryNicResourceGroupName</span></span>
<span data-ttu-id="34524-134">Имя группы ресурсов "NIC восстановления".</span><span class="sxs-lookup"><span data-stu-id="34524-134">Specifies the name of the recovery NIC resource group.</span></span>

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

### <span data-ttu-id="34524-135">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="34524-135">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="34524-136">Определяет IP-адрес восстановления NIC.</span><span class="sxs-lookup"><span data-stu-id="34524-136">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="34524-137">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="34524-137">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="34524-138">Определяет ИД общего IP-адреса, связанного с процедурой восстановления NIC.</span><span class="sxs-lookup"><span data-stu-id="34524-138">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="34524-139">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="34524-139">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="34524-140">Определяет ID виртуальной сети восстановления.</span><span class="sxs-lookup"><span data-stu-id="34524-140">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="34524-141">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="34524-141">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="34524-142">Имя подсети восстановления.</span><span class="sxs-lookup"><span data-stu-id="34524-142">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="34524-143">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="34524-143">-ReplicationProtectedItem</span></span>
<span data-ttu-id="34524-144">Укажите защищенный элемент репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="34524-144">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="34524-145">-ReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="34524-145">-ReuseExistingNic</span></span>
<span data-ttu-id="34524-146">Указывает, можно ли использовать существующую NIC во время отбойной передачи.</span><span class="sxs-lookup"><span data-stu-id="34524-146">Specifies whether an existing NIC can be used during failover.</span></span>

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

### <span data-ttu-id="34524-147">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="34524-147">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="34524-148">Определяет IDs of backend address pools for the recovery NIC .ids of backend address pools for the recovery NIC.</span><span class="sxs-lookup"><span data-stu-id="34524-148">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="34524-149">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="34524-149">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="34524-150">Определяет ID NSG, связанный с отбойной проверки NIC.</span><span class="sxs-lookup"><span data-stu-id="34524-150">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="34524-151">-TfoNicName</span><span class="sxs-lookup"><span data-stu-id="34524-151">-TfoNicName</span></span>
<span data-ttu-id="34524-152">Указывает имя отбойной проверки NIC.</span><span class="sxs-lookup"><span data-stu-id="34524-152">Specifies the name of the test failover NIC.</span></span>

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

### <span data-ttu-id="34524-153">-TfoNicResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34524-153">-TfoNicResourceGroupName</span></span>
<span data-ttu-id="34524-154">Имя группы ресурсов NIC для отбойного тестирования.</span><span class="sxs-lookup"><span data-stu-id="34524-154">Specifies the name of the test failover NIC resource group.</span></span>

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

### <span data-ttu-id="34524-155">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="34524-155">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="34524-156">Указывает IP-адрес NIC для отбойного тестирования.</span><span class="sxs-lookup"><span data-stu-id="34524-156">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="34524-157">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="34524-157">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="34524-158">Определяет ИД общего IP-адреса, связанного с отбойной проверкой NIC.</span><span class="sxs-lookup"><span data-stu-id="34524-158">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="34524-159">-TfoReuseExistingNic</span><span class="sxs-lookup"><span data-stu-id="34524-159">-TfoReuseExistingNic</span></span>
<span data-ttu-id="34524-160">Указывает, можно ли использовать существующую NIC во время отбойной проверки.</span><span class="sxs-lookup"><span data-stu-id="34524-160">Specifies whether an existing NIC can be used during test failover.</span></span>

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

### <span data-ttu-id="34524-161">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="34524-161">-TfoVMNetworkId</span></span>
<span data-ttu-id="34524-162">Определяет ID виртуальной сети отсейки тестирования.</span><span class="sxs-lookup"><span data-stu-id="34524-162">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="34524-163">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="34524-163">-TfoVMSubnetName</span></span>
<span data-ttu-id="34524-164">Имя подсети отбойной проверки.</span><span class="sxs-lookup"><span data-stu-id="34524-164">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="34524-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34524-165">-Confirm</span></span>
<span data-ttu-id="34524-166">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34524-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34524-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34524-167">-WhatIf</span></span>
<span data-ttu-id="34524-168">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34524-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34524-169">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="34524-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34524-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34524-170">CommonParameters</span></span>
<span data-ttu-id="34524-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34524-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34524-172">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34524-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34524-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34524-173">INPUTS</span></span>

### <span data-ttu-id="34524-174">Нет</span><span class="sxs-lookup"><span data-stu-id="34524-174">None</span></span>

## <span data-ttu-id="34524-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="34524-175">OUTPUTS</span></span>

### <span data-ttu-id="34524-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="34524-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="34524-177">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="34524-177">NOTES</span></span>

## <span data-ttu-id="34524-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34524-178">RELATED LINKS</span></span>
