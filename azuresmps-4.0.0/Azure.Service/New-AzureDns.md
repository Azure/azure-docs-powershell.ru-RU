---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075924"
---
# <span data-ttu-id="5e5ca-101">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5e5ca-101">New-AzureDns</span></span>

## <span data-ttu-id="5e5ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e5ca-102">SYNOPSIS</span></span>
<span data-ttu-id="5e5ca-103">Создает объект параметров DNS для Azure.</span><span class="sxs-lookup"><span data-stu-id="5e5ca-103">Creates an Azure DNS settings object.</span></span>

## <span data-ttu-id="5e5ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e5ca-104">SYNTAX</span></span>

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5e5ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e5ca-105">DESCRIPTION</span></span>
<span data-ttu-id="5e5ca-106">Командлет **New-AzureDns** создает объект параметров Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="5e5ca-106">The **New-AzureDns** cmdlet creates an Azure DNS settings object.</span></span>
<span data-ttu-id="5e5ca-107">Вы можете использовать объект параметров DNS при создании виртуальной машины с помощью командлета **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="5e5ca-107">You can use a DNS settings object when you create a virtual machine by using the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="5e5ca-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e5ca-108">EXAMPLES</span></span>

### <span data-ttu-id="5e5ca-109">Пример 1: создание объекта параметров DNS</span><span class="sxs-lookup"><span data-stu-id="5e5ca-109">Example 1: Create a DNS settings object</span></span>
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

<span data-ttu-id="5e5ca-110">Эта команда создает объект параметров Azure DNS.</span><span class="sxs-lookup"><span data-stu-id="5e5ca-110">This command creates an Azure DNS settings object.</span></span>
<span data-ttu-id="5e5ca-111">DNS-сервер имеет указанный адрес и понятное имя Dns01.</span><span class="sxs-lookup"><span data-stu-id="5e5ca-111">The DNS server has the specified address and the friendly name Dns01.</span></span>
<span data-ttu-id="5e5ca-112">Команда сохраняет объект в переменной $Dns для использования командлетом **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="5e5ca-112">The command stores the object in the $Dns variable for use by the **New-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="5e5ca-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e5ca-113">PARAMETERS</span></span>

### <span data-ttu-id="5e5ca-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5e5ca-114">-InformationAction</span></span>
<span data-ttu-id="5e5ca-115">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="5e5ca-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5e5ca-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5e5ca-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5e5ca-117">Продолжал</span><span class="sxs-lookup"><span data-stu-id="5e5ca-117">Continue</span></span>
- <span data-ttu-id="5e5ca-118">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="5e5ca-118">Ignore</span></span>
- <span data-ttu-id="5e5ca-119">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="5e5ca-119">Inquire</span></span>
- <span data-ttu-id="5e5ca-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5e5ca-120">SilentlyContinue</span></span>
- <span data-ttu-id="5e5ca-121">Остановить</span><span class="sxs-lookup"><span data-stu-id="5e5ca-121">Stop</span></span>
- <span data-ttu-id="5e5ca-122">Рвать</span><span class="sxs-lookup"><span data-stu-id="5e5ca-122">Suspend</span></span>

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

### <span data-ttu-id="5e5ca-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5e5ca-123">-InformationVariable</span></span>
<span data-ttu-id="5e5ca-124">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="5e5ca-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5e5ca-125">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="5e5ca-125">-IPAddress</span></span>
<span data-ttu-id="5e5ca-126">Указывает IP-адрес DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="5e5ca-126">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="5e5ca-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e5ca-127">-Name</span></span>
<span data-ttu-id="5e5ca-128">Задает понятное имя для DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="5e5ca-128">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="5e5ca-129">Это имя не обязательно является полным доменным именем.</span><span class="sxs-lookup"><span data-stu-id="5e5ca-129">This name is not necessarily a fully qualified domain name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e5ca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e5ca-130">CommonParameters</span></span>
<span data-ttu-id="5e5ca-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e5ca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e5ca-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e5ca-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e5ca-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e5ca-133">INPUTS</span></span>

## <span data-ttu-id="5e5ca-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e5ca-134">OUTPUTS</span></span>

## <span data-ttu-id="5e5ca-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e5ca-135">NOTES</span></span>

## <span data-ttu-id="5e5ca-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e5ca-136">RELATED LINKS</span></span>

[<span data-ttu-id="5e5ca-137">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5e5ca-137">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="5e5ca-138">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5e5ca-138">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="5e5ca-139">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="5e5ca-139">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="5e5ca-140">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5e5ca-140">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="5e5ca-141">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="5e5ca-141">Set-AzureDns</span></span>](./Set-AzureDns.md)


