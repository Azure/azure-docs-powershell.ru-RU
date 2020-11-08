---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BC16303-CCB4-40D8-ABCB-59CF0D85ED63
online version: ''
schema: 2.0.0
ms.openlocfilehash: f24f5d8f7f72c59847cfa5dde51a1937bc304735
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076069"
---
# <span data-ttu-id="25dd0-101">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="25dd0-101">Set-AzureDns</span></span>

## <span data-ttu-id="25dd0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="25dd0-103">Изменение IP-адреса DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="25dd0-103">Modifies the IP address of a DNS server.</span></span>

## <span data-ttu-id="25dd0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25dd0-104">SYNTAX</span></span>

```
Set-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="25dd0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25dd0-105">DESCRIPTION</span></span>
<span data-ttu-id="25dd0-106">Командлет **Set-AzureDns** изменяет IP-адрес DNS-сервера для службы Azure.</span><span class="sxs-lookup"><span data-stu-id="25dd0-106">The **Set-AzureDns** cmdlet modifies the IP address of a DNS server for an Azure service.</span></span>

## <span data-ttu-id="25dd0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25dd0-107">EXAMPLES</span></span>

### <span data-ttu-id="25dd0-108">Пример 1: изменение IP-адреса DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="25dd0-108">Example 1: Modify the IP address of a DNS server</span></span>
```
PS C:\> Set-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.5 -Name "Dns07"
```

<span data-ttu-id="25dd0-109">Эта команда изменяет IP-адрес DNS-сервера с именем Dns07 для службы с именем ContosoService.</span><span class="sxs-lookup"><span data-stu-id="25dd0-109">This command modifies the IP address of the DNS server named Dns07 for the service named ContosoService.</span></span>

## <span data-ttu-id="25dd0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25dd0-110">PARAMETERS</span></span>

### <span data-ttu-id="25dd0-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="25dd0-111">-InformationAction</span></span>
<span data-ttu-id="25dd0-112">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="25dd0-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="25dd0-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="25dd0-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="25dd0-114">Продолжал</span><span class="sxs-lookup"><span data-stu-id="25dd0-114">Continue</span></span>
- <span data-ttu-id="25dd0-115">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="25dd0-115">Ignore</span></span>
- <span data-ttu-id="25dd0-116">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="25dd0-116">Inquire</span></span>
- <span data-ttu-id="25dd0-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="25dd0-117">SilentlyContinue</span></span>
- <span data-ttu-id="25dd0-118">Остановить</span><span class="sxs-lookup"><span data-stu-id="25dd0-118">Stop</span></span>
- <span data-ttu-id="25dd0-119">Рвать</span><span class="sxs-lookup"><span data-stu-id="25dd0-119">Suspend</span></span>

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

### <span data-ttu-id="25dd0-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="25dd0-120">-InformationVariable</span></span>
<span data-ttu-id="25dd0-121">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="25dd0-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="25dd0-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="25dd0-122">-IPAddress</span></span>
<span data-ttu-id="25dd0-123">Указывает новый IP-адрес DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="25dd0-123">Specifies the new IP address of the DNS server.</span></span>

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

### <span data-ttu-id="25dd0-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="25dd0-124">-Name</span></span>
<span data-ttu-id="25dd0-125">Указывает имя DNS-сервера, который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="25dd0-125">Specifies the name of the DNS server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="25dd0-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="25dd0-126">-Profile</span></span>
<span data-ttu-id="25dd0-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="25dd0-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="25dd0-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="25dd0-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="25dd0-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="25dd0-129">-ServiceName</span></span>
<span data-ttu-id="25dd0-130">Указывает имя службы, для которой этот командлет изменяет адрес DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="25dd0-130">Specifies the name of the service for which this cmdlet modifies the address of the DNS server.</span></span>

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

### <span data-ttu-id="25dd0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25dd0-131">CommonParameters</span></span>
<span data-ttu-id="25dd0-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25dd0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25dd0-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25dd0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25dd0-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25dd0-134">INPUTS</span></span>

## <span data-ttu-id="25dd0-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25dd0-135">OUTPUTS</span></span>

### <span data-ttu-id="25dd0-136">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="25dd0-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="25dd0-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="25dd0-137">NOTES</span></span>

## <span data-ttu-id="25dd0-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25dd0-138">RELATED LINKS</span></span>

[<span data-ttu-id="25dd0-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="25dd0-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="25dd0-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="25dd0-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="25dd0-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="25dd0-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="25dd0-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="25dd0-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)


