---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: 1404acfa32de79096e990adbe2f66b43af0d4e96
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915154"
---
# <span data-ttu-id="68158-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="68158-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="68158-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68158-102">SYNOPSIS</span></span>
<span data-ttu-id="68158-103">Получает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="68158-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68158-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68158-104">SYNTAX</span></span>

### <span data-ttu-id="68158-105">NoExpandStandAloneIp (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="68158-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68158-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="68158-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68158-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="68158-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68158-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="68158-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68158-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68158-109">DESCRIPTION</span></span>
<span data-ttu-id="68158-110">Командлет **Get-AzureRmPublicIPAddress** получает один или несколько общедоступных IP-адресов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="68158-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="68158-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68158-111">EXAMPLES</span></span>

### <span data-ttu-id="68158-112">1: получение общедоступного IP-ресурса</span><span class="sxs-lookup"><span data-stu-id="68158-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="68158-113">Эта команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="68158-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="68158-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68158-114">PARAMETERS</span></span>

### <span data-ttu-id="68158-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68158-115">-DefaultProfile</span></span>
<span data-ttu-id="68158-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68158-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68158-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="68158-117">-ExpandResource</span></span>
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

### <span data-ttu-id="68158-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="68158-118">-IpConfigurationName</span></span>
<span data-ttu-id="68158-119">Имя IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="68158-119">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="68158-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="68158-120">-Name</span></span>
<span data-ttu-id="68158-121">Указывает имя общедоступного IP-адреса, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="68158-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="68158-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="68158-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="68158-123">Имя сетевого интерфейса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="68158-123">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="68158-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68158-124">-ResourceGroupName</span></span>
<span data-ttu-id="68158-125">Указывает имя группы ресурсов, содержащей общедоступный IP-адрес, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="68158-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="68158-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="68158-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="68158-127">Индекс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="68158-127">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="68158-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="68158-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="68158-129">Имя задания масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="68158-129">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="68158-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68158-130">CommonParameters</span></span>
<span data-ttu-id="68158-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68158-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68158-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68158-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68158-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68158-133">INPUTS</span></span>

## <span data-ttu-id="68158-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68158-134">OUTPUTS</span></span>

### <span data-ttu-id="68158-135">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="68158-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="68158-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="68158-136">NOTES</span></span>

## <span data-ttu-id="68158-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68158-137">RELATED LINKS</span></span>

[<span data-ttu-id="68158-138">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="68158-138">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="68158-139">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="68158-139">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="68158-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="68158-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


