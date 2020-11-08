---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5C8B1482-80B0-4060-A35D-E9D394156886
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a6303e685ea02408772a237c6b5f154764107e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075813"
---
# <span data-ttu-id="6b8c7-101">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="6b8c7-101">Set-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="6b8c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8c7-103">Включает расширение удаленного рабочего стола на указанных ролях или всех ролях в развернутой службе или в развертывании.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-103">Enables remote desktop extension on specified role(s) or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="6b8c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b8c7-104">SYNTAX</span></span>

### <span data-ttu-id="6b8c7-105">SetExtension (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b8c7-105">SetExtension (Default)</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6b8c7-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="6b8c7-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6b8c7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b8c7-107">DESCRIPTION</span></span>
<span data-ttu-id="6b8c7-108">Командлет **Set-AzureServiceRemoteDesktopExtension** включает расширение удаленного рабочего стола на указанных ролях или всех ролях в развернутой службе или в развертывании.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-108">The **Set-AzureServiceRemoteDesktopExtension** cmdlet enables remote desktop extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="6b8c7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b8c7-109">EXAMPLES</span></span>

### <span data-ttu-id="6b8c7-110">Пример 1: Включение расширения удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="6b8c7-110">Example 1: Enable remote desktop extension</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds
```

<span data-ttu-id="6b8c7-111">Эта команда включает расширение удаленного рабочего стола для указанной службы.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-111">This command enables the remote desktop extension for the specified service.</span></span>

### <span data-ttu-id="6b8c7-112">Пример 2: Включение расширения удаленного рабочего стола для указанной роли</span><span class="sxs-lookup"><span data-stu-id="6b8c7-112">Example 2: Enable remote desktop extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds -Role "WebRole1"
```

<span data-ttu-id="6b8c7-113">Эта команда включает расширение удаленного рабочего стола для указанной службы и роли.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-113">This command enables the remote desktop extension for the specified service and role.</span></span>

## <span data-ttu-id="6b8c7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b8c7-114">PARAMETERS</span></span>

### <span data-ttu-id="6b8c7-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="6b8c7-115">-CertificateThumbprint</span></span>
<span data-ttu-id="6b8c7-116">Указывает отпечаток сертификата, который будет использоваться для шифрования частной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="6b8c7-117">Этот сертификат уже должен существовать в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="6b8c7-118">Если вы не указали сертификат, этот командлет создаст сертификат.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8c7-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="6b8c7-119">-Credential</span></span>
<span data-ttu-id="6b8c7-120">Указывает учетные данные, которые нужно включить для удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="6b8c7-121">Учетные данные включают имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8c7-122">-Срок действия</span><span class="sxs-lookup"><span data-stu-id="6b8c7-122">-Expiration</span></span>
<span data-ttu-id="6b8c7-123">Указывает объект даты и времени, который позволяет пользователю указать, когда истечет срок действия учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-123">Specifies a date time object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8c7-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="6b8c7-124">-ExtensionId</span></span>
<span data-ttu-id="6b8c7-125">Указывает код расширения.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8c7-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6b8c7-126">-InformationAction</span></span>
<span data-ttu-id="6b8c7-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6b8c7-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6b8c7-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b8c7-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="6b8c7-129">Continue</span></span>
- <span data-ttu-id="6b8c7-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="6b8c7-130">Ignore</span></span>
- <span data-ttu-id="6b8c7-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="6b8c7-131">Inquire</span></span>
- <span data-ttu-id="6b8c7-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6b8c7-132">SilentlyContinue</span></span>
- <span data-ttu-id="6b8c7-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="6b8c7-133">Stop</span></span>
- <span data-ttu-id="6b8c7-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="6b8c7-134">Suspend</span></span>

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

### <span data-ttu-id="6b8c7-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6b8c7-135">-InformationVariable</span></span>
<span data-ttu-id="6b8c7-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6b8c7-137">-Profile</span><span class="sxs-lookup"><span data-stu-id="6b8c7-137">-Profile</span></span>
<span data-ttu-id="6b8c7-138">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6b8c7-139">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6b8c7-140">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="6b8c7-140">-Role</span></span>
<span data-ttu-id="6b8c7-141">Задает необязательный массив ролей, для которого нужно задать конфигурацию удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="6b8c7-142">Если этот параметр не указан, в качестве конфигурации по умолчанию для всех ролей применяется конфигурация удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-142">If this parameter is not specified, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8c7-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6b8c7-143">-ServiceName</span></span>
<span data-ttu-id="6b8c7-144">Указывает имя службы Azure для развертывания.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-144">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8c7-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="6b8c7-145">-Slot</span></span>
<span data-ttu-id="6b8c7-146">Задает среду развертывания, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-146">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="6b8c7-147">Допустимые значения этого параметра: "производство", "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="6b8c7-147">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="6b8c7-148">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="6b8c7-148">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="6b8c7-149">Указывает алгоритм хэширования отпечатков, который используется с отпечатком для идентификации сертификата.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-149">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="6b8c7-150">Этот параметр является необязательным и значение по умолчанию — SHA1.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-150">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8c7-151">-Version</span><span class="sxs-lookup"><span data-stu-id="6b8c7-151">-Version</span></span>
<span data-ttu-id="6b8c7-152">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-152">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8c7-153">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="6b8c7-153">-X509Certificate</span></span>
<span data-ttu-id="6b8c7-154">Указывает сертификат x509, который автоматически отправляется в облачную службу и используется для шифрования частной конфигурации расширения.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-154">Specifies an x509 certificate that is automatically uploaded to the cloud service and used for encrypting the private configuration of the extension.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8c7-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8c7-155">CommonParameters</span></span>
<span data-ttu-id="6b8c7-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b8c7-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8c7-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b8c7-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8c7-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b8c7-158">INPUTS</span></span>

## <span data-ttu-id="6b8c7-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b8c7-159">OUTPUTS</span></span>

## <span data-ttu-id="6b8c7-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b8c7-160">NOTES</span></span>

## <span data-ttu-id="6b8c7-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b8c7-161">RELATED LINKS</span></span>

[<span data-ttu-id="6b8c7-162">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="6b8c7-162">Get-AzureServiceRemoteDesktopExtension</span></span>](./Get-AzureServiceRemoteDesktopExtension.md)


