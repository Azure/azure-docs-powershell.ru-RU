---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: ed3b2de22c5f71c0782724f99c8325de4dea98b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562788"
---
# <span data-ttu-id="e2954-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2954-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="e2954-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e2954-102">SYNOPSIS</span></span>
<span data-ttu-id="e2954-103">Задает состояние цели для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e2954-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2954-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e2954-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2954-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2954-105">DESCRIPTION</span></span>
<span data-ttu-id="e2954-106">Командлет **Set-AzureRmPublicIpAddress** задает состояние цели для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="e2954-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="e2954-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e2954-107">EXAMPLES</span></span>

### <span data-ttu-id="e2954-108">1: изменение метода выделения общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="e2954-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="e2954-109">First команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="e2954-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="e2954-110">Вторая команда задает метод выделения для объекта общего IP-адреса "static".</span><span class="sxs-lookup"><span data-stu-id="e2954-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="e2954-111">Set-AzureRmPublicIPAddress команда обновляет ресурс общедоступного IP-адреса, используя обновленный объект, и изменяет метод выделения на static.</span><span class="sxs-lookup"><span data-stu-id="e2954-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="e2954-112">Общедоступный IP-адрес выделяется немедленно.</span><span class="sxs-lookup"><span data-stu-id="e2954-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="e2954-113">2. Изменение метки DNS-домена общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="e2954-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="e2954-114">First команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="e2954-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="e2954-115">Вторая команда задает для свойства DomainNameLabel требуемый префикс DNS.</span><span class="sxs-lookup"><span data-stu-id="e2954-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="e2954-116">Set-AzureRmPublicIPAddress команда обновляет ресурс общедоступного IP-адреса с помощью обновленного объекта.</span><span class="sxs-lookup"><span data-stu-id="e2954-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="e2954-117">DomainNameLabel & FQDN изменяются должным образом.</span><span class="sxs-lookup"><span data-stu-id="e2954-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="e2954-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e2954-118">PARAMETERS</span></span>

### <span data-ttu-id="e2954-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2954-119">-AsJob</span></span>
<span data-ttu-id="e2954-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e2954-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2954-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2954-121">-DefaultProfile</span></span>
<span data-ttu-id="e2954-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2954-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2954-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2954-123">-PublicIpAddress</span></span>
<span data-ttu-id="e2954-124">Указывает объект **PublicIpAddress** , который представляет состояние цели, для которого должен быть установлен общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="e2954-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="e2954-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2954-125">CommonParameters</span></span>
<span data-ttu-id="e2954-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e2954-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2954-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2954-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2954-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e2954-128">INPUTS</span></span>

### <span data-ttu-id="e2954-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2954-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>
<span data-ttu-id="e2954-130">Параметры: PublicIpAddress (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2954-130">Parameters: PublicIpAddress (ByValue)</span></span>

## <span data-ttu-id="e2954-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2954-131">OUTPUTS</span></span>

### <span data-ttu-id="e2954-132">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2954-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="e2954-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e2954-133">NOTES</span></span>

## <span data-ttu-id="e2954-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2954-134">RELATED LINKS</span></span>

[<span data-ttu-id="e2954-135">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2954-135">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="e2954-136">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2954-136">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="e2954-137">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e2954-137">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


