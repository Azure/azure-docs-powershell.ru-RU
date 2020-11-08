---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7BEFA810-685C-4553-BED8-4CD6BCF8A5FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: d88784e5d4fdd153700bd3879262198e5dd3807a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076356"
---
# <span data-ttu-id="a8d3c-101">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="a8d3c-101">Get-AzureCertificate</span></span>

## <span data-ttu-id="a8d3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d3c-103">Получает объект сертификата из службы Azure.</span><span class="sxs-lookup"><span data-stu-id="a8d3c-103">Gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="a8d3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8d3c-104">SYNTAX</span></span>

```
Get-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm <String>] [-Thumbprint <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8d3c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8d3c-105">DESCRIPTION</span></span>
<span data-ttu-id="a8d3c-106">Командлет **Get-AzureCertificate** получает объект сертификата из службы Azure.</span><span class="sxs-lookup"><span data-stu-id="a8d3c-106">The **Get-AzureCertificate** cmdlet gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="a8d3c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8d3c-107">EXAMPLES</span></span>

### <span data-ttu-id="a8d3c-108">Пример 1: получение сертификатов из службы</span><span class="sxs-lookup"><span data-stu-id="a8d3c-108">Example 1: Get certificates from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService"
```

<span data-ttu-id="a8d3c-109">Эта команда получает объекты сертификата из службы с именем ContosoService и сохраняет их в переменной $AzureCert.</span><span class="sxs-lookup"><span data-stu-id="a8d3c-109">This command gets certificate objects from the service named ContosoService, and then stores them in the $AzureCert variable.</span></span>

### <span data-ttu-id="a8d3c-110">Пример 2: получение сертификата из службы</span><span class="sxs-lookup"><span data-stu-id="a8d3c-110">Example 2: Get a certificate from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="a8d3c-111">Эта команда получает объект сертификата, определенный указанным отпечатком из службы с именем ContosoService, и сохраняет его в переменной $AzureCert.</span><span class="sxs-lookup"><span data-stu-id="a8d3c-111">This command gets the certificate object identified by the specified thumbprint from the service named ContosoService, and then stores it in the $AzureCert variable.</span></span>

## <span data-ttu-id="a8d3c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8d3c-112">PARAMETERS</span></span>

### <span data-ttu-id="a8d3c-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a8d3c-113">-InformationAction</span></span>
<span data-ttu-id="a8d3c-114">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a8d3c-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a8d3c-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a8d3c-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a8d3c-116">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a8d3c-116">Continue</span></span>
- <span data-ttu-id="a8d3c-117">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a8d3c-117">Ignore</span></span>
- <span data-ttu-id="a8d3c-118">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a8d3c-118">Inquire</span></span>
- <span data-ttu-id="a8d3c-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a8d3c-119">SilentlyContinue</span></span>
- <span data-ttu-id="a8d3c-120">Остановить</span><span class="sxs-lookup"><span data-stu-id="a8d3c-120">Stop</span></span>
- <span data-ttu-id="a8d3c-121">Рвать</span><span class="sxs-lookup"><span data-stu-id="a8d3c-121">Suspend</span></span>

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

### <span data-ttu-id="a8d3c-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a8d3c-122">-InformationVariable</span></span>
<span data-ttu-id="a8d3c-123">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a8d3c-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a8d3c-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="a8d3c-124">-Profile</span></span>
<span data-ttu-id="a8d3c-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a8d3c-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8d3c-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8d3c-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a8d3c-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a8d3c-127">-ServiceName</span></span>
<span data-ttu-id="a8d3c-128">Указывает имя службы Azure, от которой этот командлет получает сертификат.</span><span class="sxs-lookup"><span data-stu-id="a8d3c-128">Specifies the name of the Azure service from which this cmdlet gets a certificate.</span></span>

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

### <span data-ttu-id="a8d3c-129">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="a8d3c-129">-Thumbprint</span></span>
<span data-ttu-id="a8d3c-130">Указывает отпечаток сертификата, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a8d3c-130">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8d3c-131">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="a8d3c-131">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="a8d3c-132">Указывает алгоритм, который используется для создания отпечатка сертификата.</span><span class="sxs-lookup"><span data-stu-id="a8d3c-132">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8d3c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d3c-133">CommonParameters</span></span>
<span data-ttu-id="a8d3c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8d3c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d3c-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8d3c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d3c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8d3c-136">INPUTS</span></span>

## <span data-ttu-id="a8d3c-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8d3c-137">OUTPUTS</span></span>

### <span data-ttu-id="a8d3c-138">CertificateContext</span><span class="sxs-lookup"><span data-stu-id="a8d3c-138">CertificateContext</span></span>

## <span data-ttu-id="a8d3c-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8d3c-139">NOTES</span></span>

## <span data-ttu-id="a8d3c-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8d3c-140">RELATED LINKS</span></span>

[<span data-ttu-id="a8d3c-141">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="a8d3c-141">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="a8d3c-142">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="a8d3c-142">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="a8d3c-143">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="a8d3c-143">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


