---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1B1C1459-A602-423D-8CAA-B4901CFC2C82
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f684908e8119da007f8b1f844ebbac40713d51
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076479"
---
# <span data-ttu-id="e52ac-101">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e52ac-101">Remove-AzureDns</span></span>

## <span data-ttu-id="e52ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e52ac-102">SYNOPSIS</span></span>
<span data-ttu-id="e52ac-103">Удаляет DNS-сервер из службы Azure.</span><span class="sxs-lookup"><span data-stu-id="e52ac-103">Removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="e52ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e52ac-104">SYNTAX</span></span>

```
Remove-AzureDns [-Name] <String> [-ServiceName] <String> [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e52ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e52ac-105">DESCRIPTION</span></span>
<span data-ttu-id="e52ac-106">Командлет **Remove-AzureDns** удаляет DNS-сервер из службы Azure.</span><span class="sxs-lookup"><span data-stu-id="e52ac-106">The **Remove-AzureDns** cmdlet removes a DNS server from an Azure service.</span></span>

## <span data-ttu-id="e52ac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e52ac-107">EXAMPLES</span></span>

### <span data-ttu-id="e52ac-108">Пример 1: Удаление DNS-сервера из службы</span><span class="sxs-lookup"><span data-stu-id="e52ac-108">Example 1: Remove a DNS server from a service</span></span>
```
PS C:\> Remove-AzureDns -ServiceName "ContosoService" -Name "Dns07"
```

<span data-ttu-id="e52ac-109">Эта команда удаляет DNS-сервер с именем Dns07 из ContosoService.</span><span class="sxs-lookup"><span data-stu-id="e52ac-109">This command removes the DNS server named Dns07 from ContosoService.</span></span>

## <span data-ttu-id="e52ac-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e52ac-110">PARAMETERS</span></span>

### <span data-ttu-id="e52ac-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e52ac-111">-Force</span></span>
<span data-ttu-id="e52ac-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e52ac-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e52ac-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e52ac-113">-InformationAction</span></span>
<span data-ttu-id="e52ac-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="e52ac-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e52ac-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e52ac-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e52ac-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="e52ac-116">Continue</span></span>
- <span data-ttu-id="e52ac-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="e52ac-117">Ignore</span></span>
- <span data-ttu-id="e52ac-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="e52ac-118">Inquire</span></span>
- <span data-ttu-id="e52ac-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e52ac-119">SilentlyContinue</span></span>
- <span data-ttu-id="e52ac-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="e52ac-120">Stop</span></span>
- <span data-ttu-id="e52ac-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="e52ac-121">Suspend</span></span>

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

### <span data-ttu-id="e52ac-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e52ac-122">-InformationVariable</span></span>
<span data-ttu-id="e52ac-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="e52ac-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e52ac-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e52ac-124">-Name</span></span>
<span data-ttu-id="e52ac-125">Указывает имя DNS-сервера, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e52ac-125">Specifies the name of the DNS server that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e52ac-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="e52ac-126">-Profile</span></span>
<span data-ttu-id="e52ac-127">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e52ac-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e52ac-128">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e52ac-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e52ac-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e52ac-129">-ServiceName</span></span>
<span data-ttu-id="e52ac-130">Указывает имя службы, из которой этот командлет удаляет DNS-сервер.</span><span class="sxs-lookup"><span data-stu-id="e52ac-130">Specifies the name of the service from which this cmdlet removes a DNS server.</span></span>

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

### <span data-ttu-id="e52ac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e52ac-131">CommonParameters</span></span>
<span data-ttu-id="e52ac-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e52ac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e52ac-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e52ac-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e52ac-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e52ac-134">INPUTS</span></span>

## <span data-ttu-id="e52ac-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e52ac-135">OUTPUTS</span></span>

### <span data-ttu-id="e52ac-136">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="e52ac-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="e52ac-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="e52ac-137">NOTES</span></span>

## <span data-ttu-id="e52ac-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e52ac-138">RELATED LINKS</span></span>

[<span data-ttu-id="e52ac-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e52ac-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="e52ac-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e52ac-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="e52ac-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e52ac-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="e52ac-142">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e52ac-142">Set-AzureDns</span></span>](./Set-AzureDns.md)


