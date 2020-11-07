---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: b9eaacb9a9d779814fc5f0b873aa8e98afedd362
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909878"
---
# <span data-ttu-id="89c74-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89c74-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="89c74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89c74-102">SYNOPSIS</span></span>
<span data-ttu-id="89c74-103">Получает общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="89c74-103">Gets a public IP address.</span></span>

## <span data-ttu-id="89c74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89c74-104">SYNTAX</span></span>

### <span data-ttu-id="89c74-105">NoExpandStandAloneIp (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89c74-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89c74-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="89c74-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89c74-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="89c74-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89c74-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="89c74-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89c74-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89c74-109">DESCRIPTION</span></span>
<span data-ttu-id="89c74-110">Командлет **Get-AzPublicIPAddress** получает один или несколько общедоступных IP-адресов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89c74-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="89c74-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89c74-111">EXAMPLES</span></span>

### <span data-ttu-id="89c74-112">1: получение общедоступного IP-ресурса</span><span class="sxs-lookup"><span data-stu-id="89c74-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="89c74-113">Эта команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="89c74-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="89c74-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89c74-114">PARAMETERS</span></span>

### <span data-ttu-id="89c74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c74-115">-DefaultProfile</span></span>
<span data-ttu-id="89c74-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89c74-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89c74-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="89c74-117">-ExpandResource</span></span>
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

### <span data-ttu-id="89c74-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="89c74-118">-IpConfigurationName</span></span>
<span data-ttu-id="89c74-119">Имя IP-конфигурации сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="89c74-119">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="89c74-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89c74-120">-Name</span></span>
<span data-ttu-id="89c74-121">Указывает имя общедоступного IP-адреса, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="89c74-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="89c74-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="89c74-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="89c74-123">Имя сетевого интерфейса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="89c74-123">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="89c74-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89c74-124">-ResourceGroupName</span></span>
<span data-ttu-id="89c74-125">Указывает имя группы ресурсов, содержащей общедоступный IP-адрес, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="89c74-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="89c74-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="89c74-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="89c74-127">Индекс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="89c74-127">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="89c74-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="89c74-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="89c74-129">Имя задания масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="89c74-129">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="89c74-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c74-130">CommonParameters</span></span>
<span data-ttu-id="89c74-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89c74-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c74-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89c74-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c74-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89c74-133">INPUTS</span></span>

## <span data-ttu-id="89c74-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89c74-134">OUTPUTS</span></span>

### <span data-ttu-id="89c74-135">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89c74-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="89c74-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="89c74-136">NOTES</span></span>

## <span data-ttu-id="89c74-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89c74-137">RELATED LINKS</span></span>

[<span data-ttu-id="89c74-138">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89c74-138">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="89c74-139">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89c74-139">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="89c74-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="89c74-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


