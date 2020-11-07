---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: 4401ae153fc237d1f1bc9ccfa870e5cecc1e2c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904414"
---
# <span data-ttu-id="23526-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23526-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="23526-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23526-102">SYNOPSIS</span></span>
<span data-ttu-id="23526-103">Обновление службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="23526-103">Updates a private link service.</span></span>

## <span data-ttu-id="23526-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23526-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23526-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23526-105">DESCRIPTION</span></span>
<span data-ttu-id="23526-106">Командлет **Set-AzPrivateLinkService** обновляет службу частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="23526-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="23526-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23526-107">EXAMPLES</span></span>

### <span data-ttu-id="23526-108">1: создание службы частной ссылки и обновление ее</span><span class="sxs-lookup"><span data-stu-id="23526-108">1: Creates a private link service and update its</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
$privateLinkService = New-AzPrivateLinkService -ServiceName "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig

$newIPConfig = New-AzPrivateLinkServiceIpConfig -Name "New-IP-Config" -Subnet $vnet.subnets[0] 
$privateLinkService.IpConfigurations[0] = $newIPConfig
$privateLinkService | Set-AzPrivateLinkService
```

<span data-ttu-id="23526-109">В этом примере создается служба частной ссылки с именем mypls.</span><span class="sxs-lookup"><span data-stu-id="23526-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="23526-110">Затем он заменит ipConfigurations из объекта ipConfiguratiuon в памяти.</span><span class="sxs-lookup"><span data-stu-id="23526-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="23526-111">Затем командлет Set-AzPrivateLinkService используется для записи измененного состояния службы частной ссылки на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="23526-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="23526-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23526-112">PARAMETERS</span></span>

### <span data-ttu-id="23526-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23526-113">-AsJob</span></span>
<span data-ttu-id="23526-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="23526-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23526-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23526-115">-DefaultProfile</span></span>
<span data-ttu-id="23526-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23526-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23526-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23526-117">-PrivateLinkService</span></span>
<span data-ttu-id="23526-118">Указывает объект службы частной ссылки, представляющий состояние, в котором должна быть установлена служба частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="23526-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23526-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23526-119">CommonParameters</span></span>
<span data-ttu-id="23526-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23526-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23526-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23526-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23526-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23526-122">INPUTS</span></span>

### <span data-ttu-id="23526-123">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23526-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="23526-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23526-124">OUTPUTS</span></span>

### <span data-ttu-id="23526-125">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23526-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="23526-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="23526-126">NOTES</span></span>

## <span data-ttu-id="23526-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23526-127">RELATED LINKS</span></span>

[<span data-ttu-id="23526-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23526-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="23526-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23526-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="23526-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23526-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


