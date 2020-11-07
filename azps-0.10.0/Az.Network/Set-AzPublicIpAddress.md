---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 53d5e15e6354e359461e59728e0776b7d3ec99ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911020"
---
# <span data-ttu-id="a95f6-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a95f6-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="a95f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a95f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a95f6-103">Задает состояние цели для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="a95f6-103">Sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="a95f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a95f6-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a95f6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a95f6-105">DESCRIPTION</span></span>
<span data-ttu-id="a95f6-106">Командлет **Set-AzPublicIpAddress** задает состояние цели для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="a95f6-106">The **Set-AzPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="a95f6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a95f6-107">EXAMPLES</span></span>

### <span data-ttu-id="a95f6-108">1: изменение метода выделения общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="a95f6-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="a95f6-109">First команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="a95f6-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="a95f6-110">Вторая команда задает метод выделения для объекта общего IP-адреса "static".</span><span class="sxs-lookup"><span data-stu-id="a95f6-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="a95f6-111">Set-AzPublicIPAddress команда обновляет ресурс общедоступного IP-адреса, используя обновленный объект, и изменяет метод выделения на static.</span><span class="sxs-lookup"><span data-stu-id="a95f6-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="a95f6-112">Общедоступный IP-адрес выделяется немедленно.</span><span class="sxs-lookup"><span data-stu-id="a95f6-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="a95f6-113">2. Изменение метки DNS-домена общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="a95f6-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="a95f6-114">First команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="a95f6-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="a95f6-115">Вторая команда задает для свойства DomainNameLabel требуемый префикс DNS.</span><span class="sxs-lookup"><span data-stu-id="a95f6-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="a95f6-116">Set-AzPublicIPAddress команда обновляет ресурс общедоступного IP-адреса с помощью обновленного объекта.</span><span class="sxs-lookup"><span data-stu-id="a95f6-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="a95f6-117">DomainNameLabel & FQDN изменяются должным образом.</span><span class="sxs-lookup"><span data-stu-id="a95f6-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="a95f6-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a95f6-118">PARAMETERS</span></span>

### <span data-ttu-id="a95f6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a95f6-119">-AsJob</span></span>
<span data-ttu-id="a95f6-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a95f6-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95f6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95f6-121">-DefaultProfile</span></span>
<span data-ttu-id="a95f6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a95f6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a95f6-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a95f6-123">-PublicIpAddress</span></span>
<span data-ttu-id="a95f6-124">Указывает объект **PublicIpAddress** , который представляет состояние цели, для которого должен быть установлен общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a95f6-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95f6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95f6-125">CommonParameters</span></span>
<span data-ttu-id="a95f6-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a95f6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95f6-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a95f6-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95f6-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a95f6-128">INPUTS</span></span>

### <span data-ttu-id="a95f6-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a95f6-129">PSPublicIpAddress</span></span>
<span data-ttu-id="a95f6-130">Параметр "PublicIpAddress" принимает значение типа "PSPublicIpAddress" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a95f6-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="a95f6-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a95f6-131">OUTPUTS</span></span>

### <span data-ttu-id="a95f6-132">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a95f6-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="a95f6-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a95f6-133">NOTES</span></span>

## <span data-ttu-id="a95f6-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a95f6-134">RELATED LINKS</span></span>

[<span data-ttu-id="a95f6-135">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a95f6-135">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="a95f6-136">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a95f6-136">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="a95f6-137">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a95f6-137">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


