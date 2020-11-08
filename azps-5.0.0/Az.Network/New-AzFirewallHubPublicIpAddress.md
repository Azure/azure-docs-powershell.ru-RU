---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248322"
---
# <span data-ttu-id="ee64a-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="ee64a-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="ee64a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee64a-102">SYNOPSIS</span></span>
<span data-ttu-id="ee64a-103">Общедоступный IP-assoicated в брандмауэр на виртуальном концентраторе</span><span class="sxs-lookup"><span data-stu-id="ee64a-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="ee64a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee64a-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee64a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee64a-105">DESCRIPTION</span></span>
<span data-ttu-id="ee64a-106">Общедоступный IP-assoicated в брандмауэр на виртуальном концентраторе</span><span class="sxs-lookup"><span data-stu-id="ee64a-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="ee64a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee64a-107">EXAMPLES</span></span>

### <span data-ttu-id="ee64a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee64a-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="ee64a-109">На брандмауэре, подключенном к виртуальному концентратору, будет создано 2 общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="ee64a-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="ee64a-110">Это приведет к созданию IP-адреса в серверной части. Мы не можем предоставить ipaddresses явным образом для нового брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ee64a-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="ee64a-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ee64a-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="ee64a-112">Для этого на брандмауэре будет создан 1 новый общедоступный IP-адрес, сохранив $publicIp 1, $publicIp 2, уже существующие в брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="ee64a-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="ee64a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee64a-113">PARAMETERS</span></span>

### <span data-ttu-id="ee64a-114">-Адреса</span><span class="sxs-lookup"><span data-stu-id="ee64a-114">-Addresses</span></span>
<span data-ttu-id="ee64a-115">Общедоступные IP-адреса брандмауэра, подключенного к концентратору</span><span class="sxs-lookup"><span data-stu-id="ee64a-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="ee64a-116">— Количество</span><span class="sxs-lookup"><span data-stu-id="ee64a-116">-Count</span></span>
<span data-ttu-id="ee64a-117">Количество общедоступных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="ee64a-117">The count of public Ip addresses</span></span>

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

### <span data-ttu-id="ee64a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee64a-118">-DefaultProfile</span></span>
<span data-ttu-id="ee64a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee64a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee64a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee64a-120">CommonParameters</span></span>
<span data-ttu-id="ee64a-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee64a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee64a-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee64a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee64a-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee64a-123">INPUTS</span></span>

### <span data-ttu-id="ee64a-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="ee64a-124">None</span></span>

## <span data-ttu-id="ee64a-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee64a-125">OUTPUTS</span></span>

### <span data-ttu-id="ee64a-126">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="ee64a-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="ee64a-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee64a-127">NOTES</span></span>

## <span data-ttu-id="ee64a-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee64a-128">RELATED LINKS</span></span>
