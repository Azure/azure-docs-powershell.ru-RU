---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073087"
---
# <span data-ttu-id="65215-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="65215-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="65215-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65215-102">SYNOPSIS</span></span>
<span data-ttu-id="65215-103">Обновление общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="65215-103">Updates a public IP address.</span></span>

## <span data-ttu-id="65215-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65215-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65215-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65215-105">DESCRIPTION</span></span>
<span data-ttu-id="65215-106">Командлет **Set-AzPublicIpAddress** обновляет общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="65215-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="65215-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65215-107">EXAMPLES</span></span>

### <span data-ttu-id="65215-108">1: изменение метода выделения общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="65215-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="65215-109">First команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="65215-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="65215-110">Вторая команда задает метод выделения для объекта общего IP-адреса "static".</span><span class="sxs-lookup"><span data-stu-id="65215-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="65215-111">Set-AzPublicIPAddress команда обновляет ресурс общедоступного IP-адреса, используя обновленный объект, и изменяет метод выделения на static.</span><span class="sxs-lookup"><span data-stu-id="65215-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="65215-112">Общедоступный IP-адрес выделяется немедленно.</span><span class="sxs-lookup"><span data-stu-id="65215-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="65215-113">2. Добавление метки DNS-домена для общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="65215-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="65215-114">First команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="65215-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="65215-115">Вторая команда задает для свойства DomainNameLabel требуемый префикс DNS.</span><span class="sxs-lookup"><span data-stu-id="65215-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="65215-116">Set-AzPublicIPAddress команда обновляет ресурс общедоступного IP-адреса с помощью обновленного объекта.</span><span class="sxs-lookup"><span data-stu-id="65215-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="65215-117">DomainNameLabel & FQDN изменяются должным образом.</span><span class="sxs-lookup"><span data-stu-id="65215-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="65215-118">3. Изменение метки DNS-домена общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="65215-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="65215-119">First команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="65215-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="65215-120">Вторая команда задает для свойства DomainNameLabel требуемый префикс DNS.</span><span class="sxs-lookup"><span data-stu-id="65215-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="65215-121">Set-AzPublicIPAddress команда обновляет ресурс общедоступного IP-адреса с помощью обновленного объекта.</span><span class="sxs-lookup"><span data-stu-id="65215-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="65215-122">DomainNameLabel & FQDN изменяются должным образом.</span><span class="sxs-lookup"><span data-stu-id="65215-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="65215-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65215-123">PARAMETERS</span></span>

### <span data-ttu-id="65215-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65215-124">-AsJob</span></span>
<span data-ttu-id="65215-125">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="65215-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65215-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65215-126">-DefaultProfile</span></span>
<span data-ttu-id="65215-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65215-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65215-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="65215-128">-PublicIpAddress</span></span>
<span data-ttu-id="65215-129">Указывает общедоступный объект IP-адреса, представляющий состояние, в котором должен быть установлен общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="65215-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65215-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65215-130">CommonParameters</span></span>
<span data-ttu-id="65215-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65215-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65215-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65215-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65215-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65215-133">INPUTS</span></span>

### <span data-ttu-id="65215-134">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="65215-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="65215-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65215-135">OUTPUTS</span></span>

### <span data-ttu-id="65215-136">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="65215-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="65215-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="65215-137">NOTES</span></span>

## <span data-ttu-id="65215-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65215-138">RELATED LINKS</span></span>

[<span data-ttu-id="65215-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="65215-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="65215-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="65215-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="65215-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="65215-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


