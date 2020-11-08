---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AF4DF7EC-95BA-44E2-AB9B-5C8FE45CCE4C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83c0858d813c157301098f680fa9d2a90ef6950a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075734"
---
# <span data-ttu-id="43d17-101">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="43d17-101">Add-AzureDns</span></span>

## <span data-ttu-id="43d17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43d17-102">SYNOPSIS</span></span>
<span data-ttu-id="43d17-103">Добавляет DNS-сервер в службу Azure.</span><span class="sxs-lookup"><span data-stu-id="43d17-103">Adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="43d17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43d17-104">SYNTAX</span></span>

```
Add-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="43d17-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43d17-105">DESCRIPTION</span></span>
<span data-ttu-id="43d17-106">Командлет **Add-AzureDns** добавляет DNS-сервер в службу Azure.</span><span class="sxs-lookup"><span data-stu-id="43d17-106">The **Add-AzureDns** cmdlet adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="43d17-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43d17-107">EXAMPLES</span></span>

### <span data-ttu-id="43d17-108">Пример 1: Добавление DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="43d17-108">Example 1: Add a DNS server</span></span>
```
PS C:\> Add-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.4 -Name "Dns07"
```

<span data-ttu-id="43d17-109">Эта команда добавляет DNS-сервер с адресом 10.1.2.4 в ContosoService.</span><span class="sxs-lookup"><span data-stu-id="43d17-109">This command adds the DNS server that has the address 10.1.2.4 to ContosoService.</span></span>

## <span data-ttu-id="43d17-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43d17-110">PARAMETERS</span></span>

### <span data-ttu-id="43d17-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="43d17-111">-InformationAction</span></span>
<span data-ttu-id="43d17-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="43d17-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="43d17-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="43d17-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="43d17-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="43d17-114">Continue</span></span>
- <span data-ttu-id="43d17-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="43d17-115">Ignore</span></span>
- <span data-ttu-id="43d17-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="43d17-116">Inquire</span></span>
- <span data-ttu-id="43d17-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="43d17-117">SilentlyContinue</span></span>
- <span data-ttu-id="43d17-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="43d17-118">Stop</span></span>
- <span data-ttu-id="43d17-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="43d17-119">Suspend</span></span>

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

### <span data-ttu-id="43d17-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="43d17-120">-InformationVariable</span></span>
<span data-ttu-id="43d17-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="43d17-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="43d17-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="43d17-122">-IPAddress</span></span>
<span data-ttu-id="43d17-123">Указывает IP-адрес DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="43d17-123">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="43d17-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="43d17-124">-Name</span></span>
<span data-ttu-id="43d17-125">Задает понятное имя для DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="43d17-125">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="43d17-126">Это имя не обязательно является полным доменным именем.</span><span class="sxs-lookup"><span data-stu-id="43d17-126">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="43d17-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="43d17-127">-Profile</span></span>
<span data-ttu-id="43d17-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="43d17-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="43d17-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="43d17-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="43d17-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="43d17-130">-ServiceName</span></span>
<span data-ttu-id="43d17-131">Указывает имя службы, к которой этот командлет добавляет DNS-сервер.</span><span class="sxs-lookup"><span data-stu-id="43d17-131">Specifies the name of the service to which this cmdlet adds the DNS server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d17-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d17-132">CommonParameters</span></span>
<span data-ttu-id="43d17-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43d17-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d17-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43d17-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d17-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43d17-135">INPUTS</span></span>

## <span data-ttu-id="43d17-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43d17-136">OUTPUTS</span></span>

### <span data-ttu-id="43d17-137">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="43d17-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="43d17-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="43d17-138">NOTES</span></span>

## <span data-ttu-id="43d17-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43d17-139">RELATED LINKS</span></span>

[<span data-ttu-id="43d17-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="43d17-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="43d17-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="43d17-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="43d17-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="43d17-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="43d17-143">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="43d17-143">Set-AzureDns</span></span>](./Set-AzureDns.md)


