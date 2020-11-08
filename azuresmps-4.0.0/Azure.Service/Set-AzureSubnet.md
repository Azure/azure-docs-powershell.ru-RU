---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 69974370-4542-4417-BD9D-3928EB005C31
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81d6e523978196a47b01d21aa8e857027b0b4f40
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075951"
---
# <span data-ttu-id="1c5ce-101">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="1c5ce-101">Set-AzureSubnet</span></span>

## <span data-ttu-id="1c5ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="1c5ce-103">Определяет список подсетей для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="1c5ce-103">Defines the subnet list for an Azure virtual machine.</span></span>

## <span data-ttu-id="1c5ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c5ce-104">SYNTAX</span></span>

```
Set-AzureSubnet [-SubnetNames] <String[]> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1c5ce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c5ce-105">DESCRIPTION</span></span>
<span data-ttu-id="1c5ce-106">Командлет **Set-AzureSubnet** задает список подсетей для конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1c5ce-106">The **Set-AzureSubnet** cmdlet sets the subnet list for a virtual machine configuration.</span></span>
<span data-ttu-id="1c5ce-107">Использование с помощью **New-AzureVM** для настройки подсетей для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1c5ce-107">Use with **New-AzureVM** to set the subnets for a virtual machine.</span></span>

## <span data-ttu-id="1c5ce-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c5ce-108">EXAMPLES</span></span>

### <span data-ttu-id="1c5ce-109">Пример 1: Добавление подсети в конфигурацию виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="1c5ce-109">Example 1: Add a subnet to a virtual machine configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine04" -ImageName $image -InstanceSize "Small" | Add-AzureProvisioningConfig -Windows -Password "password" | Set-AzureSubnet "PubSubnet","PrivSubnet" | New-AzureVM -ServiceName "ContosoService03"
```

<span data-ttu-id="1c5ce-110">Эта команда добавляет подсеть в конфигурацию виртуальной машины, а затем создает виртуальную машину с именем VirtualMachine04.</span><span class="sxs-lookup"><span data-stu-id="1c5ce-110">This command adds a subnet to the virtual machine configuration, and then creates the virtual machine named VirtualMachine04.</span></span>

## <span data-ttu-id="1c5ce-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c5ce-111">PARAMETERS</span></span>

### <span data-ttu-id="1c5ce-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1c5ce-112">-InformationAction</span></span>
<span data-ttu-id="1c5ce-113">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="1c5ce-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1c5ce-114">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1c5ce-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c5ce-115">Продолжал</span><span class="sxs-lookup"><span data-stu-id="1c5ce-115">Continue</span></span>
- <span data-ttu-id="1c5ce-116">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="1c5ce-116">Ignore</span></span>
- <span data-ttu-id="1c5ce-117">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="1c5ce-117">Inquire</span></span>
- <span data-ttu-id="1c5ce-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1c5ce-118">SilentlyContinue</span></span>
- <span data-ttu-id="1c5ce-119">Остановить</span><span class="sxs-lookup"><span data-stu-id="1c5ce-119">Stop</span></span>
- <span data-ttu-id="1c5ce-120">Рвать</span><span class="sxs-lookup"><span data-stu-id="1c5ce-120">Suspend</span></span>

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

### <span data-ttu-id="1c5ce-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1c5ce-121">-InformationVariable</span></span>
<span data-ttu-id="1c5ce-122">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="1c5ce-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1c5ce-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="1c5ce-123">-Profile</span></span>
<span data-ttu-id="1c5ce-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1c5ce-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1c5ce-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c5ce-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1c5ce-126">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="1c5ce-126">-SubnetNames</span></span>
<span data-ttu-id="1c5ce-127">Указывает массив, который содержит список имен подсетей.</span><span class="sxs-lookup"><span data-stu-id="1c5ce-127">Specifies an array that contains the list of subnet names.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c5ce-128">-VM</span><span class="sxs-lookup"><span data-stu-id="1c5ce-128">-VM</span></span>
<span data-ttu-id="1c5ce-129">Указывает объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1c5ce-129">Specifies the virtual machine object.</span></span>

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

### <span data-ttu-id="1c5ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c5ce-130">CommonParameters</span></span>
<span data-ttu-id="1c5ce-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c5ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c5ce-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c5ce-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c5ce-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c5ce-133">INPUTS</span></span>

## <span data-ttu-id="1c5ce-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c5ce-134">OUTPUTS</span></span>

## <span data-ttu-id="1c5ce-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c5ce-135">NOTES</span></span>

## <span data-ttu-id="1c5ce-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c5ce-136">RELATED LINKS</span></span>

[<span data-ttu-id="1c5ce-137">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1c5ce-137">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="1c5ce-138">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1c5ce-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="1c5ce-139">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="1c5ce-139">Update-AzureVM</span></span>](./Update-AzureVM.md)


