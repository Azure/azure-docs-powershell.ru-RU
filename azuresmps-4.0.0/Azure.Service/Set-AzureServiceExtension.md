---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D37920D3-AF6C-4CFC-B9A3-8ED931AEC0DC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 318683c26d05c624549363ff1afe4a2b963c1fe6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075447"
---
# <span data-ttu-id="e91a3-101">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="e91a3-101">Set-AzureServiceExtension</span></span>

## <span data-ttu-id="e91a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e91a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e91a3-103">Добавляет расширение облачной службы в развертывание.</span><span class="sxs-lookup"><span data-stu-id="e91a3-103">Adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="e91a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e91a3-104">SYNTAX</span></span>

### <span data-ttu-id="e91a3-105">SetExtension (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e91a3-105">SetExtension (Default)</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e91a3-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="e91a3-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e91a3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e91a3-107">DESCRIPTION</span></span>
<span data-ttu-id="e91a3-108">Командлет **Set-AzureServiceExtension** добавляет расширение облачной службы в развертывание.</span><span class="sxs-lookup"><span data-stu-id="e91a3-108">The **Set-AzureServiceExtension** cmdlet adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="e91a3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e91a3-109">EXAMPLES</span></span>

### <span data-ttu-id="e91a3-110">Пример 1: Добавление облачной службы в развертывание</span><span class="sxs-lookup"><span data-stu-id="e91a3-110">Example 1: Add a cloud service to a deployment</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -ExtensionName "RDP" -Version "1.0" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="e91a3-111">Эта команда добавляет облачную службу в развертывание.</span><span class="sxs-lookup"><span data-stu-id="e91a3-111">This command adds a cloud service to a deployment.</span></span>

### <span data-ttu-id="e91a3-112">Пример 2: Добавление облачной службы в развертывание для указанной роли</span><span class="sxs-lookup"><span data-stu-id="e91a3-112">Example 2: Add a cloud service to a deployment for a specified role</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -Role "WebRole1" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="e91a3-113">Эта команда добавляет облачную службу в развертывание для указанной роли.</span><span class="sxs-lookup"><span data-stu-id="e91a3-113">This command adds a cloud service to a deployment for a specified role.</span></span>

## <span data-ttu-id="e91a3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e91a3-114">PARAMETERS</span></span>

### <span data-ttu-id="e91a3-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="e91a3-115">-CertificateThumbprint</span></span>
<span data-ttu-id="e91a3-116">Указывает отпечаток сертификата, который будет использоваться для шифрования частной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e91a3-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="e91a3-117">Этот сертификат уже должен существовать в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="e91a3-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="e91a3-118">Если вы не указали сертификат, этот командлет создаст сертификат.</span><span class="sxs-lookup"><span data-stu-id="e91a3-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="e91a3-119">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="e91a3-119">-ExtensionId</span></span>
<span data-ttu-id="e91a3-120">Указывает код расширения.</span><span class="sxs-lookup"><span data-stu-id="e91a3-120">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91a3-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="e91a3-121">-ExtensionName</span></span>
<span data-ttu-id="e91a3-122">Задает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="e91a3-122">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91a3-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e91a3-123">-InformationAction</span></span>
<span data-ttu-id="e91a3-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="e91a3-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e91a3-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="e91a3-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e91a3-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="e91a3-126">Continue</span></span>
- <span data-ttu-id="e91a3-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="e91a3-127">Ignore</span></span>
- <span data-ttu-id="e91a3-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="e91a3-128">Inquire</span></span>
- <span data-ttu-id="e91a3-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e91a3-129">SilentlyContinue</span></span>
- <span data-ttu-id="e91a3-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="e91a3-130">Stop</span></span>
- <span data-ttu-id="e91a3-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="e91a3-131">Suspend</span></span>

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

### <span data-ttu-id="e91a3-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e91a3-132">-InformationVariable</span></span>
<span data-ttu-id="e91a3-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="e91a3-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e91a3-134">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e91a3-134">-PrivateConfiguration</span></span>
<span data-ttu-id="e91a3-135">Указывает частный текст конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e91a3-135">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91a3-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="e91a3-136">-Profile</span></span>
<span data-ttu-id="e91a3-137">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e91a3-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e91a3-138">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e91a3-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e91a3-139">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e91a3-139">-ProviderNamespace</span></span>
<span data-ttu-id="e91a3-140">Задает пространство имен поставщика расширений.</span><span class="sxs-lookup"><span data-stu-id="e91a3-140">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91a3-141">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="e91a3-141">-PublicConfiguration</span></span>
<span data-ttu-id="e91a3-142">Указывает общедоступный текст конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e91a3-142">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91a3-143">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="e91a3-143">-Role</span></span>
<span data-ttu-id="e91a3-144">Задает необязательный массив ролей, для которого нужно задать конфигурацию удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e91a3-144">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="e91a3-145">Если этот параметр не указан, в качестве конфигурации по умолчанию для всех ролей применяется конфигурация удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e91a3-145">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="e91a3-146">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e91a3-146">-ServiceName</span></span>
<span data-ttu-id="e91a3-147">Указывает имя службы Azure для развертывания.</span><span class="sxs-lookup"><span data-stu-id="e91a3-147">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="e91a3-148">-Slot</span><span class="sxs-lookup"><span data-stu-id="e91a3-148">-Slot</span></span>
<span data-ttu-id="e91a3-149">Задает среду развертывания, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="e91a3-149">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="e91a3-150">Допустимые значения: Production или промежуточный.</span><span class="sxs-lookup"><span data-stu-id="e91a3-150">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="e91a3-151">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e91a3-151">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="e91a3-152">Указывает алгоритм хэширования отпечатков, который используется с отпечатком для идентификации сертификата.</span><span class="sxs-lookup"><span data-stu-id="e91a3-152">Specifies the thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="e91a3-153">Этот параметр является необязательным и значение по умолчанию — SHA1.</span><span class="sxs-lookup"><span data-stu-id="e91a3-153">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="e91a3-154">-Version</span><span class="sxs-lookup"><span data-stu-id="e91a3-154">-Version</span></span>
<span data-ttu-id="e91a3-155">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="e91a3-155">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e91a3-156">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="e91a3-156">-X509Certificate</span></span>
<span data-ttu-id="e91a3-157">Указывает сертификат X. 509, который автоматически отправляется в облачную службу и используется для шифрования закрытой конфигурации расширения.</span><span class="sxs-lookup"><span data-stu-id="e91a3-157">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="e91a3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91a3-158">CommonParameters</span></span>
<span data-ttu-id="e91a3-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e91a3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91a3-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e91a3-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91a3-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e91a3-161">INPUTS</span></span>

## <span data-ttu-id="e91a3-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e91a3-162">OUTPUTS</span></span>

## <span data-ttu-id="e91a3-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="e91a3-163">NOTES</span></span>

## <span data-ttu-id="e91a3-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e91a3-164">RELATED LINKS</span></span>

[<span data-ttu-id="e91a3-165">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="e91a3-165">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="e91a3-166">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="e91a3-166">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)


