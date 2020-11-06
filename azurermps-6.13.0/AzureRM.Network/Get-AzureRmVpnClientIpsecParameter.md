---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 539ae515d664aaeb01ca824603cd8ee3ed38f0fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562931"
---
# <span data-ttu-id="41af1-101">Get-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="41af1-101">Get-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="41af1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41af1-102">SYNOPSIS</span></span>
<span data-ttu-id="41af1-103">Получает параметры IPsec VPN, заданные для шлюза виртуальной сети, для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="41af1-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41af1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41af1-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41af1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41af1-105">DESCRIPTION</span></span>
<span data-ttu-id="41af1-106">Шлюз виртуальной сети — это объект, представляющий ваш шлюз в Azure.</span><span class="sxs-lookup"><span data-stu-id="41af1-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="41af1-107">Командлет **Get-AzureRmVpnClientIpsecParameter** возвращает объект параметров IPsec VPN, заданных на шлюзе в Azure на основе имени шлюза и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41af1-107">The **Get-AzureRmVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="41af1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41af1-108">EXAMPLES</span></span>

### <span data-ttu-id="41af1-109">1: получает параметры IPsec VPN, заданные для шлюза виртуальной сети, для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="41af1-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzureRmVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="41af1-110">Возвращает объект параметров IPsec VPN, заданных для шлюза виртуальной сети с именем "myGateway" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="41af1-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="41af1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41af1-111">PARAMETERS</span></span>

### <span data-ttu-id="41af1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41af1-112">-DefaultProfile</span></span>
<span data-ttu-id="41af1-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41af1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41af1-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41af1-114">-Name</span></span>
<span data-ttu-id="41af1-115">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="41af1-115">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41af1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41af1-116">-ResourceGroupName</span></span>
<span data-ttu-id="41af1-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="41af1-117">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41af1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41af1-118">CommonParameters</span></span>
<span data-ttu-id="41af1-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41af1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41af1-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41af1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41af1-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41af1-121">INPUTS</span></span>

### <span data-ttu-id="41af1-122">System. String</span><span class="sxs-lookup"><span data-stu-id="41af1-122">System.String</span></span>

## <span data-ttu-id="41af1-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41af1-123">OUTPUTS</span></span>

### <span data-ttu-id="41af1-124">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="41af1-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="41af1-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="41af1-125">NOTES</span></span>

## <span data-ttu-id="41af1-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41af1-126">RELATED LINKS</span></span>
