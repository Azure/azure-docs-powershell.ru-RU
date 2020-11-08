---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: FCB3C8EB-EAA6-48E3-A1A5-DB3050821BD8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 402aa39fb1476d6b3bc69902148e71549fccb3fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076333"
---
# <span data-ttu-id="7cf03-101">Get-AzureNetworkSecurityGroupConfig</span><span class="sxs-lookup"><span data-stu-id="7cf03-101">Get-AzureNetworkSecurityGroupConfig</span></span>

## <span data-ttu-id="7cf03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7cf03-102">SYNOPSIS</span></span>
<span data-ttu-id="7cf03-103">Получение сведений о группе безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="7cf03-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="7cf03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7cf03-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroupConfig [-Detailed] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="7cf03-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cf03-105">DESCRIPTION</span></span>
<span data-ttu-id="7cf03-106">Командлет **Get-AzureNetworkSecurityGroupConfig** возвращает сведения о сетевой группе безопасности.</span><span class="sxs-lookup"><span data-stu-id="7cf03-106">The **Get-AzureNetworkSecurityGroupConfig** cmdlet returns details for a network security group.</span></span>
<span data-ttu-id="7cf03-107">Укажите *подробный* параметр для отображения правил сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="7cf03-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="7cf03-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7cf03-108">EXAMPLES</span></span>

## <span data-ttu-id="7cf03-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7cf03-109">PARAMETERS</span></span>

### <span data-ttu-id="7cf03-110">-Подробно</span><span class="sxs-lookup"><span data-stu-id="7cf03-110">-Detailed</span></span>
<span data-ttu-id="7cf03-111">Указывает на то, что этот командлет отображает правила сетевой безопасности.</span><span class="sxs-lookup"><span data-stu-id="7cf03-111">Indicates that this cmdlet displays the network security rules.</span></span>

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

### <span data-ttu-id="7cf03-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="7cf03-112">-Profile</span></span>
<span data-ttu-id="7cf03-113">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7cf03-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7cf03-114">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7cf03-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7cf03-115">-VM</span><span class="sxs-lookup"><span data-stu-id="7cf03-115">-VM</span></span>
<span data-ttu-id="7cf03-116">Указывает виртуальную машину, для которой этот командлет получает сведения о сетевой группе безопасности.</span><span class="sxs-lookup"><span data-stu-id="7cf03-116">Specifies the virtual machine for which this cmdlet gets the details of a network security group.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cf03-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cf03-117">CommonParameters</span></span>
<span data-ttu-id="7cf03-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7cf03-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cf03-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cf03-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cf03-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7cf03-120">INPUTS</span></span>

## <span data-ttu-id="7cf03-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cf03-121">OUTPUTS</span></span>

## <span data-ttu-id="7cf03-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="7cf03-122">NOTES</span></span>

## <span data-ttu-id="7cf03-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cf03-123">RELATED LINKS</span></span>

[<span data-ttu-id="7cf03-124">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7cf03-124">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="7cf03-125">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7cf03-125">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)


