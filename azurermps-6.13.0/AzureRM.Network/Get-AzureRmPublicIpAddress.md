---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: b6d71d4c80ba30fc02bb22695132a304f94416cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562963"
---
# <span data-ttu-id="cd5d2-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cd5d2-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="cd5d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd5d2-102">SYNOPSIS</span></span>
<span data-ttu-id="cd5d2-103">Получает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="cd5d2-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd5d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd5d2-104">SYNTAX</span></span>

### <span data-ttu-id="cd5d2-105">NoExpandStandAloneIp (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd5d2-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd5d2-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="cd5d2-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd5d2-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="cd5d2-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd5d2-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="cd5d2-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd5d2-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd5d2-109">DESCRIPTION</span></span>
<span data-ttu-id="cd5d2-110">Командлет **Get-AzureRmPublicIPAddress** получает один или несколько общедоступных IP-адресов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cd5d2-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="cd5d2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd5d2-111">EXAMPLES</span></span>

### <span data-ttu-id="cd5d2-112">1: получение общедоступного IP-ресурса</span><span class="sxs-lookup"><span data-stu-id="cd5d2-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="cd5d2-113">Эта команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="cd5d2-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="cd5d2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd5d2-114">PARAMETERS</span></span>

### <span data-ttu-id="cd5d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd5d2-115">-DefaultProfile</span></span>
<span data-ttu-id="cd5d2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd5d2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd5d2-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="cd5d2-117">-ExpandResource</span></span>
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

### <span data-ttu-id="cd5d2-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cd5d2-118">-IpConfigurationName</span></span>
<span data-ttu-id="cd5d2-119">Имя IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cd5d2-119">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="cd5d2-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cd5d2-120">-Name</span></span>
<span data-ttu-id="cd5d2-121">Указывает имя общедоступного IP-адреса, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cd5d2-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5d2-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="cd5d2-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="cd5d2-123">Имя сетевого интерфейса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cd5d2-123">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="cd5d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd5d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd5d2-125">Указывает имя группы ресурсов, содержащей общедоступный IP-адрес, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cd5d2-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd5d2-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="cd5d2-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="cd5d2-127">Индекс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cd5d2-127">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="cd5d2-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cd5d2-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="cd5d2-129">Имя задания масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cd5d2-129">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="cd5d2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd5d2-130">CommonParameters</span></span>
<span data-ttu-id="cd5d2-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd5d2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd5d2-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd5d2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd5d2-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd5d2-133">INPUTS</span></span>

### <span data-ttu-id="cd5d2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cd5d2-134">System.String</span></span>

## <span data-ttu-id="cd5d2-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd5d2-135">OUTPUTS</span></span>

### <span data-ttu-id="cd5d2-136">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cd5d2-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="cd5d2-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd5d2-137">NOTES</span></span>

## <span data-ttu-id="cd5d2-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd5d2-138">RELATED LINKS</span></span>

[<span data-ttu-id="cd5d2-139">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cd5d2-139">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="cd5d2-140">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cd5d2-140">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="cd5d2-141">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="cd5d2-141">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


