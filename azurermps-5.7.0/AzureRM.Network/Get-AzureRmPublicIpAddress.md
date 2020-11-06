---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: 769fd151f68da6a38c1cf4d5b3636d7990a92943
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560328"
---
# <span data-ttu-id="042bf-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="042bf-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="042bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="042bf-102">SYNOPSIS</span></span>
<span data-ttu-id="042bf-103">Получает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="042bf-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="042bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="042bf-104">SYNTAX</span></span>

### <span data-ttu-id="042bf-105">NoExpandStandAloneIp (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="042bf-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="042bf-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="042bf-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="042bf-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="042bf-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="042bf-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="042bf-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="042bf-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="042bf-109">DESCRIPTION</span></span>
<span data-ttu-id="042bf-110">Командлет **Get-AzureRmPublicIPAddress** получает один или несколько общедоступных IP-адресов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="042bf-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="042bf-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="042bf-111">EXAMPLES</span></span>

### <span data-ttu-id="042bf-112">1: получение общедоступного IP-ресурса</span><span class="sxs-lookup"><span data-stu-id="042bf-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="042bf-113">Эта команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="042bf-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="042bf-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="042bf-114">PARAMETERS</span></span>

### <span data-ttu-id="042bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="042bf-115">-DefaultProfile</span></span>
<span data-ttu-id="042bf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="042bf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="042bf-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="042bf-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042bf-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="042bf-118">-IpConfigurationName</span></span>
<span data-ttu-id="042bf-119">Имя IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="042bf-119">Network Interface IP Configuration Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042bf-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="042bf-120">-Name</span></span>
<span data-ttu-id="042bf-121">Указывает имя общедоступного IP-адреса, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="042bf-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042bf-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="042bf-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="042bf-123">Имя сетевого интерфейса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="042bf-123">Virtual Machine Network Interface Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042bf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="042bf-124">-ResourceGroupName</span></span>
<span data-ttu-id="042bf-125">Указывает имя группы ресурсов, содержащей общедоступный IP-адрес, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="042bf-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042bf-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="042bf-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="042bf-127">Индекс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="042bf-127">Virtual Machine Index.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042bf-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="042bf-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="042bf-129">Имя задания масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="042bf-129">Virtual Machine Scale Set Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="042bf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="042bf-130">CommonParameters</span></span>
<span data-ttu-id="042bf-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="042bf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="042bf-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="042bf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="042bf-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="042bf-133">INPUTS</span></span>

### <span data-ttu-id="042bf-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="042bf-134">None</span></span>
<span data-ttu-id="042bf-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="042bf-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="042bf-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="042bf-136">OUTPUTS</span></span>

### <span data-ttu-id="042bf-137">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="042bf-137">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="042bf-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="042bf-138">NOTES</span></span>

## <span data-ttu-id="042bf-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="042bf-139">RELATED LINKS</span></span>

[<span data-ttu-id="042bf-140">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="042bf-140">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="042bf-141">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="042bf-141">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="042bf-142">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="042bf-142">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


