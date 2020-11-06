---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpAddress.md
ms.openlocfilehash: 9864ba724d20e088e410bc99e8642fae97d71fd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568324"
---
# <span data-ttu-id="0f35e-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0f35e-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="0f35e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f35e-102">SYNOPSIS</span></span>
<span data-ttu-id="0f35e-103">Получает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0f35e-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f35e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f35e-104">SYNTAX</span></span>

### <span data-ttu-id="0f35e-105">NoExpandStandAloneIp (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f35e-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f35e-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="0f35e-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f35e-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="0f35e-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f35e-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="0f35e-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f35e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f35e-109">DESCRIPTION</span></span>
<span data-ttu-id="0f35e-110">Командлет **Get-AzureRmPublicIPAddress** получает один или несколько общедоступных IP-адресов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f35e-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="0f35e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f35e-111">EXAMPLES</span></span>

### <span data-ttu-id="0f35e-112">1: получение общедоступного IP-ресурса</span><span class="sxs-lookup"><span data-stu-id="0f35e-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="0f35e-113">Эта команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="0f35e-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="0f35e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f35e-114">PARAMETERS</span></span>

### <span data-ttu-id="0f35e-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="0f35e-115">-ExpandResource</span></span>
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

### <span data-ttu-id="0f35e-116">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0f35e-116">-IpConfigurationName</span></span>
<span data-ttu-id="0f35e-117">Имя IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0f35e-117">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="0f35e-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f35e-118">-Name</span></span>
<span data-ttu-id="0f35e-119">Указывает имя общедоступного IP-адреса, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0f35e-119">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0f35e-120">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="0f35e-120">-NetworkInterfaceName</span></span>
<span data-ttu-id="0f35e-121">Имя сетевого интерфейса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0f35e-121">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="0f35e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f35e-122">-ResourceGroupName</span></span>
<span data-ttu-id="0f35e-123">Указывает имя группы ресурсов, содержащей общедоступный IP-адрес, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0f35e-123">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0f35e-124">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="0f35e-124">-VirtualMachineIndex</span></span>
<span data-ttu-id="0f35e-125">Индекс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0f35e-125">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="0f35e-126">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0f35e-126">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="0f35e-127">Имя задания масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0f35e-127">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="0f35e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f35e-128">-DefaultProfile</span></span>
<span data-ttu-id="0f35e-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f35e-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f35e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f35e-130">CommonParameters</span></span>
<span data-ttu-id="0f35e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f35e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f35e-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f35e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f35e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f35e-133">INPUTS</span></span>

## <span data-ttu-id="0f35e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f35e-134">OUTPUTS</span></span>

### <span data-ttu-id="0f35e-135">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0f35e-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="0f35e-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f35e-136">NOTES</span></span>

## <span data-ttu-id="0f35e-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f35e-137">RELATED LINKS</span></span>

[<span data-ttu-id="0f35e-138">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0f35e-138">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="0f35e-139">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0f35e-139">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="0f35e-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="0f35e-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


