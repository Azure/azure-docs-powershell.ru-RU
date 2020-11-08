---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4D75240C-F2B5-4273-848C-107308DD6837
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d56de5b27565f7bfdd90198ad45e2766da521f4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075638"
---
# <span data-ttu-id="6f9ef-101">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="6f9ef-101">Get-AzureNetworkSecurityGroupForSubnet</span></span>

## <span data-ttu-id="6f9ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9ef-103">Получает сетевую группу безопасности для подсети.</span><span class="sxs-lookup"><span data-stu-id="6f9ef-103">Gets the network security group for a subnet.</span></span>

## <span data-ttu-id="6f9ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f9ef-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupForSubnet -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6f9ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f9ef-105">DESCRIPTION</span></span>
<span data-ttu-id="6f9ef-106">Командлет **Get-AzureNetworkSecurityGroupForSubnet** получает сетевую группу безопасности, связанную с подсетью.</span><span class="sxs-lookup"><span data-stu-id="6f9ef-106">The **Get-AzureNetworkSecurityGroupForSubnet** cmdlet gets the network security group that is associated to a subnet.</span></span>

## <span data-ttu-id="6f9ef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f9ef-107">EXAMPLES</span></span>

## <span data-ttu-id="6f9ef-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f9ef-108">PARAMETERS</span></span>

### <span data-ttu-id="6f9ef-109">-Подробно</span><span class="sxs-lookup"><span data-stu-id="6f9ef-109">-Detailed</span></span>
<span data-ttu-id="6f9ef-110">Указывает на то, что этот командлет отображает правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="6f9ef-110">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="6f9ef-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="6f9ef-111">-Profile</span></span>
<span data-ttu-id="6f9ef-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6f9ef-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6f9ef-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6f9ef-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f9ef-114">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6f9ef-114">-SubnetName</span></span>
<span data-ttu-id="6f9ef-115">Указывает имя подсети, для которой этот командлет получает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="6f9ef-115">Specifies the name of a subnet for which this cmdlet gets a network security group.</span></span>

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

### <span data-ttu-id="6f9ef-116">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6f9ef-116">-VirtualNetworkName</span></span>
<span data-ttu-id="6f9ef-117">Указывает имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6f9ef-117">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="6f9ef-118">Этот командлет получает сетевую группу безопасности для подсети в виртуальной сети, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="6f9ef-118">This cmdlet gets a network security group for a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f9ef-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f9ef-119">CommonParameters</span></span>
<span data-ttu-id="6f9ef-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f9ef-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f9ef-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f9ef-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f9ef-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f9ef-122">INPUTS</span></span>

## <span data-ttu-id="6f9ef-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f9ef-123">OUTPUTS</span></span>

## <span data-ttu-id="6f9ef-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f9ef-124">NOTES</span></span>

## <span data-ttu-id="6f9ef-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f9ef-125">RELATED LINKS</span></span>

[<span data-ttu-id="6f9ef-126">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="6f9ef-126">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)

[<span data-ttu-id="6f9ef-127">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="6f9ef-127">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)
