---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: 1460b4497909d56e2d10d03e33df71518c52b796
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732430"
---
# <span data-ttu-id="34b93-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="34b93-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="34b93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34b93-102">SYNOPSIS</span></span>
<span data-ttu-id="34b93-103">Задает состояние цели для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="34b93-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34b93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34b93-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34b93-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34b93-105">DESCRIPTION</span></span>
<span data-ttu-id="34b93-106">Командлет **Set-AzureRmPublicIpAddress** задает состояние цели для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="34b93-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="34b93-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34b93-107">EXAMPLES</span></span>

### <span data-ttu-id="34b93-108">1: изменение метода выделения общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="34b93-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="34b93-109">First команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="34b93-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="34b93-110">Вторая команда задает метод выделения для объекта общего IP-адреса "static".</span><span class="sxs-lookup"><span data-stu-id="34b93-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="34b93-111">Set-AzureRmPublicIPAddress команда обновляет ресурс общедоступного IP-адреса, используя обновленный объект, и изменяет метод выделения на static.</span><span class="sxs-lookup"><span data-stu-id="34b93-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="34b93-112">Общедоступный IP-адрес выделяется немедленно.</span><span class="sxs-lookup"><span data-stu-id="34b93-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="34b93-113">2. Изменение метки DNS-домена общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="34b93-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="34b93-114">First команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="34b93-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="34b93-115">Вторая команда задает для свойства DomainNameLabel требуемый префикс DNS.</span><span class="sxs-lookup"><span data-stu-id="34b93-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="34b93-116">Set-AzureRmPublicIPAddress команда обновляет ресурс общедоступного IP-адреса с помощью обновленного объекта.</span><span class="sxs-lookup"><span data-stu-id="34b93-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="34b93-117">DomainNameLabel & FQDN изменяются должным образом.</span><span class="sxs-lookup"><span data-stu-id="34b93-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="34b93-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34b93-118">PARAMETERS</span></span>

### <span data-ttu-id="34b93-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="34b93-119">-PublicIpAddress</span></span>
<span data-ttu-id="34b93-120">Указывает объект **PublicIpAddress** , который представляет состояние цели, для которого должен быть установлен общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="34b93-120">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="34b93-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34b93-121">-DefaultProfile</span></span>
<span data-ttu-id="34b93-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34b93-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34b93-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34b93-123">CommonParameters</span></span>
<span data-ttu-id="34b93-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34b93-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34b93-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34b93-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34b93-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34b93-126">INPUTS</span></span>

### <span data-ttu-id="34b93-127">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="34b93-127">PSPublicIpAddress</span></span>
<span data-ttu-id="34b93-128">Параметр "PublicIpAddress" принимает значение типа "PSPublicIpAddress" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="34b93-128">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="34b93-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34b93-129">OUTPUTS</span></span>

### <span data-ttu-id="34b93-130">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="34b93-130">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="34b93-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="34b93-131">NOTES</span></span>

## <span data-ttu-id="34b93-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34b93-132">RELATED LINKS</span></span>

[<span data-ttu-id="34b93-133">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="34b93-133">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="34b93-134">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="34b93-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="34b93-135">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="34b93-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="34b93-136">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="34b93-136">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


