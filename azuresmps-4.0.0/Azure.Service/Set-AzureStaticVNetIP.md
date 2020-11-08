---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E54E4D16-DB2A-4626-B543-773C187B2E08
online version: ''
schema: 2.0.0
ms.openlocfilehash: d242418117b1bb576206f9ebb5fd568bd3e63cd1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075862"
---
# <span data-ttu-id="a9ce4-101">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="a9ce4-101">Set-AzureStaticVNetIP</span></span>

## <span data-ttu-id="a9ce4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ce4-103">Задает статическую информацию IP-адреса VNet для объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-103">Sets the static VNet IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="a9ce4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9ce4-104">SYNTAX</span></span>

```
Set-AzureStaticVNetIP [-IPAddress] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a9ce4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9ce4-105">DESCRIPTION</span></span>
<span data-ttu-id="a9ce4-106">Командлет **Set-AzureStaticVNetIP** устанавливает данные IP-адреса для статических виртуальных сетей (VNet) для объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-106">The **Set-AzureStaticVNetIP** cmdlet sets the static virtual network (VNet) IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="a9ce4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9ce4-107">EXAMPLES</span></span>

### <span data-ttu-id="a9ce4-108">Пример 1: Настройка IP-адреса виртуальной сети, связанного с виртуальной машиной</span><span class="sxs-lookup"><span data-stu-id="a9ce4-108">Example 1: Set the virtual network IP address associated with a virtual machine</span></span>
```
PS C:\> # Prerequisite: VNet has been set up with SubNet
          # Set-AzureVNetConfig -ConfigurationPath $vnetConfigPath;

          $vm = New-AzureVMConfig -Name $vmname -ImageName $img -InstanceSize $sz | Add-AzureProvisioningConfig -Windows -Password $pwd -AdminUsername $usr;
          $vm = Set-AzureSubNet -VM $vm -SubNetNames $sn;
          Set-AzureStaticVNetIP -IPAddress $ip -VM $vm;
          New-AzureVM -ServiceName $svc -VMs $vm -VNetName $vnetName -Location $loc;
```

<span data-ttu-id="a9ce4-109">Первая команда задает путь конфигурации для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-109">The first command sets the configuration path for a virtual network.</span></span>

<span data-ttu-id="a9ce4-110">Вторая команда создает конфигурацию виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-110">The second command creates a virtual machine configuration.</span></span>

<span data-ttu-id="a9ce4-111">Третья команда задает подсеть для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-111">The third command sets the subnet for the virtual machine.</span></span>

<span data-ttu-id="a9ce4-112">Четвертая команда задает IP-адрес виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-112">The fourth command sets the IP address for the virtual machine.</span></span>

<span data-ttu-id="a9ce4-113">Пятая команда создает виртуальную машину с помощью виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-113">The fifth command creates a virtual machine using the virtual machine.</span></span>

## <span data-ttu-id="a9ce4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9ce4-114">PARAMETERS</span></span>

### <span data-ttu-id="a9ce4-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a9ce4-115">-InformationAction</span></span>
<span data-ttu-id="a9ce4-116">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a9ce4-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a9ce4-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a9ce4-118">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a9ce4-118">Continue</span></span>
- <span data-ttu-id="a9ce4-119">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a9ce4-119">Ignore</span></span>
- <span data-ttu-id="a9ce4-120">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a9ce4-120">Inquire</span></span>
- <span data-ttu-id="a9ce4-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a9ce4-121">SilentlyContinue</span></span>
- <span data-ttu-id="a9ce4-122">Остановить</span><span class="sxs-lookup"><span data-stu-id="a9ce4-122">Stop</span></span>
- <span data-ttu-id="a9ce4-123">Рвать</span><span class="sxs-lookup"><span data-stu-id="a9ce4-123">Suspend</span></span>

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

### <span data-ttu-id="a9ce4-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a9ce4-124">-InformationVariable</span></span>
<span data-ttu-id="a9ce4-125">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a9ce4-126">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="a9ce4-126">-IPAddress</span></span>
<span data-ttu-id="a9ce4-127">Задает статический IP-адрес виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-127">Specifies the static VNet IP address</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ce4-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="a9ce4-128">-Profile</span></span>
<span data-ttu-id="a9ce4-129">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a9ce4-130">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a9ce4-131">-VM</span><span class="sxs-lookup"><span data-stu-id="a9ce4-131">-VM</span></span>
<span data-ttu-id="a9ce4-132">Указывает Сохраняемый объект виртуальной машины, для которого нужно задать статический IP-адрес виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-132">Specifies a persistent virtual machine object for which to set the static VNet IP address.</span></span>

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

### <span data-ttu-id="a9ce4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ce4-133">CommonParameters</span></span>
<span data-ttu-id="a9ce4-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9ce4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ce4-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9ce4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ce4-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9ce4-136">INPUTS</span></span>

## <span data-ttu-id="a9ce4-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9ce4-137">OUTPUTS</span></span>

## <span data-ttu-id="a9ce4-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9ce4-138">NOTES</span></span>

## <span data-ttu-id="a9ce4-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9ce4-139">RELATED LINKS</span></span>

[<span data-ttu-id="a9ce4-140">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="a9ce4-140">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="a9ce4-141">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="a9ce4-141">Test-AzureStaticVNetIP</span></span>](./Test-AzureStaticVNetIP.md)


