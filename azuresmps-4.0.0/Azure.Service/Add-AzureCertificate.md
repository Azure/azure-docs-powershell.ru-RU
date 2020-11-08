---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9A6D5C40-2532-4FD1-A74F-16725CAD8EDD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29d049dbdce93102411a875cfaef8e5fb9c719b6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076395"
---
# <span data-ttu-id="d0796-101">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="d0796-101">Add-AzureCertificate</span></span>

## <span data-ttu-id="d0796-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0796-102">SYNOPSIS</span></span>
<span data-ttu-id="d0796-103">Отправляет сертификат в облачную службу Azure.</span><span class="sxs-lookup"><span data-stu-id="d0796-103">Uploads a certificate to an Azure cloud service.</span></span>

## <span data-ttu-id="d0796-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0796-104">SYNTAX</span></span>

```
Add-AzureCertificate [-ServiceName] <String> [-CertToDeploy] <Object> [-Password <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0796-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0796-105">DESCRIPTION</span></span>
<span data-ttu-id="d0796-106">Командлет **Add-AzureCertificate** отправляет сертификат для службы Azure.</span><span class="sxs-lookup"><span data-stu-id="d0796-106">The **Add-AzureCertificate** cmdlet uploads a certificate for an Azure service.</span></span>

## <span data-ttu-id="d0796-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0796-107">EXAMPLES</span></span>

### <span data-ttu-id="d0796-108">Пример 1: отправка сертификата и пароля</span><span class="sxs-lookup"><span data-stu-id="d0796-108">Example 1: Upload a certificate and password</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy ContosoCertificate.pfx -Password "password"
```

<span data-ttu-id="d0796-109">Эта команда передает файл сертификата ContosoCertificate. pfx в облачную службу.</span><span class="sxs-lookup"><span data-stu-id="d0796-109">This command uploads the certificate file ContosoCertificate.pfx to a cloud service.</span></span>
<span data-ttu-id="d0796-110">Команда задает пароль для сертификата.</span><span class="sxs-lookup"><span data-stu-id="d0796-110">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="d0796-111">Пример 2: Отправка файла сертификата</span><span class="sxs-lookup"><span data-stu-id="d0796-111">Example 2: Upload a certificate file</span></span>
```
PS C:\> Add-AzureCertificate -serviceName "MyService" -CertToDeploy ContosoCertificate.cer
```

<span data-ttu-id="d0796-112">Эта команда передает файл сертификата ContosoCertificate. cer в облачную службу.</span><span class="sxs-lookup"><span data-stu-id="d0796-112">This command uploads the certificate file ContosoCertificate.cer to a cloud service.</span></span>
<span data-ttu-id="d0796-113">Команда задает пароль для сертификата.</span><span class="sxs-lookup"><span data-stu-id="d0796-113">The command specifies the password for the certificate.</span></span>

### <span data-ttu-id="d0796-114">Пример 3: Отправка объекта сертификата</span><span class="sxs-lookup"><span data-stu-id="d0796-114">Example 3: Upload a certificate object</span></span>
```
PS C:\> $Certificate = Get-Item cert:\PATTIFULLER\MY\1D6E34B526723E06C235BE8E5457784BF12C9F39
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy $Certificate
```

<span data-ttu-id="d0796-115">Первая команда получает сертификат из хранилища "мой магазин" пользователя с помощью базового командлета **Get-Item** Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d0796-115">The first command gets a certificate from the MY store of a user by using the Windows PowerShell core **Get-Item** cmdlet.</span></span>
<span data-ttu-id="d0796-116">Эта команда хранит сертификат в переменной $Certificate.</span><span class="sxs-lookup"><span data-stu-id="d0796-116">The command stores the certificate in the $Certificate variable.</span></span>

<span data-ttu-id="d0796-117">Вторая команда отправляет сертификат в $certificate облачной службе.</span><span class="sxs-lookup"><span data-stu-id="d0796-117">The second command uploads the certificate in $certificate to a cloud service.</span></span>

## <span data-ttu-id="d0796-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0796-118">PARAMETERS</span></span>

### <span data-ttu-id="d0796-119">-CertToDeploy</span><span class="sxs-lookup"><span data-stu-id="d0796-119">-CertToDeploy</span></span>
<span data-ttu-id="d0796-120">Указывает сертификат для развертывания.</span><span class="sxs-lookup"><span data-stu-id="d0796-120">Specifies the certificate to deploy.</span></span>
<span data-ttu-id="d0796-121">Вы можете указать полный путь к файлу сертификата, например файл с расширением. cer или \*.</span><span class="sxs-lookup"><span data-stu-id="d0796-121">You can specify the full path of a certificate file, such as a file that has a \*.cer or \*.</span></span>
<span data-ttu-id="d0796-122">расширение имени PFX-файла или объект сертификата X. 509.</span><span class="sxs-lookup"><span data-stu-id="d0796-122">pfx file name extension, or an X.509 Certificate object.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0796-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d0796-123">-InformationAction</span></span>
<span data-ttu-id="d0796-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="d0796-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d0796-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d0796-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d0796-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="d0796-126">Continue</span></span>
- <span data-ttu-id="d0796-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="d0796-127">Ignore</span></span>
- <span data-ttu-id="d0796-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="d0796-128">Inquire</span></span>
- <span data-ttu-id="d0796-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d0796-129">SilentlyContinue</span></span>
- <span data-ttu-id="d0796-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="d0796-130">Stop</span></span>
- <span data-ttu-id="d0796-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="d0796-131">Suspend</span></span>

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

### <span data-ttu-id="d0796-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d0796-132">-InformationVariable</span></span>
<span data-ttu-id="d0796-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="d0796-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d0796-134">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="d0796-134">-Password</span></span>
<span data-ttu-id="d0796-135">Указывает пароль сертификата.</span><span class="sxs-lookup"><span data-stu-id="d0796-135">Specifies the certificate password.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0796-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="d0796-136">-Profile</span></span>
<span data-ttu-id="d0796-137">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d0796-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d0796-138">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d0796-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d0796-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d0796-139">-ServiceName</span></span>
<span data-ttu-id="d0796-140">Указывает имя службы Azure, к которой этот командлет добавляет сертификат.</span><span class="sxs-lookup"><span data-stu-id="d0796-140">Specifies the name of the Azure service to which this cmdlet adds a certificate.</span></span>

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

### <span data-ttu-id="d0796-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0796-141">CommonParameters</span></span>
<span data-ttu-id="d0796-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0796-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0796-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0796-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0796-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0796-144">INPUTS</span></span>

## <span data-ttu-id="d0796-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0796-145">OUTPUTS</span></span>

### <span data-ttu-id="d0796-146">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="d0796-146">ManagementOperationContext</span></span>

## <span data-ttu-id="d0796-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0796-147">NOTES</span></span>

## <span data-ttu-id="d0796-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0796-148">RELATED LINKS</span></span>

[<span data-ttu-id="d0796-149">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="d0796-149">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="d0796-150">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="d0796-150">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="d0796-151">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="d0796-151">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


