---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1F76C63E-5289-4F88-9522-3FF4EF732908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a232ec03da38ea3d527dcd9aa214dbf681bcc6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075898"
---
# <span data-ttu-id="ff852-101">New-AzureServiceDiagnosticsExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="ff852-101">New-AzureServiceDiagnosticsExtensionConfig</span></span>

## <span data-ttu-id="ff852-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff852-102">SYNOPSIS</span></span>
<span data-ttu-id="ff852-103">Создает конфигурацию для расширения диагностики для указанных ролей или всех ролей.</span><span class="sxs-lookup"><span data-stu-id="ff852-103">Generates a configuration for a diagnostics extension for specified role(s) or all roles.</span></span>

## <span data-ttu-id="ff852-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff852-104">SYNTAX</span></span>

### <span data-ttu-id="ff852-105">NewExtension (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff852-105">NewExtension (Default)</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ff852-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="ff852-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>]
 [[-StorageContext] <AzureStorageContext>] [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff852-107">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="ff852-107">SetExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ff852-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff852-108">DESCRIPTION</span></span>
<span data-ttu-id="ff852-109">Командлет **New-AzureServiceDiagnosticsExtensionConfig** создает конфигурацию для расширения диагностики для указанных ролей или всех ролей.</span><span class="sxs-lookup"><span data-stu-id="ff852-109">The **New-AzureServiceDiagnosticsExtensionConfig** cmdlet generates a configuration for a diagnostics extension for specified roles or all roles.</span></span>

## <span data-ttu-id="ff852-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff852-110">EXAMPLES</span></span>

### <span data-ttu-id="ff852-111">Пример 1: создание расширения диагностики Azure для всех ролей в облачной службе</span><span class="sxs-lookup"><span data-stu-id="ff852-111">Example 1: Create the Azure Diagnostics extension for all roles in the cloud service</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="ff852-112">Эта команда создает расширение диагностики Azure для всех ролей в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="ff852-112">This command creates the Azure Diagnostics extension for all of the roles in the cloud service.</span></span>

### <span data-ttu-id="ff852-113">Пример 2: создание расширения диагностики Azure для роли</span><span class="sxs-lookup"><span data-stu-id="ff852-113">Example 2: Create the Azure Diagnostics extension for a role</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole1"
```

<span data-ttu-id="ff852-114">Эта команда создает расширение диагностики Azure для роли WebRole01 в облачной службе.</span><span class="sxs-lookup"><span data-stu-id="ff852-114">This command creates the Azure Diagnostics extension for the role WebRole01 in the cloud service.</span></span>

## <span data-ttu-id="ff852-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff852-115">PARAMETERS</span></span>

### <span data-ttu-id="ff852-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ff852-116">-CertificateThumbprint</span></span>
<span data-ttu-id="ff852-117">Указывает отпечаток сертификата, который будет использоваться для шифрования частной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ff852-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="ff852-118">Этот сертификат уже должен существовать в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="ff852-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="ff852-119">Если вы не указали сертификат, этот командлет создаст сертификат.</span><span class="sxs-lookup"><span data-stu-id="ff852-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="ff852-120">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="ff852-120">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="ff852-121">Указывает путь конфигурации диагностики.</span><span class="sxs-lookup"><span data-stu-id="ff852-121">Specifies the diagnostics configuration path.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff852-122">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="ff852-122">-ExtensionId</span></span>
<span data-ttu-id="ff852-123">Указывает код расширения.</span><span class="sxs-lookup"><span data-stu-id="ff852-123">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff852-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ff852-124">-InformationAction</span></span>
<span data-ttu-id="ff852-125">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="ff852-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ff852-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ff852-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ff852-127">Продолжал</span><span class="sxs-lookup"><span data-stu-id="ff852-127">Continue</span></span>
- <span data-ttu-id="ff852-128">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="ff852-128">Ignore</span></span>
- <span data-ttu-id="ff852-129">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="ff852-129">Inquire</span></span>
- <span data-ttu-id="ff852-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ff852-130">SilentlyContinue</span></span>
- <span data-ttu-id="ff852-131">Остановить</span><span class="sxs-lookup"><span data-stu-id="ff852-131">Stop</span></span>
- <span data-ttu-id="ff852-132">Рвать</span><span class="sxs-lookup"><span data-stu-id="ff852-132">Suspend</span></span>

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

### <span data-ttu-id="ff852-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ff852-133">-InformationVariable</span></span>
<span data-ttu-id="ff852-134">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="ff852-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ff852-135">-Profile</span><span class="sxs-lookup"><span data-stu-id="ff852-135">-Profile</span></span>
<span data-ttu-id="ff852-136">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ff852-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff852-137">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ff852-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff852-138">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="ff852-138">-Role</span></span>
<span data-ttu-id="ff852-139">Задает необязательный массив ролей, для которого нужно указать конфигурацию диагностики.</span><span class="sxs-lookup"><span data-stu-id="ff852-139">Specifies an optional array of roles to specify the diagnostics configuration for.</span></span>
<span data-ttu-id="ff852-140">Если не указано, конфигурация диагностики применяется в качестве конфигурации по умолчанию для всех ролей.</span><span class="sxs-lookup"><span data-stu-id="ff852-140">If not specified the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff852-141">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff852-141">-StorageAccountEndpoint</span></span>
<span data-ttu-id="ff852-142">Указывает конечную точку учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ff852-142">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff852-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ff852-143">-StorageAccountKey</span></span>
<span data-ttu-id="ff852-144">Указывает ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ff852-144">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff852-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ff852-145">-StorageAccountName</span></span>
<span data-ttu-id="ff852-146">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ff852-146">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff852-147">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ff852-147">-StorageContext</span></span>
<span data-ttu-id="ff852-148">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="ff852-148">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff852-149">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ff852-149">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="ff852-150">Указывает алгоритм хэширования отпечатков, который используется с отпечатком для идентификации сертификата.</span><span class="sxs-lookup"><span data-stu-id="ff852-150">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="ff852-151">Этот параметр является необязательным и значение по умолчанию — SHA1.</span><span class="sxs-lookup"><span data-stu-id="ff852-151">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff852-152">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="ff852-152">-X509Certificate</span></span>
<span data-ttu-id="ff852-153">Указывает сертификат X. 509, который автоматически отправляется в облачную службу и используется для шифрования закрытой конфигурации расширения.</span><span class="sxs-lookup"><span data-stu-id="ff852-153">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="ff852-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff852-154">CommonParameters</span></span>
<span data-ttu-id="ff852-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff852-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff852-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff852-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff852-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff852-157">INPUTS</span></span>

## <span data-ttu-id="ff852-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff852-158">OUTPUTS</span></span>

## <span data-ttu-id="ff852-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff852-159">NOTES</span></span>

## <span data-ttu-id="ff852-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff852-160">RELATED LINKS</span></span>

[<span data-ttu-id="ff852-161">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ff852-161">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="ff852-162">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="ff852-162">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


