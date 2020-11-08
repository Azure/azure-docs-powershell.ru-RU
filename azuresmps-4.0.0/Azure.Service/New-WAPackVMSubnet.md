---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 83D18A17-94A4-4FB8-9DA6-F652D5BB84C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf06561ac5f8c9e0c19edb88b7a8ff5ef816c609
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075886"
---
# <span data-ttu-id="c63eb-101">New-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="c63eb-101">New-WAPackVMSubnet</span></span>

## <span data-ttu-id="c63eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c63eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c63eb-103">Создание подсети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c63eb-103">Creates a virtual machine subnet.</span></span>

## <span data-ttu-id="c63eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c63eb-104">SYNTAX</span></span>

```
New-WAPackVMSubnet -VNet <VMNetwork> -Name <String> -Subnet <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c63eb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c63eb-105">DESCRIPTION</span></span>
<span data-ttu-id="c63eb-106">Командлет **New-WAPackVMSubnet** создает подсеть виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c63eb-106">The **New-WAPackVMSubnet** cmdlet creates a virtual machine subnet.</span></span>

## <span data-ttu-id="c63eb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c63eb-107">EXAMPLES</span></span>

### <span data-ttu-id="c63eb-108">Пример 1: Создание подсети виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="c63eb-108">Example 1: Create a virtual machine subnet</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> New-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01" -Subnet "192.168.1.0/24"
```

<span data-ttu-id="c63eb-109">Первая команда сначала извлекает сеть виртуальной машины, к которой требуется добавить новую подсеть виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c63eb-109">The first command first retrieves the virtual machine network to which we want to add a new virtual machine subnet.</span></span>
<span data-ttu-id="c63eb-110">Эта сеть виртуальной машины называется ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="c63eb-110">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="c63eb-111">Вторая команда создает подсеть виртуальной машины, используя ранее извлеченную сеть виртуальной машины, имя ContosoVMSubnet01 и подсеть 192.168.1.0/24.</span><span class="sxs-lookup"><span data-stu-id="c63eb-111">The second command creates a virtual machine subnet using the previously retrieve virtual machine network, a name ContosoVMSubnet01 and a subnet 192.168.1.0/24.</span></span>

## <span data-ttu-id="c63eb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c63eb-112">PARAMETERS</span></span>

### <span data-ttu-id="c63eb-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c63eb-113">-Name</span></span>
<span data-ttu-id="c63eb-114">Задает имя для подсети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c63eb-114">Specifies a name for the virtual machine subnet.</span></span>

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

### <span data-ttu-id="c63eb-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="c63eb-115">-Profile</span></span>
<span data-ttu-id="c63eb-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c63eb-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c63eb-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c63eb-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c63eb-118">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="c63eb-118">-Subnet</span></span>
<span data-ttu-id="c63eb-119">Указывает подсеть для подсети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c63eb-119">Specifies a subnet for the virtual machine subnet.</span></span>

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

### <span data-ttu-id="c63eb-120">-VNet</span><span class="sxs-lookup"><span data-stu-id="c63eb-120">-VNet</span></span>
<span data-ttu-id="c63eb-121">Указывает виртуальную сеть, связанную с подсети виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c63eb-121">Specifies a VNet associated with the virtual machine subnet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c63eb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63eb-122">CommonParameters</span></span>
<span data-ttu-id="c63eb-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c63eb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63eb-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c63eb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63eb-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c63eb-125">INPUTS</span></span>

## <span data-ttu-id="c63eb-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c63eb-126">OUTPUTS</span></span>

## <span data-ttu-id="c63eb-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="c63eb-127">NOTES</span></span>

## <span data-ttu-id="c63eb-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c63eb-128">RELATED LINKS</span></span>

[<span data-ttu-id="c63eb-129">Get-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="c63eb-129">Get-WAPackVMSubnet</span></span>](./Get-WAPackVMSubnet.md)

[<span data-ttu-id="c63eb-130">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="c63eb-130">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="c63eb-131">Remove-WAPackVMSubnet</span><span class="sxs-lookup"><span data-stu-id="c63eb-131">Remove-WAPackVMSubnet</span></span>](./Remove-WAPackVMSubnet.md)


