---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2E738CEF-BBDD-425D-B12C-86FF7C45A634
online version: ''
schema: 2.0.0
ms.openlocfilehash: 518528d4af8889cf36b30c417e0170e0ea228ebf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076047"
---
# <span data-ttu-id="27ae6-101">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="27ae6-101">Set-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="27ae6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27ae6-102">SYNOPSIS</span></span>
<span data-ttu-id="27ae6-103">Включает расширение диагностики Azure на указанных ролях или всех ролях в развернутой службе или в развертывании.</span><span class="sxs-lookup"><span data-stu-id="27ae6-103">Enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="27ae6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27ae6-104">SYNTAX</span></span>

### <span data-ttu-id="27ae6-105">SetExtension (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27ae6-105">SetExtension (Default)</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="27ae6-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="27ae6-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-CertificateThumbprint] <String>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="27ae6-107">SetExtensionUsingDiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ae6-107">SetExtensionUsingDiagnosticsConfiguration</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-DiagnosticsConfiguration] <ExtensionConfigurationInput[]> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="27ae6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27ae6-108">DESCRIPTION</span></span>
<span data-ttu-id="27ae6-109">Командлет **Set-AzureServiceDiagnosticsExtension** включает расширение диагностики Azure на указанных ролях или всех ролях в развернутой службе или в развертывании.</span><span class="sxs-lookup"><span data-stu-id="27ae6-109">The **Set-AzureServiceDiagnosticsExtension** cmdlet enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="27ae6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27ae6-110">EXAMPLES</span></span>

### <span data-ttu-id="27ae6-111">Пример 1: Включение расширения диагностики Azure</span><span class="sxs-lookup"><span data-stu-id="27ae6-111">Example 1: Enable Azure Diagnostics extension</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="27ae6-112">Эта команда включает расширение диагностики Azure для всех ролей.</span><span class="sxs-lookup"><span data-stu-id="27ae6-112">This command enables the Azure Diagnostics extension for all roles.</span></span>

