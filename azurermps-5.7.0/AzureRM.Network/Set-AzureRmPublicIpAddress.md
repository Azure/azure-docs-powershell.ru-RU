---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: df1c03551d520a833e8b974ae2a2b71fe442c4c4
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93735212"
---
# <span data-ttu-id="52ef0-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52ef0-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="52ef0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="52ef0-103">Задает состояние цели для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="52ef0-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52ef0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52ef0-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52ef0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52ef0-105">DESCRIPTION</span></span>
<span data-ttu-id="52ef0-106">Командлет **Set-AzureRmPublicIpAddress** задает состояние цели для общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="52ef0-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="52ef0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52ef0-107">EXAMPLES</span></span>

### <span data-ttu-id="52ef0-108">1: изменение метода выделения общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="52ef0-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="52ef0-109">First команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="52ef0-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="52ef0-110">Вторая команда задает метод выделения для объекта общего IP-адреса "static".</span><span class="sxs-lookup"><span data-stu-id="52ef0-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="52ef0-111">Set-AzureRmPublicIPAddress команда обновляет ресурс общедоступного IP-адреса, используя обновленный объект, и изменяет метод выделения на static.</span><span class="sxs-lookup"><span data-stu-id="52ef0-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="52ef0-112">Общедоступный IP-адрес выделяется немедленно.</span><span class="sxs-lookup"><span data-stu-id="52ef0-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="52ef0-113">2. Изменение метки DNS-домена общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="52ef0-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="52ef0-114">First команда получает ресурс общедоступного IP-адреса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="52ef0-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="52ef0-115">Вторая команда задает для свойства DomainNameLabel требуемый префикс DNS.</span><span class="sxs-lookup"><span data-stu-id="52ef0-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="52ef0-116">Set-AzureRmPublicIPAddress команда обновляет ресурс общедоступного IP-адреса с помощью обновленного объекта.</span><span class="sxs-lookup"><span data-stu-id="52ef0-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="52ef0-117">DomainNameLabel & FQDN изменяются должным образом.</span><span class="sxs-lookup"><span data-stu-id="52ef0-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="52ef0-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52ef0-118">PARAMETERS</span></span>

### <span data-ttu-id="52ef0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52ef0-119">-AsJob</span></span>
<span data-ttu-id="52ef0-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="52ef0-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52ef0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ef0-121">-DefaultProfile</span></span>
<span data-ttu-id="52ef0-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52ef0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52ef0-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52ef0-123">-PublicIpAddress</span></span>
<span data-ttu-id="52ef0-124">Указывает объект **PublicIpAddress** , который представляет состояние цели, для которого должен быть установлен общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="52ef0-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="52ef0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ef0-125">CommonParameters</span></span>
<span data-ttu-id="52ef0-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52ef0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ef0-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ef0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ef0-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52ef0-128">INPUTS</span></span>

### <span data-ttu-id="52ef0-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52ef0-129">PSPublicIpAddress</span></span>
<span data-ttu-id="52ef0-130">Параметр "PublicIpAddress" принимает значение типа "PSPublicIpAddress" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="52ef0-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="52ef0-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52ef0-131">OUTPUTS</span></span>

### <span data-ttu-id="52ef0-132">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52ef0-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="52ef0-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="52ef0-133">NOTES</span></span>

## <span data-ttu-id="52ef0-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52ef0-134">RELATED LINKS</span></span>

[<span data-ttu-id="52ef0-135">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52ef0-135">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="52ef0-136">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52ef0-136">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="52ef0-137">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52ef0-137">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


