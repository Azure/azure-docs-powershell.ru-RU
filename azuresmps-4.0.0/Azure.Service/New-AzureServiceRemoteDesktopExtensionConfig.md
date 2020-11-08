---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2563898E-C4A0-4530-AB46-30A6FC1BE55C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d295e2198cdbd8168d76b1f8e19e75fb4a662116
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075895"
---
# <span data-ttu-id="f2b83-101">New-AzureServiceRemoteDesktopExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="f2b83-101">New-AzureServiceRemoteDesktopExtensionConfig</span></span>

## <span data-ttu-id="f2b83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2b83-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b83-103">Генерирует конфигурацию расширений удаленных рабочих столов для развертывания.</span><span class="sxs-lookup"><span data-stu-id="f2b83-103">Generates a remote desktop extension configuration for a deployment.</span></span>

## <span data-ttu-id="f2b83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2b83-104">SYNTAX</span></span>

### <span data-ttu-id="f2b83-105">NewExtension (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f2b83-105">NewExtension (Default)</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f2b83-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="f2b83-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f2b83-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2b83-107">DESCRIPTION</span></span>
<span data-ttu-id="f2b83-108">Командлет **New-AzureServiceRemoteDesktopExtensionConfig** создает конфигурацию для расширения удаленных рабочих столов для развертывания.</span><span class="sxs-lookup"><span data-stu-id="f2b83-108">The **New-AzureServiceRemoteDesktopExtensionConfig** cmdlet generates a configuration for a remote desktop extension for a deployment.</span></span>

## <span data-ttu-id="f2b83-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2b83-109">EXAMPLES</span></span>

### <span data-ttu-id="f2b83-110">Пример 1: создание конфигурации расширения для удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="f2b83-110">Example 1: Generate a remote desktop extension configuration</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred
```

<span data-ttu-id="f2b83-111">Эта команда генерирует конфигурацию расширения удаленных рабочих столов для указанных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="f2b83-111">This command generates a remote desktop extension configuration for the specified credentials.</span></span>

### <span data-ttu-id="f2b83-112">Пример 2: создание конфигурации расширения удаленных рабочих столов для указанной роли</span><span class="sxs-lookup"><span data-stu-id="f2b83-112">Example 2: Generate a remote desktop extension configuration for a specified role</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred -Role "WebRole01"
```

<span data-ttu-id="f2b83-113">Эта команда генерирует расширение конфигурации удаленного рабочего стола для указанных учетных данных и роль WebRole01.</span><span class="sxs-lookup"><span data-stu-id="f2b83-113">This command generates a remote desktop extension configuration for the specified credentials and the WebRole01 role.</span></span>

## <span data-ttu-id="f2b83-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2b83-114">PARAMETERS</span></span>

### <span data-ttu-id="f2b83-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f2b83-115">-CertificateThumbprint</span></span>
<span data-ttu-id="f2b83-116">Указывает отпечаток сертификата, который будет использоваться для шифрования частной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f2b83-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="f2b83-117">Этот сертификат уже должен существовать в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="f2b83-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="f2b83-118">Если вы не указали сертификат, этот командлет создаст сертификат.</span><span class="sxs-lookup"><span data-stu-id="f2b83-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b83-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="f2b83-119">-Credential</span></span>
<span data-ttu-id="f2b83-120">Указывает учетные данные, которые нужно включить для удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="f2b83-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="f2b83-121">Учетные данные включают имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="f2b83-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b83-122">-Срок действия</span><span class="sxs-lookup"><span data-stu-id="f2b83-122">-Expiration</span></span>
<span data-ttu-id="f2b83-123">Указывает объект **DateTime** , который позволяет пользователю указать, когда истечет срок действия учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="f2b83-123">Specifies a **DateTime** object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b83-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="f2b83-124">-ExtensionId</span></span>
<span data-ttu-id="f2b83-125">Указывает код расширения.</span><span class="sxs-lookup"><span data-stu-id="f2b83-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b83-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f2b83-126">-InformationAction</span></span>
<span data-ttu-id="f2b83-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="f2b83-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f2b83-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f2b83-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2b83-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="f2b83-129">Continue</span></span>
- <span data-ttu-id="f2b83-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="f2b83-130">Ignore</span></span>
- <span data-ttu-id="f2b83-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="f2b83-131">Inquire</span></span>
- <span data-ttu-id="f2b83-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f2b83-132">SilentlyContinue</span></span>
- <span data-ttu-id="f2b83-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="f2b83-133">Stop</span></span>
- <span data-ttu-id="f2b83-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="f2b83-134">Suspend</span></span>

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

### <span data-ttu-id="f2b83-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f2b83-135">-InformationVariable</span></span>
<span data-ttu-id="f2b83-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="f2b83-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f2b83-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="f2b83-137">-Profile</span></span>
<span data-ttu-id="f2b83-138">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f2b83-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2b83-139">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f2b83-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2b83-140">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="f2b83-140">-Role</span></span>
<span data-ttu-id="f2b83-141">Задает необязательный массив ролей, для которого нужно задать конфигурацию удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f2b83-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="f2b83-142">Если этот параметр не указан, в качестве конфигурации по умолчанию для всех ролей применяется конфигурация удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="f2b83-142">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b83-143">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="f2b83-143">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="f2b83-144">Указывает алгоритм хэширования отпечатков, который используется с отпечатком для идентификации сертификата.</span><span class="sxs-lookup"><span data-stu-id="f2b83-144">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="f2b83-145">Этот параметр является необязательным и значение по умолчанию — SHA1.</span><span class="sxs-lookup"><span data-stu-id="f2b83-145">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b83-146">-Version</span><span class="sxs-lookup"><span data-stu-id="f2b83-146">-Version</span></span>
<span data-ttu-id="f2b83-147">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="f2b83-147">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b83-148">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="f2b83-148">-X509Certificate</span></span>
<span data-ttu-id="f2b83-149">Указывает сертификат x509, который при указании будет автоматически передан в облачную службу и использоваться для шифрования закрытой конфигурации расширения.</span><span class="sxs-lookup"><span data-stu-id="f2b83-149">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: NewExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b83-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b83-150">CommonParameters</span></span>
<span data-ttu-id="f2b83-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2b83-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b83-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b83-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b83-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2b83-153">INPUTS</span></span>

## <span data-ttu-id="f2b83-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2b83-154">OUTPUTS</span></span>

## <span data-ttu-id="f2b83-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2b83-155">NOTES</span></span>

## <span data-ttu-id="f2b83-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2b83-156">RELATED LINKS</span></span>

[<span data-ttu-id="f2b83-157">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="f2b83-157">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


