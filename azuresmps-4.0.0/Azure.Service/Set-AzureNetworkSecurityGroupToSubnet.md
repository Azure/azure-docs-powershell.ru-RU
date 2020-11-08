---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A14F9105-1422-4073-96CF-E75CFC039E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7eaf1af2efe3f93f4e0a44d54e1f07ea52166942
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075829"
---
# <span data-ttu-id="11c59-101">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="11c59-101">Set-AzureNetworkSecurityGroupToSubnet</span></span>

## <span data-ttu-id="11c59-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11c59-102">SYNOPSIS</span></span>
<span data-ttu-id="11c59-103">Связывает группу безопасности сети с подсетью.</span><span class="sxs-lookup"><span data-stu-id="11c59-103">Associates a network security group to a subnet.</span></span>

## <span data-ttu-id="11c59-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11c59-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupToSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String> [-Force]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="11c59-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11c59-105">DESCRIPTION</span></span>
<span data-ttu-id="11c59-106">Командлет **Set-AzureNetworkSecurityGroupToSubnet** связывает группу безопасности сети Azure с подсетью.</span><span class="sxs-lookup"><span data-stu-id="11c59-106">The **Set-AzureNetworkSecurityGroupToSubnet** cmdlet associates an Azure network security group to a subnet.</span></span>

## <span data-ttu-id="11c59-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11c59-107">EXAMPLES</span></span>

## <span data-ttu-id="11c59-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11c59-108">PARAMETERS</span></span>

### <span data-ttu-id="11c59-109">-Force</span><span class="sxs-lookup"><span data-stu-id="11c59-109">-Force</span></span>
<span data-ttu-id="11c59-110">Указывает на то, что этот командлет не предложит вам подтвердить удаление предыдущей сетевой группы безопасности из подсети.</span><span class="sxs-lookup"><span data-stu-id="11c59-110">Indicates that this cmdlet does not prompt you to confirm the removal of a previous network security group from the subnet.</span></span>

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

### <span data-ttu-id="11c59-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11c59-111">-Name</span></span>
<span data-ttu-id="11c59-112">Указывает имя сетевой группы безопасности, которую этот командлет свяжет с подсетью.</span><span class="sxs-lookup"><span data-stu-id="11c59-112">Specifies the name of the network security group that this cmdlet associates to a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c59-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11c59-113">-PassThru</span></span>
<span data-ttu-id="11c59-114">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="11c59-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="11c59-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="11c59-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="11c59-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="11c59-116">-Profile</span></span>
<span data-ttu-id="11c59-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="11c59-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="11c59-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="11c59-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="11c59-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="11c59-119">-SubnetName</span></span>
<span data-ttu-id="11c59-120">Указывает имя подсети, в которую этот командлет связывает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="11c59-120">Specifies the name of a subnet to which this cmdlet associates a network security group.</span></span>

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

### <span data-ttu-id="11c59-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="11c59-121">-VirtualNetworkName</span></span>
<span data-ttu-id="11c59-122">Указывает имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="11c59-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="11c59-123">Этот командлет связывает группу безопасности сети с подсетью в виртуальной сети, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="11c59-123">This cmdlet associates a network security group to a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="11c59-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c59-124">CommonParameters</span></span>
<span data-ttu-id="11c59-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11c59-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c59-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11c59-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c59-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11c59-127">INPUTS</span></span>

## <span data-ttu-id="11c59-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11c59-128">OUTPUTS</span></span>

## <span data-ttu-id="11c59-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="11c59-129">NOTES</span></span>

## <span data-ttu-id="11c59-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11c59-130">RELATED LINKS</span></span>

[<span data-ttu-id="11c59-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="11c59-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="11c59-132">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="11c59-132">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)


