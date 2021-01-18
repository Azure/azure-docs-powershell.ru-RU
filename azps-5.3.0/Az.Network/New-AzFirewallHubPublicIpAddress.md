---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506942"
---
# <span data-ttu-id="7245e-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7245e-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="7245e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7245e-102">SYNOPSIS</span></span>
<span data-ttu-id="7245e-103">Public Ip assoicated to the firewall on virtual hub</span><span class="sxs-lookup"><span data-stu-id="7245e-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="7245e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7245e-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7245e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7245e-105">DESCRIPTION</span></span>
<span data-ttu-id="7245e-106">Public Ip assoicated to the firewall on virtual hub</span><span class="sxs-lookup"><span data-stu-id="7245e-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="7245e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7245e-107">EXAMPLES</span></span>

### <span data-ttu-id="7245e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7245e-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="7245e-109">В брандмауэре, подключенного к виртуальному концентратору, будут создаваться два общедоступных IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="7245e-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="7245e-110">При этом будет создаваться IP-адрес в backend. Мы не можем предоставить ipaddresses явным образом для нового брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="7245e-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="7245e-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7245e-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="7245e-112">Это позволит создать 1 новый общедоступный IP-адрес в брандмауэре, сохранив $publicIp 1, $publicIp 2, которые уже существуют в брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="7245e-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="7245e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7245e-113">PARAMETERS</span></span>

### <span data-ttu-id="7245e-114">-Addresses</span><span class="sxs-lookup"><span data-stu-id="7245e-114">-Addresses</span></span>
<span data-ttu-id="7245e-115">Общедоступные IP-адреса брандмауэра, подключенного к центру</span><span class="sxs-lookup"><span data-stu-id="7245e-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallPublicIpAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7245e-116">-Count</span><span class="sxs-lookup"><span data-stu-id="7245e-116">-Count</span></span>
<span data-ttu-id="7245e-117">Количество общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="7245e-117">The count of public Ip addresses</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7245e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7245e-118">-DefaultProfile</span></span>
<span data-ttu-id="7245e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7245e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7245e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7245e-120">CommonParameters</span></span>
<span data-ttu-id="7245e-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7245e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7245e-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7245e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7245e-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7245e-123">INPUTS</span></span>

### <span data-ttu-id="7245e-124">Нет</span><span class="sxs-lookup"><span data-stu-id="7245e-124">None</span></span>

## <span data-ttu-id="7245e-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7245e-125">OUTPUTS</span></span>

### <span data-ttu-id="7245e-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="7245e-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="7245e-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7245e-127">NOTES</span></span>

## <span data-ttu-id="7245e-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7245e-128">RELATED LINKS</span></span>
