---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: d9a0d35b58a69bca8a48cdb42342a720c8bc6da1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954115"
---
# <span data-ttu-id="83724-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83724-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="83724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83724-102">SYNOPSIS</span></span>
<span data-ttu-id="83724-103">Возвращает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="83724-103">Gets a public IP address.</span></span>

## <span data-ttu-id="83724-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="83724-104">SYNTAX</span></span>

### <span data-ttu-id="83724-105">NoExpandStandAloneIp (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="83724-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83724-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="83724-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83724-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="83724-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83724-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="83724-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83724-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83724-109">DESCRIPTION</span></span>
<span data-ttu-id="83724-110">С **помощью cmdlet Get-AzPublicIPAddress** можно получить один или несколько общедоступных IP-адресов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83724-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="83724-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="83724-111">EXAMPLES</span></span>

### <span data-ttu-id="83724-112">Пример 1. Получить общедоступный IP-ресурс</span><span class="sxs-lookup"><span data-stu-id="83724-112">Example 1: Get a public IP resource</span></span>
```powershell
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
                             "Name": "Basic", 
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="83724-113">Эта команда возвращает общедоступный IP-адрес ресурса с именем myPublicIp в группе ресурсов myRg.</span><span class="sxs-lookup"><span data-stu-id="83724-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="83724-114">Пример 2. Использование фильтрации для получения общедоступных IP-ресурсов</span><span class="sxs-lookup"><span data-stu-id="83724-114">Example 2: Get public IP resources using filtering</span></span>
```powershell
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
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="83724-115">Эта команда возвращает все общедоступные IP-адреса ресурсов, имя которых начинается с myPublicIp.</span><span class="sxs-lookup"><span data-stu-id="83724-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="83724-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83724-116">PARAMETERS</span></span>

### <span data-ttu-id="83724-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83724-117">-DefaultProfile</span></span>
<span data-ttu-id="83724-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83724-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83724-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="83724-119">-ExpandResource</span></span>
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

### <span data-ttu-id="83724-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="83724-120">-IpConfigurationName</span></span>
<span data-ttu-id="83724-121">Имя конфигурации IP-интерфейса сети.</span><span class="sxs-lookup"><span data-stu-id="83724-121">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="83724-122">-Name</span><span class="sxs-lookup"><span data-stu-id="83724-122">-Name</span></span>
<span data-ttu-id="83724-123">Указывает имя общего IP-адреса, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83724-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="83724-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="83724-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="83724-125">Имя сетевого интерфейса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="83724-125">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="83724-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83724-126">-ResourceGroupName</span></span>
<span data-ttu-id="83724-127">Имя группы ресурсов, которая содержит общедоступный IP-адрес, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83724-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="83724-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="83724-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="83724-129">Индекс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="83724-129">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="83724-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="83724-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="83724-131">Имя набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="83724-131">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="83724-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83724-132">CommonParameters</span></span>
<span data-ttu-id="83724-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83724-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83724-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83724-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83724-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83724-135">INPUTS</span></span>

### <span data-ttu-id="83724-136">System.String</span><span class="sxs-lookup"><span data-stu-id="83724-136">System.String</span></span>

## <span data-ttu-id="83724-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="83724-137">OUTPUTS</span></span>

### <span data-ttu-id="83724-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83724-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="83724-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="83724-139">NOTES</span></span>

## <span data-ttu-id="83724-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83724-140">RELATED LINKS</span></span>

[<span data-ttu-id="83724-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83724-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="83724-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83724-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="83724-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="83724-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


