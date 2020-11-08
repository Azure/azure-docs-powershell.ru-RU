---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BABA5142-541F-40C8-AFF5-20E4283BE147
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a718e2f675b4a5e204610a2d4f1fb1aac4c5478
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076150"
---
# <span data-ttu-id="dc1ac-101">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="dc1ac-101">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>

## <span data-ttu-id="dc1ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc1ac-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1ac-103">Отменяет сетевую группу безопасности из подсети.</span><span class="sxs-lookup"><span data-stu-id="dc1ac-103">Dissociates a network security group from a subnet.</span></span>

## <span data-ttu-id="dc1ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc1ac-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupFromSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dc1ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc1ac-105">DESCRIPTION</span></span>
<span data-ttu-id="dc1ac-106">Командлет **Remove-AzureNetworkSecurityGroupFromSubnet** отменяет сетевую группу безопасности Azure из подсети.</span><span class="sxs-lookup"><span data-stu-id="dc1ac-106">The **Remove-AzureNetworkSecurityGroupFromSubnet** cmdlet dissociates an Azure network security group from a subnet.</span></span>

## <span data-ttu-id="dc1ac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc1ac-107">EXAMPLES</span></span>

## <span data-ttu-id="dc1ac-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc1ac-108">PARAMETERS</span></span>

### <span data-ttu-id="dc1ac-109">-Force</span><span class="sxs-lookup"><span data-stu-id="dc1ac-109">-Force</span></span>
<span data-ttu-id="dc1ac-110">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc1ac-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dc1ac-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc1ac-111">-Name</span></span>
<span data-ttu-id="dc1ac-112">Указывает имя группы безопасности сети, несвязанное с этим командлетом из подсети.</span><span class="sxs-lookup"><span data-stu-id="dc1ac-112">Specifies the name of the network security group that this cmdlet dissociates from a subnet.</span></span>

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

### <span data-ttu-id="dc1ac-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc1ac-113">-PassThru</span></span>
<span data-ttu-id="dc1ac-114">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="dc1ac-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="dc1ac-115">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="dc1ac-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dc1ac-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="dc1ac-116">-Profile</span></span>
<span data-ttu-id="dc1ac-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dc1ac-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="dc1ac-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dc1ac-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dc1ac-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="dc1ac-119">-SubnetName</span></span>
<span data-ttu-id="dc1ac-120">Указывает имя подсети, из которой этот командлет не отменяет сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="dc1ac-120">Specifies the name of a subnet from which this cmdlet dissociates a network security group.</span></span>

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

### <span data-ttu-id="dc1ac-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="dc1ac-121">-VirtualNetworkName</span></span>
<span data-ttu-id="dc1ac-122">Указывает имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="dc1ac-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="dc1ac-123">Этот командлет разрывает сетевую группу безопасности из подсети виртуальной сети, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="dc1ac-123">This cmdlet disassociates a network security group from a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc1ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1ac-124">CommonParameters</span></span>
<span data-ttu-id="dc1ac-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc1ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1ac-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc1ac-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1ac-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc1ac-127">INPUTS</span></span>

## <span data-ttu-id="dc1ac-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc1ac-128">OUTPUTS</span></span>

## <span data-ttu-id="dc1ac-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc1ac-129">NOTES</span></span>

## <span data-ttu-id="dc1ac-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc1ac-130">RELATED LINKS</span></span>

[<span data-ttu-id="dc1ac-131">Get-AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="dc1ac-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="dc1ac-132">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="dc1ac-132">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)


