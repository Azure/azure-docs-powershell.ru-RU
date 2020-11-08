---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9C22F5D7-1FD0-4699-83D7-1D72C5234DEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d09173c43de9c01056055f714217db5eb4c58225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075993"
---
# <span data-ttu-id="8ef52-101">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="8ef52-101">New-AzureReservedIP</span></span>

## <span data-ttu-id="8ef52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ef52-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef52-103">Создает зарезервированный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8ef52-103">Creates a reserved IP address.</span></span>

## <span data-ttu-id="8ef52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ef52-104">SYNTAX</span></span>

### <span data-ttu-id="8ef52-105">CreateNewReservedIP (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ef52-105">CreateNewReservedIP (Default)</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ef52-106">CreateInUseReservedIPUsingSlot</span><span class="sxs-lookup"><span data-stu-id="8ef52-106">CreateInUseReservedIPUsingSlot</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ef52-107">CreateInUseReservedIP</span><span class="sxs-lookup"><span data-stu-id="8ef52-107">CreateInUseReservedIP</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8ef52-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ef52-108">DESCRIPTION</span></span>
<span data-ttu-id="8ef52-109">Командлет **New-AzureReservedIP** создает зарезервированный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8ef52-109">The **New-AzureReservedIP** cmdlet creates a reserved IP address.</span></span>

## <span data-ttu-id="8ef52-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ef52-110">EXAMPLES</span></span>

### <span data-ttu-id="8ef52-111">Пример 1: создание нового зарезервированного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="8ef52-111">Example 1: Create a new reserved IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName $Name -Label $Label -Location $Location
```

<span data-ttu-id="8ef52-112">Эта команда создает в подписке новый зарезервированный IP-адрес, который можно использовать для создания облачных служб, включающих веб-, рабочие и виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="8ef52-112">This command creates a new reserved IP address in the subscription, which can be used for creating cloud services that include Web, Worker, and Virtual Machines.</span></span>

### <span data-ttu-id="8ef52-113">Пример 2: создание зарезервированного IP-адреса на основе существующего IP-адреса</span><span class="sxs-lookup"><span data-stu-id="8ef52-113">Example 2: Create a reserved IP based on an existing IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName resip14 -Location "West Europe" -ServiceName piptestwesteurope
```

<span data-ttu-id="8ef52-114">Эта команда создает существующий VIP (виртуальный IP-адрес) для указанной службы.</span><span class="sxs-lookup"><span data-stu-id="8ef52-114">This command creates an existing VIP (Virtual IP) on the specified service.</span></span>

## <span data-ttu-id="8ef52-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ef52-115">PARAMETERS</span></span>

### <span data-ttu-id="8ef52-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8ef52-116">-InformationAction</span></span>
<span data-ttu-id="8ef52-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="8ef52-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8ef52-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8ef52-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8ef52-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="8ef52-119">Continue</span></span>
- <span data-ttu-id="8ef52-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="8ef52-120">Ignore</span></span>
- <span data-ttu-id="8ef52-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="8ef52-121">Inquire</span></span>
- <span data-ttu-id="8ef52-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8ef52-122">SilentlyContinue</span></span>
- <span data-ttu-id="8ef52-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="8ef52-123">Stop</span></span>
- <span data-ttu-id="8ef52-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="8ef52-124">Suspend</span></span>

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

### <span data-ttu-id="8ef52-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8ef52-125">-InformationVariable</span></span>
<span data-ttu-id="8ef52-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="8ef52-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8ef52-127">-Label</span><span class="sxs-lookup"><span data-stu-id="8ef52-127">-Label</span></span>
<span data-ttu-id="8ef52-128">Указывает метку для зарезервированного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="8ef52-128">Specifies a label for the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ef52-129">-Location</span><span class="sxs-lookup"><span data-stu-id="8ef52-129">-Location</span></span>
<span data-ttu-id="8ef52-130">Указывает место, на котором нужно создать зарезервированный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8ef52-130">Specifies a location at which to create the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ef52-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="8ef52-131">-Profile</span></span>
<span data-ttu-id="8ef52-132">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8ef52-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8ef52-133">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ef52-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8ef52-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="8ef52-134">-ReservedIPName</span></span>
<span data-ttu-id="8ef52-135">Задает зарезервированное имя IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="8ef52-135">Specifies the reserved IP address name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ef52-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8ef52-136">-ServiceName</span></span>
<span data-ttu-id="8ef52-137">Указывает имя службы.</span><span class="sxs-lookup"><span data-stu-id="8ef52-137">Specifies a service name.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ef52-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="8ef52-138">-Slot</span></span>
<span data-ttu-id="8ef52-139">Указывает слот развертывания.</span><span class="sxs-lookup"><span data-stu-id="8ef52-139">Specifies the deployment slot.</span></span>
<span data-ttu-id="8ef52-140">Допустимые значения этого параметра: "промежуточное хранение", "производство".</span><span class="sxs-lookup"><span data-stu-id="8ef52-140">The acceptable values for this parameter are: Staging, Production.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ef52-141">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="8ef52-141">-VirtualIPName</span></span>
<span data-ttu-id="8ef52-142">Указывает, что этот командлет использует параметр **VirtualIPName** , чтобы зарезервировать существующий виртуальный IP-адрес (VIP) в развертывании.</span><span class="sxs-lookup"><span data-stu-id="8ef52-142">Specifies that this cmdlet uses the **VirtualIPName** parameter to reserve an existing virtual IP address (VIP) in your deployment.</span></span>
<span data-ttu-id="8ef52-143">Если этот параметр не указан, этот командлет резервирует новый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8ef52-143">If this parameter is not specified, this cmdlet reserves a new VIP.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ef52-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef52-144">CommonParameters</span></span>
<span data-ttu-id="8ef52-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ef52-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef52-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ef52-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef52-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ef52-147">INPUTS</span></span>

## <span data-ttu-id="8ef52-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ef52-148">OUTPUTS</span></span>

## <span data-ttu-id="8ef52-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ef52-149">NOTES</span></span>

## <span data-ttu-id="8ef52-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ef52-150">RELATED LINKS</span></span>

[<span data-ttu-id="8ef52-151">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="8ef52-151">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="8ef52-152">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="8ef52-152">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


