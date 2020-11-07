---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 38eff375baa948098ac66c8e2b3c3fe1849f3bc0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902337"
---
# <span data-ttu-id="4d287-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4d287-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="4d287-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d287-102">SYNOPSIS</span></span>
<span data-ttu-id="4d287-103">Получает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="4d287-103">Gets a public IP address.</span></span>

## <span data-ttu-id="4d287-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d287-104">SYNTAX</span></span>

### <span data-ttu-id="4d287-105">NoExpandStandAloneIp (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d287-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d287-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="4d287-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d287-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="4d287-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d287-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="4d287-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d287-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d287-109">DESCRIPTION</span></span>
<span data-ttu-id="4d287-110">Командлет **Get-AzPublicIPAddress** получает один или несколько общедоступных IP-адресов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d287-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="4d287-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d287-111">EXAMPLES</span></span>

### <span data-ttu-id="4d287-112">1: получение общедоступного IP-ресурса</span><span class="sxs-lookup"><span data-stu-id="4d287-112">1: Get a public IP resource</span></span>
```
Get-AzPublicIpAddress -Name myPublicIp1 -ResourceGroupName myRg

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="4d287-113">Эта команда получает ресурс общедоступного IP-адреса с именем myPublicIp в группе ресурсов myRg.</span><span class="sxs-lookup"><span data-stu-id="4d287-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="4d287-114">2. получение общедоступных IP-ресурсов с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="4d287-114">2: Get public IP resources using filtering</span></span>
```
Get-AzPublicIpAddress -Name myPublicIp*

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="4d287-115">Эта команда получает все общедоступные IP-адреса ресурсов, имя которых начинается с myPublicIp.</span><span class="sxs-lookup"><span data-stu-id="4d287-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="4d287-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d287-116">PARAMETERS</span></span>

### <span data-ttu-id="4d287-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d287-117">-DefaultProfile</span></span>
<span data-ttu-id="4d287-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d287-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d287-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4d287-119">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d287-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4d287-120">-IpConfigurationName</span></span>
<span data-ttu-id="4d287-121">Имя IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4d287-121">Network Interface IP Configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d287-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4d287-122">-Name</span></span>
<span data-ttu-id="4d287-123">Указывает имя общедоступного IP-адреса, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4d287-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4d287-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="4d287-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="4d287-125">Имя сетевого интерфейса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4d287-125">Virtual Machine Network Interface Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d287-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d287-126">-ResourceGroupName</span></span>
<span data-ttu-id="4d287-127">Указывает имя группы ресурсов, содержащей общедоступный IP-адрес, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4d287-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4d287-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="4d287-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="4d287-129">Индекс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4d287-129">Virtual Machine Index.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d287-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4d287-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="4d287-131">Имя задания масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4d287-131">Virtual Machine Scale Set Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d287-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d287-132">CommonParameters</span></span>
<span data-ttu-id="4d287-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d287-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d287-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d287-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d287-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d287-135">INPUTS</span></span>

### <span data-ttu-id="4d287-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4d287-136">System.String</span></span>

## <span data-ttu-id="4d287-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d287-137">OUTPUTS</span></span>

### <span data-ttu-id="4d287-138">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4d287-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="4d287-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d287-139">NOTES</span></span>

## <span data-ttu-id="4d287-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d287-140">RELATED LINKS</span></span>

[<span data-ttu-id="4d287-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4d287-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="4d287-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4d287-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="4d287-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4d287-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


