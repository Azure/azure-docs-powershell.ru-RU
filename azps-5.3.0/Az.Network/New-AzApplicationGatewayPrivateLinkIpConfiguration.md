---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421871"
---
# <span data-ttu-id="23b2b-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="23b2b-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="23b2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="23b2b-103">Создает конфигурацию IP-адреса, которая будет связана с конфигурацией PrivateLink.</span><span class="sxs-lookup"><span data-stu-id="23b2b-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="23b2b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23b2b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23b2b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23b2b-105">DESCRIPTION</span></span>
<span data-ttu-id="23b2b-106">С **помощью cmdlet New-AzApplicationGatewayPrivateLinkIpConfiguration** создается конфигурация IP-адреса, которая будет связана с конфигурацией PrivateLink для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="23b2b-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="23b2b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23b2b-107">EXAMPLES</span></span>

### <span data-ttu-id="23b2b-108">Пример 1. Настройка IP-адреса PrivateLink</span><span class="sxs-lookup"><span data-stu-id="23b2b-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="23b2b-109">Эта команда создает конфигурацию IP-адреса PrivateLink с именем ipConfig01, в результате чего будет хранится переменная с именем $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="23b2b-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="23b2b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23b2b-110">PARAMETERS</span></span>

### <span data-ttu-id="23b2b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b2b-111">-DefaultProfile</span></span>
<span data-ttu-id="23b2b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23b2b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b2b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="23b2b-113">-Name</span></span>
<span data-ttu-id="23b2b-114">Имя ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="23b2b-114">The name of the IpConfiguration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b2b-115">-Primary</span><span class="sxs-lookup"><span data-stu-id="23b2b-115">-Primary</span></span>
<span data-ttu-id="23b2b-116">Указать, что конфигурация IP-адреса является основной.</span><span class="sxs-lookup"><span data-stu-id="23b2b-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="23b2b-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="23b2b-117">-PrivateIpAddress</span></span>
<span data-ttu-id="23b2b-118">Личный IP-адрес ipConfiguration, если требуется статическое выделение.</span><span class="sxs-lookup"><span data-stu-id="23b2b-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b2b-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="23b2b-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="23b2b-120">Ip-версия конфигурации IP-адреса</span><span class="sxs-lookup"><span data-stu-id="23b2b-120">The ip version of the ip configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b2b-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="23b2b-121">-Subnet</span></span>
<span data-ttu-id="23b2b-122">Подсеть</span><span class="sxs-lookup"><span data-stu-id="23b2b-122">Subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b2b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b2b-123">CommonParameters</span></span>
<span data-ttu-id="23b2b-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b2b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b2b-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23b2b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b2b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23b2b-126">INPUTS</span></span>

### <span data-ttu-id="23b2b-127">Нет</span><span class="sxs-lookup"><span data-stu-id="23b2b-127">None</span></span>

## <span data-ttu-id="23b2b-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23b2b-128">OUTPUTS</span></span>

### <span data-ttu-id="23b2b-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="23b2b-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="23b2b-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23b2b-130">NOTES</span></span>

## <span data-ttu-id="23b2b-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23b2b-131">RELATED LINKS</span></span>

[<span data-ttu-id="23b2b-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="23b2b-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)