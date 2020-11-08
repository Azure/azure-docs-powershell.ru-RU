---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrvmnicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrVMNicConfig.md
ms.openlocfilehash: f7b6cd7171b6f50ed0f239e733ca98f0ecd5c05a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072686"
---
# <span data-ttu-id="31608-101">New-AzRecoveryServicesAsrVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="31608-101">New-AzRecoveryServicesAsrVMNicConfig</span></span>

## <span data-ttu-id="31608-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31608-102">SYNOPSIS</span></span>
<span data-ttu-id="31608-103">Создание конфигурации сетевого адаптера ASR, содержащей сведения о конфигурации, связанные с отработкой отказа и тестированием.</span><span class="sxs-lookup"><span data-stu-id="31608-103">Creates an ASR NIC config that contains the failover and test failover related configuration details.</span></span>

## <span data-ttu-id="31608-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31608-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrVMNicConfig -NicId <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryVMNetworkId <String>] [-RecoveryVMSubnetName <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryNicStaticIPAddress <String>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoVMNetworkId <String>]
 [-TfoVMSubnetName <String>] [-TfoNetworkSecurityGroupId <String>] [-EnableAcceleratedNetworkingOnTfo]
 [-TfoNicStaticIPAddress <String>] [-TfoPublicIPAddressId <String>] [-TfoLBBackendAddressPoolId <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31608-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31608-105">DESCRIPTION</span></span>
<span data-ttu-id="31608-106">Командлет **New-AzRecoveryServicesAsrVMNicConfig** создает объект конфигурации сетевого адаптера ASR, содержащий сведения об отработке отказа и тест, связанные с отработкой отказа.</span><span class="sxs-lookup"><span data-stu-id="31608-106">The **New-AzRecoveryServicesAsrVMNicConfig** cmdlet creates an ASR NIC config object that contains the failover and test failover related details.</span></span> <span data-ttu-id="31608-107">В случае если любая информация не передается, соответствующие значения выбираются из элемента, защищенного репликацией, чтобы избежать их обновления до значения NULL.</span><span class="sxs-lookup"><span data-stu-id="31608-107">In case any information is not passed, the corresponding values are picked from the replication protected item to avoid these values being updated to null.</span></span>

## <span data-ttu-id="31608-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31608-108">EXAMPLES</span></span>

### <span data-ttu-id="31608-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="31608-109">Example 1</span></span>
```powershell
PS C:\> $nicConfig = New-AzRecoveryServicesAsrVMNicConfig -NicId $AsrNicGuid -ReplicationProtectedItem $Rpi -RecoveryVMNetworkId $recoveryNetworkId -RecoveryVMSubnetName $recoverySubnetName -RecoveryNicStaticIPAddress "10.0.0.1" `
    -TfoVMNetworkId $tfoNetworkId -TfoVMSubnetName $tfoSubnetName -TfoNicStaticIPAddress "10.0.1.1"
```

<span data-ttu-id="31608-110">Создает объект ASRVmNicConfig с сетевыми параметрами faiover, настроенными для сетевого адаптера, и тестами.</span><span class="sxs-lookup"><span data-stu-id="31608-110">Creates an ASRVmNicConfig object with the failover and test faiover networking settings configured for the NIC.</span></span> <span data-ttu-id="31608-111">Любое свойство, не переданное выше, извлекается из переданного защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="31608-111">Any property that's not passed above is fetched from the protected item passed.</span></span>

## <span data-ttu-id="31608-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31608-112">PARAMETERS</span></span>

### <span data-ttu-id="31608-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31608-113">-DefaultProfile</span></span>
<span data-ttu-id="31608-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31608-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31608-115">-EnableAcceleratedNetworkingOnRecovery</span><span class="sxs-lookup"><span data-stu-id="31608-115">-EnableAcceleratedNetworkingOnRecovery</span></span>
<span data-ttu-id="31608-116">Указывает, включена ли сеть ускорения для восстановления сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="31608-116">Specifies whether accelerated networking is enabled on recovery NIC.</span></span>

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

### <span data-ttu-id="31608-117">-EnableAcceleratedNetworkingOnTfo</span><span class="sxs-lookup"><span data-stu-id="31608-117">-EnableAcceleratedNetworkingOnTfo</span></span>
<span data-ttu-id="31608-118">Указывает, включена ли сеть ускоренной проверки поработки отказа для тестового сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="31608-118">Specifies whether accelerated networking is enabled on test failover NIC.</span></span>

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

### <span data-ttu-id="31608-119">-NicId</span><span class="sxs-lookup"><span data-stu-id="31608-119">-NicId</span></span>
<span data-ttu-id="31608-120">Укажите GUID сетевого адаптера ASR.</span><span class="sxs-lookup"><span data-stu-id="31608-120">Specify the ASR NIC GUID.</span></span>

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

### <span data-ttu-id="31608-121">-RecoveryLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="31608-121">-RecoveryLBBackendAddressPoolId</span></span>
<span data-ttu-id="31608-122">Указывает идентификаторы пулов серверных адресов для сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="31608-122">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="31608-123">-RecoveryNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="31608-123">-RecoveryNetworkSecurityGroupId</span></span>
<span data-ttu-id="31608-124">Указывает идентификатор NSG, связанного с сетевым адаптером восстановления.</span><span class="sxs-lookup"><span data-stu-id="31608-124">Specifies the ID of the NSG associated with recovery NIC.</span></span>

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

### <span data-ttu-id="31608-125">-RecoveryNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="31608-125">-RecoveryNicStaticIPAddress</span></span>
<span data-ttu-id="31608-126">Указывает IP-адрес сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="31608-126">Specifies the IP address of the recovery NIC.</span></span>

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

### <span data-ttu-id="31608-127">-RecoveryPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="31608-127">-RecoveryPublicIPAddressId</span></span>
<span data-ttu-id="31608-128">Указывает идентификатор общедоступного IP-адреса, связанного с сетевым адаптером восстановления.</span><span class="sxs-lookup"><span data-stu-id="31608-128">Specifies the ID of the public IP address associated with recovery NIC.</span></span>

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

### <span data-ttu-id="31608-129">-RecoveryVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="31608-129">-RecoveryVMNetworkId</span></span>
<span data-ttu-id="31608-130">Указывает идентификатор виртуальной сети восстановления.</span><span class="sxs-lookup"><span data-stu-id="31608-130">Specifies the ID of the recovery virtual network.</span></span>

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

### <span data-ttu-id="31608-131">-RecoveryVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="31608-131">-RecoveryVMSubnetName</span></span>
<span data-ttu-id="31608-132">Указывает имя подсети восстановления.</span><span class="sxs-lookup"><span data-stu-id="31608-132">Specifies the name of the recovery subnet.</span></span>

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

### <span data-ttu-id="31608-133">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="31608-133">-ReplicationProtectedItem</span></span>
<span data-ttu-id="31608-134">Укажите элемент, защищенный репликацией ASR.</span><span class="sxs-lookup"><span data-stu-id="31608-134">Specify the ASR Replication Protected Item.</span></span>

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

### <span data-ttu-id="31608-135">-TfoLBBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="31608-135">-TfoLBBackendAddressPoolId</span></span>
<span data-ttu-id="31608-136">Указывает идентификаторы пулов серверных адресов для сетевого адаптера восстановления.</span><span class="sxs-lookup"><span data-stu-id="31608-136">Specifies the IDs of backend address pools for the recovery NIC.</span></span>

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

### <span data-ttu-id="31608-137">-TfoNetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="31608-137">-TfoNetworkSecurityGroupId</span></span>
<span data-ttu-id="31608-138">Указывает идентификатор NSG, связанного с сетевым адаптером тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="31608-138">Specifies the ID of the NSG associated with test failover NIC.</span></span>

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

### <span data-ttu-id="31608-139">-TfoNicStaticIPAddress</span><span class="sxs-lookup"><span data-stu-id="31608-139">-TfoNicStaticIPAddress</span></span>
<span data-ttu-id="31608-140">Указывает IP-адрес тестового сетевого адаптера для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="31608-140">Specifies the IP address of the test failover NIC.</span></span>

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

### <span data-ttu-id="31608-141">-TfoPublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="31608-141">-TfoPublicIPAddressId</span></span>
<span data-ttu-id="31608-142">Указывает идентификатор общедоступного IP-адреса, связанного с сетевой адаптером тестового отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="31608-142">Specifies the ID of the public IP address associated with test failover NIC.</span></span>

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

### <span data-ttu-id="31608-143">-TfoVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="31608-143">-TfoVMNetworkId</span></span>
<span data-ttu-id="31608-144">Указывает идентификатор тестовой виртуальной сети для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="31608-144">Specifies the ID of the test failover virtual network.</span></span>

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

### <span data-ttu-id="31608-145">-TfoVMSubnetName</span><span class="sxs-lookup"><span data-stu-id="31608-145">-TfoVMSubnetName</span></span>
<span data-ttu-id="31608-146">Указывает имя подсети тестовой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="31608-146">Specifies the name of the test failover subnet.</span></span>

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

### <span data-ttu-id="31608-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31608-147">CommonParameters</span></span>
<span data-ttu-id="31608-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31608-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31608-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31608-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31608-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31608-150">INPUTS</span></span>

### <span data-ttu-id="31608-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="31608-151">None</span></span>

## <span data-ttu-id="31608-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31608-152">OUTPUTS</span></span>

### <span data-ttu-id="31608-153">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVMNicConfig</span><span class="sxs-lookup"><span data-stu-id="31608-153">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig</span></span>

## <span data-ttu-id="31608-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="31608-154">NOTES</span></span>

## <span data-ttu-id="31608-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31608-155">RELATED LINKS</span></span>
