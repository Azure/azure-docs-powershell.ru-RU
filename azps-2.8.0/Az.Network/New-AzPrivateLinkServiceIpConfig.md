---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: c7ea999af626206b741e86457d92627e4db196a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902098"
---
# <span data-ttu-id="258aa-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="258aa-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="258aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="258aa-102">SYNOPSIS</span></span>
<span data-ttu-id="258aa-103">Создание IP-конфигурации службы частной связи.</span><span class="sxs-lookup"><span data-stu-id="258aa-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="258aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="258aa-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="258aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="258aa-105">DESCRIPTION</span></span>
<span data-ttu-id="258aa-106">Командлет **New-AzPrivateLinkServiceIpConfig** создает IP-конфигурацию службы частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="258aa-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="258aa-107">Эта конфигурация используется для NAT источника и для входящего трафика из частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="258aa-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="258aa-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="258aa-108">EXAMPLES</span></span>

### <span data-ttu-id="258aa-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="258aa-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="258aa-110">Этот пример создает IP-конфигурацию службы частной ссылки в памяти.</span><span class="sxs-lookup"><span data-stu-id="258aa-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="258aa-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="258aa-111">PARAMETERS</span></span>

### <span data-ttu-id="258aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="258aa-112">-DefaultProfile</span></span>
<span data-ttu-id="258aa-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="258aa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="258aa-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="258aa-114">-Name</span></span>
<span data-ttu-id="258aa-115">Имя IP</span><span class="sxs-lookup"><span data-stu-id="258aa-115">The name of the IpConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="258aa-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="258aa-116">-PrivateIpAddress</span></span>
<span data-ttu-id="258aa-117">Частный IP-адрес для IP-адреса, если указана статическая область выделения.</span><span class="sxs-lookup"><span data-stu-id="258aa-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="258aa-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="258aa-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="258aa-119">IP-версия конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="258aa-119">The ip version of the ip configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="258aa-120">-Primary</span><span class="sxs-lookup"><span data-stu-id="258aa-120">-Primary</span></span>
<span data-ttu-id="258aa-121">Указывает, что текущая IP-конфигурация является основной или нет.</span><span class="sxs-lookup"><span data-stu-id="258aa-121">Indicate current ip configuration is primary or not.</span></span>

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

### <span data-ttu-id="258aa-122">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="258aa-122">-Subnet</span></span>
<span data-ttu-id="258aa-123">Связью</span><span class="sxs-lookup"><span data-stu-id="258aa-123">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="258aa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="258aa-124">CommonParameters</span></span>
<span data-ttu-id="258aa-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="258aa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="258aa-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="258aa-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="258aa-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="258aa-127">INPUTS</span></span>

### <span data-ttu-id="258aa-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="258aa-128">None</span></span>

## <span data-ttu-id="258aa-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="258aa-129">OUTPUTS</span></span>

### <span data-ttu-id="258aa-130">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="258aa-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="258aa-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="258aa-131">NOTES</span></span>

## <span data-ttu-id="258aa-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="258aa-132">RELATED LINKS</span></span>

[<span data-ttu-id="258aa-133">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="258aa-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)