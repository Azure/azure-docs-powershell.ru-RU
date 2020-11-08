---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 184FB33A-C866-4AF0-BA31-8ADCFC6EE8E2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ce5d8511383ad93e288b97381416d7864c3f80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075646"
---
# <span data-ttu-id="426f4-101">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="426f4-101">Get-AzureDns</span></span>

## <span data-ttu-id="426f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="426f4-102">SYNOPSIS</span></span>
<span data-ttu-id="426f4-103">Получает параметры DNS для развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="426f4-103">Gets the DNS settings for an Azure deployment.</span></span>

## <span data-ttu-id="426f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="426f4-104">SYNTAX</span></span>

```
Get-AzureDns [-DnsSettings <DnsSettings>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="426f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="426f4-105">DESCRIPTION</span></span>
<span data-ttu-id="426f4-106">Командлет **Get-AzureDns** получает параметры DNS для развертывания Azure.</span><span class="sxs-lookup"><span data-stu-id="426f4-106">The **Get-AzureDns** cmdlet gets the DNS settings for an Azure deployment.</span></span>
<span data-ttu-id="426f4-107">Командлет возвращает понятное имя и IP-адрес DNS-сервера в объекте параметров DNS.</span><span class="sxs-lookup"><span data-stu-id="426f4-107">The cmdlet returns the friendly name and IP address of the DNS server in a DNS settings object.</span></span>

## <span data-ttu-id="426f4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="426f4-108">EXAMPLES</span></span>

### <span data-ttu-id="426f4-109">Пример 1: получение параметров DNS</span><span class="sxs-lookup"><span data-stu-id="426f4-109">Example 1: Get DNS settings</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Production" | Get-AzureDNS
```

<span data-ttu-id="426f4-110">Эта команда использует командлет **Get-AzureDeployment** для получения рабочего развертывания службы с именем ContosoService.</span><span class="sxs-lookup"><span data-stu-id="426f4-110">This command uses the **Get-AzureDeployment** cmdlet to get the production deployment of the service named ContosoService.</span></span>
<span data-ttu-id="426f4-111">Команда передает этот объект в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="426f4-111">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="426f4-112">Текущий командлет получает параметры DNS.</span><span class="sxs-lookup"><span data-stu-id="426f4-112">The current cmdlet gets the DNS settings.</span></span>

## <span data-ttu-id="426f4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="426f4-113">PARAMETERS</span></span>

### <span data-ttu-id="426f4-114">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="426f4-114">-DnsSettings</span></span>
<span data-ttu-id="426f4-115">Указывает объект **DnsSettings** .</span><span class="sxs-lookup"><span data-stu-id="426f4-115">Specifies a **DnsSettings** object.</span></span>

```yaml
Type: DnsSettings
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="426f4-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="426f4-116">-InformationAction</span></span>
<span data-ttu-id="426f4-117">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="426f4-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="426f4-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="426f4-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="426f4-119">Продолжал</span><span class="sxs-lookup"><span data-stu-id="426f4-119">Continue</span></span>
- <span data-ttu-id="426f4-120">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="426f4-120">Ignore</span></span>
- <span data-ttu-id="426f4-121">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="426f4-121">Inquire</span></span>
- <span data-ttu-id="426f4-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="426f4-122">SilentlyContinue</span></span>
- <span data-ttu-id="426f4-123">Остановить</span><span class="sxs-lookup"><span data-stu-id="426f4-123">Stop</span></span>
- <span data-ttu-id="426f4-124">Рвать</span><span class="sxs-lookup"><span data-stu-id="426f4-124">Suspend</span></span>

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

### <span data-ttu-id="426f4-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="426f4-125">-InformationVariable</span></span>
<span data-ttu-id="426f4-126">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="426f4-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="426f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="426f4-127">CommonParameters</span></span>
<span data-ttu-id="426f4-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="426f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="426f4-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="426f4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="426f4-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="426f4-130">INPUTS</span></span>

## <span data-ttu-id="426f4-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="426f4-131">OUTPUTS</span></span>

## <span data-ttu-id="426f4-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="426f4-132">NOTES</span></span>

## <span data-ttu-id="426f4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="426f4-133">RELATED LINKS</span></span>

[<span data-ttu-id="426f4-134">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="426f4-134">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="426f4-135">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="426f4-135">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="426f4-136">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="426f4-136">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="426f4-137">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="426f4-137">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="426f4-138">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="426f4-138">Set-AzureDns</span></span>](./Set-AzureDns.md)


