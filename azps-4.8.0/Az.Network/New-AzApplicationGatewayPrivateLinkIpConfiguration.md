---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244873"
---
# <span data-ttu-id="7b550-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b550-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="7b550-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b550-102">SYNOPSIS</span></span>
<span data-ttu-id="7b550-103">Создание конфигурации IP, которая должна быть связана с конфигурацией PrivateLink</span><span class="sxs-lookup"><span data-stu-id="7b550-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="7b550-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b550-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b550-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b550-105">DESCRIPTION</span></span>
<span data-ttu-id="7b550-106">Командлет **New-AzApplicationGatewayPrivateLinkIpConfiguration** создает IP-конфигурацию, которая должна быть связана с конфигурацией PrivateLink для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="7b550-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="7b550-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b550-107">EXAMPLES</span></span>

### <span data-ttu-id="7b550-108">Пример 1: Настройка IP PrivateLink</span><span class="sxs-lookup"><span data-stu-id="7b550-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="7b550-109">Эта команда создает IP-конфигурацию PrivateLink с именем "ipConfig01", сохраняет результат в переменной с именем $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7b550-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="7b550-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b550-110">PARAMETERS</span></span>

### <span data-ttu-id="7b550-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b550-111">-DefaultProfile</span></span>
<span data-ttu-id="7b550-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b550-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b550-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7b550-113">-Name</span></span>
<span data-ttu-id="7b550-114">Имя IP</span><span class="sxs-lookup"><span data-stu-id="7b550-114">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="7b550-115">-Primary</span><span class="sxs-lookup"><span data-stu-id="7b550-115">-Primary</span></span>
<span data-ttu-id="7b550-116">Указывает, что IP-конфигурация является основной.</span><span class="sxs-lookup"><span data-stu-id="7b550-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="7b550-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="7b550-117">-PrivateIpAddress</span></span>
<span data-ttu-id="7b550-118">Частный IP-адрес для IP-адреса, если требуется статическая выделена.</span><span class="sxs-lookup"><span data-stu-id="7b550-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="7b550-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="7b550-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="7b550-120">IP-версия конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="7b550-120">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="7b550-121">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="7b550-121">-Subnet</span></span>
<span data-ttu-id="7b550-122">Связью</span><span class="sxs-lookup"><span data-stu-id="7b550-122">Subnet</span></span>

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

### <span data-ttu-id="7b550-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b550-123">CommonParameters</span></span>
<span data-ttu-id="7b550-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b550-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b550-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b550-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b550-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b550-126">INPUTS</span></span>

### <span data-ttu-id="7b550-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="7b550-127">None</span></span>

## <span data-ttu-id="7b550-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b550-128">OUTPUTS</span></span>

### <span data-ttu-id="7b550-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b550-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="7b550-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b550-130">NOTES</span></span>

## <span data-ttu-id="7b550-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b550-131">RELATED LINKS</span></span>

[<span data-ttu-id="7b550-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b550-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
