---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 73CEA6A8-46C9-4772-9A67-03F532696CFD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1287b3a0bb1cc39dea78fb4e92d2dcc4508c6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075543"
---
# <span data-ttu-id="4f7b8-101">Get-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="4f7b8-101">Get-AzureSubnet</span></span>

## <span data-ttu-id="4f7b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f7b8-102">SYNOPSIS</span></span>
<span data-ttu-id="4f7b8-103">Получает список подсетей, связанных с указанной виртуальной машиной Azure.</span><span class="sxs-lookup"><span data-stu-id="4f7b8-103">Gets a list of subnets associated with the specified Azure virtual machine.</span></span>

## <span data-ttu-id="4f7b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f7b8-104">SYNTAX</span></span>

```
Get-AzureSubnet -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4f7b8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f7b8-105">DESCRIPTION</span></span>
<span data-ttu-id="4f7b8-106">Командлет **Get-AzureSubnet** возвращает список подсетей, связанных с указанной виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="4f7b8-106">The **Get-AzureSubnet** cmdlet returns a list the subnets associated with the specified virtual machine.</span></span>
<span data-ttu-id="4f7b8-107">Укажите виртуальную машину с помощью **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="4f7b8-107">Use **Get-AzureVM** to specify the virtual machine.</span></span>

## <span data-ttu-id="4f7b8-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f7b8-108">EXAMPLES</span></span>

### <span data-ttu-id="4f7b8-109">Пример 1: получение подсетей для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="4f7b8-109">Example 1: Get subnets for a virtual machine</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine01"
C:\PS> Get-AzureSubnet -VM $VM
```

<span data-ttu-id="4f7b8-110">Первая команда получает виртуальную машину с именем VirtualMachine01 в службе с именем ContosoService03 и сохраняет ее в переменной $VM.</span><span class="sxs-lookup"><span data-stu-id="4f7b8-110">The first command gets a virtual machine named VirtualMachine01 in the service named ContosoService03, and then stores it in the $VM variable.</span></span>

<span data-ttu-id="4f7b8-111">Вторая команда получает подсети Azure для виртуальной машины в $VM.</span><span class="sxs-lookup"><span data-stu-id="4f7b8-111">The second command gets the Azure subnets for the virtual machine in $VM.</span></span>

## <span data-ttu-id="4f7b8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f7b8-112">PARAMETERS</span></span>

### <span data-ttu-id="4f7b8-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4f7b8-113">-InformationAction</span></span>
<span data-ttu-id="4f7b8-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="4f7b8-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4f7b8-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="4f7b8-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f7b8-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="4f7b8-116">Continue</span></span>
- <span data-ttu-id="4f7b8-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="4f7b8-117">Ignore</span></span>
- <span data-ttu-id="4f7b8-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="4f7b8-118">Inquire</span></span>
- <span data-ttu-id="4f7b8-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4f7b8-119">SilentlyContinue</span></span>
- <span data-ttu-id="4f7b8-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="4f7b8-120">Stop</span></span>
- <span data-ttu-id="4f7b8-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="4f7b8-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f7b8-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4f7b8-122">-InformationVariable</span></span>
<span data-ttu-id="4f7b8-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="4f7b8-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f7b8-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="4f7b8-124">-Profile</span></span>
<span data-ttu-id="4f7b8-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4f7b8-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f7b8-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4f7b8-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f7b8-127">-VM</span><span class="sxs-lookup"><span data-stu-id="4f7b8-127">-VM</span></span>
<span data-ttu-id="4f7b8-128">Указывает объект виртуальной машины, из которого нужно получить список подсетей.</span><span class="sxs-lookup"><span data-stu-id="4f7b8-128">Specifies the virtual machine object from which to get the subnet list.</span></span>

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

### <span data-ttu-id="4f7b8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f7b8-129">CommonParameters</span></span>
<span data-ttu-id="4f7b8-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f7b8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f7b8-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f7b8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f7b8-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f7b8-132">INPUTS</span></span>

## <span data-ttu-id="4f7b8-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f7b8-133">OUTPUTS</span></span>

## <span data-ttu-id="4f7b8-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f7b8-134">NOTES</span></span>

## <span data-ttu-id="4f7b8-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f7b8-135">RELATED LINKS</span></span>

[<span data-ttu-id="4f7b8-136">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4f7b8-136">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="4f7b8-137">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="4f7b8-137">Set-AzureSubnet</span></span>](./Set-AzureSubnet.md)


