---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413068"
---
# <span data-ttu-id="8815c-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8815c-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="8815c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8815c-102">SYNOPSIS</span></span>
<span data-ttu-id="8815c-103">Обновляет общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8815c-103">Updates a public IP address.</span></span>

## <span data-ttu-id="8815c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8815c-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8815c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8815c-105">DESCRIPTION</span></span>
<span data-ttu-id="8815c-106">С **помощью cmdlet Set-AzPublicIpAddress** можно обновить общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8815c-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="8815c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8815c-107">EXAMPLES</span></span>

### <span data-ttu-id="8815c-108">1. Изменение способа выделения общего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="8815c-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="8815c-109">Первая команда получает общедоступный IP-адрес ресурса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="8815c-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="8815c-110">Вторая команда задает для метода выделения объекта общего IP-адреса "Статический".</span><span class="sxs-lookup"><span data-stu-id="8815c-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="8815c-111">Set-AzPublicIPAddress обновляет общедоступный IP-адрес ресурса с обновленным объектом и изменяет способ выделения на "Статический".</span><span class="sxs-lookup"><span data-stu-id="8815c-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="8815c-112">Общедоступный IP-адрес выделяется немедленно.</span><span class="sxs-lookup"><span data-stu-id="8815c-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="8815c-113">2. Добавление метки домена DNS для общего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="8815c-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="8815c-114">Первая команда получает общедоступный IP-адрес ресурса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="8815c-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="8815c-115">Вторая команда задает для свойства DomainNameLabel необходимый префикс DNS.</span><span class="sxs-lookup"><span data-stu-id="8815c-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="8815c-116">Set-AzPublicIPAddress обновляет общедоступный IP-адрес ресурса с обновленным объектом.</span><span class="sxs-lookup"><span data-stu-id="8815c-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="8815c-117">Доменное имяLabel & FQDN будет изменено, как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="8815c-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="8815c-118">3. Изменение метки домена DNS для общего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="8815c-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="8815c-119">Первая команда получает общедоступный IP-адрес ресурса с именем $publicIPName в группе ресурсов $rgName.</span><span class="sxs-lookup"><span data-stu-id="8815c-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="8815c-120">Вторая команда задает для свойства DomainNameLabel необходимый префикс DNS.</span><span class="sxs-lookup"><span data-stu-id="8815c-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="8815c-121">Set-AzPublicIPAddress обновляет общедоступный IP-адрес ресурса с обновленным объектом.</span><span class="sxs-lookup"><span data-stu-id="8815c-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="8815c-122">Доменное имяLabel & FQDN будет изменено, как ожидалось.</span><span class="sxs-lookup"><span data-stu-id="8815c-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="8815c-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8815c-123">PARAMETERS</span></span>

### <span data-ttu-id="8815c-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8815c-124">-AsJob</span></span>
<span data-ttu-id="8815c-125">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8815c-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8815c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8815c-126">-DefaultProfile</span></span>
<span data-ttu-id="8815c-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8815c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8815c-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8815c-128">-PublicIpAddress</span></span>
<span data-ttu-id="8815c-129">Указывает общедоступный IP-адрес, представляющий состояние, в котором должен быть установлен общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8815c-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="8815c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8815c-130">CommonParameters</span></span>
<span data-ttu-id="8815c-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8815c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8815c-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8815c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8815c-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8815c-133">INPUTS</span></span>

### <span data-ttu-id="8815c-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8815c-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="8815c-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8815c-135">OUTPUTS</span></span>

### <span data-ttu-id="8815c-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8815c-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="8815c-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8815c-137">NOTES</span></span>

## <span data-ttu-id="8815c-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8815c-138">RELATED LINKS</span></span>

[<span data-ttu-id="8815c-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8815c-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="8815c-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8815c-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="8815c-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8815c-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