### <span data-ttu-id="27ae6-113">Пример 2: Включение расширения диагностики Azure для указанной роли</span><span class="sxs-lookup"><span data-stu-id="27ae6-113">Example 2: Enable Azure Diagnostics extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole01"
```

<span data-ttu-id="27ae6-114">Эта команда включает расширение диагностики Azure для указанной роли.</span><span class="sxs-lookup"><span data-stu-id="27ae6-114">This command enables the Azure Diagnostics extension for a specified role.</span></span>

## <span data-ttu-id="27ae6-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27ae6-115">PARAMETERS</span></span>

### <span data-ttu-id="27ae6-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="27ae6-116">-CertificateThumbprint</span></span>
<span data-ttu-id="27ae6-117">Указывает отпечаток сертификата, который будет использоваться для шифрования частной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="27ae6-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="27ae6-118">Этот сертификат уже должен существовать в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="27ae6-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="27ae6-119">Если вы не указали сертификат, этот командлет создаст сертификат.</span><span class="sxs-lookup"><span data-stu-id="27ae6-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ae6-120">-DiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="27ae6-120">-DiagnosticsConfiguration</span></span>
<span data-ttu-id="27ae6-121">Задает массив конфигураций для диагностики Azure.</span><span class="sxs-lookup"><span data-stu-id="27ae6-121">Specifies an array of configuration for Azure Diagnostics.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: SetExtensionUsingDiagnosticsConfiguration
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ae6-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="27ae6-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="27ae6-123">Указывает конфигурацию для диагностики Azure.</span><span class="sxs-lookup"><span data-stu-id="27ae6-123">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="27ae6-124">Вы можете загрузить схему, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="27ae6-124">You can download the schema by using the following command:</span></span> 

`(Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'`

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ae6-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="27ae6-125">-ExtensionId</span></span>
<span data-ttu-id="27ae6-126">Указывает код расширения</span><span class="sxs-lookup"><span data-stu-id="27ae6-126">Specifies the extension ID</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ae6-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="27ae6-127">-InformationAction</span></span>
<span data-ttu-id="27ae6-128">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="27ae6-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="27ae6-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="27ae6-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="27ae6-130">Продолжал</span><span class="sxs-lookup"><span data-stu-id="27ae6-130">Continue</span></span>
- <span data-ttu-id="27ae6-131">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="27ae6-131">Ignore</span></span>
- <span data-ttu-id="27ae6-132">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="27ae6-132">Inquire</span></span>
- <span data-ttu-id="27ae6-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="27ae6-133">SilentlyContinue</span></span>
- <span data-ttu-id="27ae6-134">Остановить</span><span class="sxs-lookup"><span data-stu-id="27ae6-134">Stop</span></span>
- <span data-ttu-id="27ae6-135">Рвать</span><span class="sxs-lookup"><span data-stu-id="27ae6-135">Suspend</span></span>

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

### <span data-ttu-id="27ae6-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="27ae6-136">-InformationVariable</span></span>
<span data-ttu-id="27ae6-137">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="27ae6-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="27ae6-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="27ae6-138">-Profile</span></span>
<span data-ttu-id="27ae6-139">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="27ae6-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="27ae6-140">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="27ae6-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="27ae6-141">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="27ae6-141">-Role</span></span>
<span data-ttu-id="27ae6-142">Задает необязательный массив ролей, для которого нужно задать конфигурацию диагностики Azure.</span><span class="sxs-lookup"><span data-stu-id="27ae6-142">Specifies an optional array of roles for which to specify the Azure Diagnostics configuration.</span></span>
<span data-ttu-id="27ae6-143">Если этот параметр не указан, конфигурация диагностики применяется как конфигурация по умолчанию для всех ролей.</span><span class="sxs-lookup"><span data-stu-id="27ae6-143">If you do not specify this parameter, the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ae6-144">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="27ae6-144">-ServiceName</span></span>
<span data-ttu-id="27ae6-145">Указывает имя службы Azure для развертывания.</span><span class="sxs-lookup"><span data-stu-id="27ae6-145">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="27ae6-146">-Slot</span><span class="sxs-lookup"><span data-stu-id="27ae6-146">-Slot</span></span>
<span data-ttu-id="27ae6-147">Задает среду развертывания, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="27ae6-147">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="27ae6-148">Допустимые значения этого параметра: "производственный" или "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="27ae6-148">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="27ae6-149">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="27ae6-149">-StorageAccountEndpoint</span></span>
<span data-ttu-id="27ae6-150">Указывает конечную точку учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="27ae6-150">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ae6-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="27ae6-151">-StorageAccountKey</span></span>
<span data-ttu-id="27ae6-152">Указывает ключ учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="27ae6-152">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ae6-153">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="27ae6-153">-StorageAccountName</span></span>
<span data-ttu-id="27ae6-154">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="27ae6-154">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ae6-155">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="27ae6-155">-StorageContext</span></span>
<span data-ttu-id="27ae6-156">Указывает контекст хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="27ae6-156">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ae6-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="27ae6-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="27ae6-158">Указывает алгоритм хэширования отпечатка, который используется с отпечатком для идентификации сертификата.</span><span class="sxs-lookup"><span data-stu-id="27ae6-158">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="27ae6-159">Этот параметр является необязательным и значение по умолчанию — SHA1.</span><span class="sxs-lookup"><span data-stu-id="27ae6-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ae6-160">-Version</span><span class="sxs-lookup"><span data-stu-id="27ae6-160">-Version</span></span>
<span data-ttu-id="27ae6-161">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="27ae6-161">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ae6-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="27ae6-162">-X509Certificate</span></span>
<span data-ttu-id="27ae6-163">Задает сертификат X. 509, который, при указании, автоматически отправляется в облачную службу и используется для шифрования закрытой конфигурации расширения.</span><span class="sxs-lookup"><span data-stu-id="27ae6-163">Specifies an X.509 certificate that, when specified, is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="27ae6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ae6-164">CommonParameters</span></span>
<span data-ttu-id="27ae6-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27ae6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ae6-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27ae6-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ae6-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27ae6-167">INPUTS</span></span>

## <span data-ttu-id="27ae6-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27ae6-168">OUTPUTS</span></span>

## <span data-ttu-id="27ae6-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="27ae6-169">NOTES</span></span>

## <span data-ttu-id="27ae6-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27ae6-170">RELATED LINKS</span></span>

[<span data-ttu-id="27ae6-171">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="27ae6-171">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="27ae6-172">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="27ae6-172">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)


