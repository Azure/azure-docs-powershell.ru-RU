---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076167"
---
# <span data-ttu-id="88bcd-101">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="88bcd-101">Remove-AzureCertificate</span></span>

## <span data-ttu-id="88bcd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="88bcd-103">Удаление сертификата из службы Azure.</span><span class="sxs-lookup"><span data-stu-id="88bcd-103">Removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="88bcd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88bcd-104">SYNTAX</span></span>

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="88bcd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88bcd-105">DESCRIPTION</span></span>
<span data-ttu-id="88bcd-106">Командлет **Remove-AzureCertificate** Удаляет сертификат из службы Azure.</span><span class="sxs-lookup"><span data-stu-id="88bcd-106">The **Remove-AzureCertificate** cmdlet removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="88bcd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88bcd-107">EXAMPLES</span></span>

### <span data-ttu-id="88bcd-108">Пример 1: Удаление сертификата из службы</span><span class="sxs-lookup"><span data-stu-id="88bcd-108">Example 1: Remove a certificate from a service</span></span>
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="88bcd-109">Эта команда удаляет объект сертификата с указанным отпечатком из облачной службы.</span><span class="sxs-lookup"><span data-stu-id="88bcd-109">This command removes the certificate object that has the specified thumbprint from the cloud service.</span></span>

### <span data-ttu-id="88bcd-110">Пример 2: удаление всех сертификатов из службы</span><span class="sxs-lookup"><span data-stu-id="88bcd-110">Example 2: Remove all certificates from a service</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

<span data-ttu-id="88bcd-111">Эта команда получает все сертификаты из службы с именем ContosoService с помощью командлета **Get-AzureCertificate** .</span><span class="sxs-lookup"><span data-stu-id="88bcd-111">This command gets all the certificates from the service named ContosoService by using the **Get-AzureCertificate** cmdlet.</span></span>
<span data-ttu-id="88bcd-112">Команда передает каждый сертификат текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="88bcd-112">The command passes each certificate to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="88bcd-113">Этот командлет удаляет все сертификаты из облачной службы.</span><span class="sxs-lookup"><span data-stu-id="88bcd-113">That cmdlet removes each certificate from the cloud service.</span></span>

### <span data-ttu-id="88bcd-114">Пример 3: удаление всех сертификатов из службы, использующей определенный алгоритм отпечатка</span><span class="sxs-lookup"><span data-stu-id="88bcd-114">Example 3: Remove all certificates from a service that use a specific thumbprint algorithm</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

<span data-ttu-id="88bcd-115">Эта команда получает все сертификаты из службы с именем ContosoService, которые используют алгоритм отпечатка SHA1.</span><span class="sxs-lookup"><span data-stu-id="88bcd-115">This command gets all the certificates from the service named ContosoService that use the sha1 thumbprint algorithm.</span></span>
<span data-ttu-id="88bcd-116">Команда передает каждый сертификат в текущий командлет, удаляющий каждый из сертификатов.</span><span class="sxs-lookup"><span data-stu-id="88bcd-116">The command passes each certificate to the current cmdlet, which removes each certificate.</span></span>

## <span data-ttu-id="88bcd-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88bcd-117">PARAMETERS</span></span>

### <span data-ttu-id="88bcd-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="88bcd-118">-InformationAction</span></span>
<span data-ttu-id="88bcd-119">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="88bcd-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="88bcd-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="88bcd-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="88bcd-121">Продолжал</span><span class="sxs-lookup"><span data-stu-id="88bcd-121">Continue</span></span>
- <span data-ttu-id="88bcd-122">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="88bcd-122">Ignore</span></span>
- <span data-ttu-id="88bcd-123">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="88bcd-123">Inquire</span></span>
- <span data-ttu-id="88bcd-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="88bcd-124">SilentlyContinue</span></span>
- <span data-ttu-id="88bcd-125">Остановить</span><span class="sxs-lookup"><span data-stu-id="88bcd-125">Stop</span></span>
- <span data-ttu-id="88bcd-126">Рвать</span><span class="sxs-lookup"><span data-stu-id="88bcd-126">Suspend</span></span>

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

### <span data-ttu-id="88bcd-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="88bcd-127">-InformationVariable</span></span>
<span data-ttu-id="88bcd-128">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="88bcd-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="88bcd-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="88bcd-129">-Profile</span></span>
<span data-ttu-id="88bcd-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="88bcd-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="88bcd-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="88bcd-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="88bcd-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="88bcd-132">-ServiceName</span></span>
<span data-ttu-id="88bcd-133">Указывает имя службы Azure, из которой этот командлет удаляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="88bcd-133">Specifies the name of the Azure service from which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="88bcd-134">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="88bcd-134">-Thumbprint</span></span>
<span data-ttu-id="88bcd-135">Указывает отпечаток сертификата, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="88bcd-135">Specifies the thumbprint of the certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="88bcd-136">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="88bcd-136">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="88bcd-137">Указывает алгоритм, который используется для создания отпечатка сертификата.</span><span class="sxs-lookup"><span data-stu-id="88bcd-137">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88bcd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88bcd-138">CommonParameters</span></span>
<span data-ttu-id="88bcd-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88bcd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88bcd-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88bcd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88bcd-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88bcd-141">INPUTS</span></span>

## <span data-ttu-id="88bcd-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88bcd-142">OUTPUTS</span></span>

### <span data-ttu-id="88bcd-143">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="88bcd-143">ManagementOperationContext</span></span>

## <span data-ttu-id="88bcd-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="88bcd-144">NOTES</span></span>

## <span data-ttu-id="88bcd-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88bcd-145">RELATED LINKS</span></span>

[<span data-ttu-id="88bcd-146">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="88bcd-146">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="88bcd-147">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="88bcd-147">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="88bcd-148">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="88bcd-148">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)


