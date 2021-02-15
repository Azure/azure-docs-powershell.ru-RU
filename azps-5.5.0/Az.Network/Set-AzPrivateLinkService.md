---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateLinkService.md
ms.openlocfilehash: a594e23505b9db1004a086ff4e0c168353c6bc28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218236"
---
# <span data-ttu-id="d2235-101">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d2235-101">Set-AzPrivateLinkService</span></span>

## <span data-ttu-id="d2235-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2235-102">SYNOPSIS</span></span>
<span data-ttu-id="d2235-103">Обновляет личную службу ссылок.</span><span class="sxs-lookup"><span data-stu-id="d2235-103">Updates a private link service.</span></span>

## <span data-ttu-id="d2235-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2235-104">SYNTAX</span></span>

```
Set-AzPrivateLinkService -PrivateLinkService <PSPrivateLinkService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2235-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2235-105">DESCRIPTION</span></span>
<span data-ttu-id="d2235-106">Для обновления закрытой службы ссылок будет создана ссылка на **веб-службу Set-AzPrivateLinkService.**</span><span class="sxs-lookup"><span data-stu-id="d2235-106">The **Set-AzPrivateLinkService** cmdlet updates a private link service.</span></span>

## <span data-ttu-id="d2235-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2235-107">EXAMPLES</span></span>

### <span data-ttu-id="d2235-108">1. Создание частной службы ссылок и обновление ее</span><span class="sxs-lookup"><span data-stu-id="d2235-108">1: Creates a private link service and update its</span></span>
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

<span data-ttu-id="d2235-109">В этом примере создается частная служба ссылок mypls.</span><span class="sxs-lookup"><span data-stu-id="d2235-109">This example creates a private link service called mypls.</span></span> <span data-ttu-id="d2235-110">Затем он заменяет свои ipConfigurations из объекта ipConfiguratiuon в памяти.</span><span class="sxs-lookup"><span data-stu-id="d2235-110">Then it replace its ipConfigurations from the in-memory ipConfiguratiuon object.</span></span> <span data-ttu-id="d2235-111">Затем Set-AzPrivateLinkService записи измененного состояния частной службы ссылок на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="d2235-111">The Set-AzPrivateLinkService cmdlet is then used to write the modified private link service state on the service side.</span></span> 

## <span data-ttu-id="d2235-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2235-112">PARAMETERS</span></span>

### <span data-ttu-id="d2235-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2235-113">-AsJob</span></span>
<span data-ttu-id="d2235-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d2235-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2235-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2235-115">-DefaultProfile</span></span>
<span data-ttu-id="d2235-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2235-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2235-117">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d2235-117">-PrivateLinkService</span></span>
<span data-ttu-id="d2235-118">Указывает объект закрытой службы ссылок, представляющий состояние, в котором должна быть установлена частная служба ссылок.</span><span class="sxs-lookup"><span data-stu-id="d2235-118">Specifies a private link service object representing the state to which the private link service should be set.</span></span>

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

### <span data-ttu-id="d2235-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2235-119">CommonParameters</span></span>
<span data-ttu-id="d2235-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2235-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2235-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2235-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2235-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2235-122">INPUTS</span></span>

### <span data-ttu-id="d2235-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d2235-123">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="d2235-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2235-124">OUTPUTS</span></span>

### <span data-ttu-id="d2235-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d2235-125">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="d2235-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2235-126">NOTES</span></span>

## <span data-ttu-id="d2235-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2235-127">RELATED LINKS</span></span>

[<span data-ttu-id="d2235-128">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d2235-128">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="d2235-129">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d2235-129">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)

[<span data-ttu-id="d2235-130">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="d2235-130">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)


