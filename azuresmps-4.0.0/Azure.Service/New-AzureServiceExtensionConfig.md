---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E27283AF-4057-48D9-9F08-7D36290DD907
online version: ''
schema: 2.0.0
ms.openlocfilehash: dfe55fb2ced2275eae06e96480249acd99d3ad6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075896"
---
# <span data-ttu-id="d638f-101">New-AzureServiceExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="d638f-101">New-AzureServiceExtensionConfig</span></span>

## <span data-ttu-id="d638f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d638f-102">SYNOPSIS</span></span>
<span data-ttu-id="d638f-103">Создает конфигурацию расширения облачной службы для развертывания.</span><span class="sxs-lookup"><span data-stu-id="d638f-103">Creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="d638f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d638f-104">SYNTAX</span></span>

### <span data-ttu-id="d638f-105">NewExtension (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d638f-105">NewExtension (Default)</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d638f-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="d638f-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d638f-107">UpdateExtensionStatusParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d638f-107">UpdateExtensionStatusParameterSetName</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-ExtensionId] <String> [-ExtensionState] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d638f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d638f-108">DESCRIPTION</span></span>
<span data-ttu-id="d638f-109">Командлет **New-AzureServiceExtensionConfig** создает конфигурацию расширения облачной службы для развертывания.</span><span class="sxs-lookup"><span data-stu-id="d638f-109">The **New-AzureServiceExtensionConfig** cmdlet creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="d638f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d638f-110">EXAMPLES</span></span>

### <span data-ttu-id="d638f-111">Пример 1: создание конфигурации расширения</span><span class="sxs-lookup"><span data-stu-id="d638f-111">Example 1: Create an extension configuration</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -ExtensionName 'RDP' -Version '1.0' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="d638f-112">Эта команда задает конфигурацию расширения.</span><span class="sxs-lookup"><span data-stu-id="d638f-112">This command specifies an extension configuration.</span></span>

### <span data-ttu-id="d638f-113">Пример 2: создание конфигурации расширения для роли</span><span class="sxs-lookup"><span data-stu-id="d638f-113">Example 2: Create an extension configuration for a role</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -Role WebRole1 -ExtensionName 'RDP' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="d638f-114">Эта команда задает конфигурацию расширения для роли WebRole1.</span><span class="sxs-lookup"><span data-stu-id="d638f-114">This command specifies an extension configuration for the role WebRole1.</span></span>

## <span data-ttu-id="d638f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d638f-115">PARAMETERS</span></span>

### <span data-ttu-id="d638f-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="d638f-116">-CertificateThumbprint</span></span>
<span data-ttu-id="d638f-117">Указывает отпечаток сертификата, который будет использоваться для шифрования частной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d638f-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="d638f-118">Этот сертификат уже должен существовать в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d638f-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="d638f-119">Если вы не указали сертификат, этот командлет создаст сертификат.</span><span class="sxs-lookup"><span data-stu-id="d638f-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="d638f-120">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="d638f-120">-ExtensionId</span></span>
<span data-ttu-id="d638f-121">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="d638f-121">Specifies the name of the extension.</span></span>

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

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d638f-122">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="d638f-122">-ExtensionName</span></span>
<span data-ttu-id="d638f-123">Указывает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="d638f-123">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d638f-124">-ExtensionState</span><span class="sxs-lookup"><span data-stu-id="d638f-124">-ExtensionState</span></span>
<span data-ttu-id="d638f-125">Задает состояние расширения.</span><span class="sxs-lookup"><span data-stu-id="d638f-125">Specifies the state of the extension.</span></span>
<span data-ttu-id="d638f-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d638f-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d638f-127">Включите</span><span class="sxs-lookup"><span data-stu-id="d638f-127">Enable</span></span> 
- <span data-ttu-id="d638f-128">Ключив</span><span class="sxs-lookup"><span data-stu-id="d638f-128">Disable</span></span> 
- <span data-ttu-id="d638f-129">Отмен</span><span class="sxs-lookup"><span data-stu-id="d638f-129">Uninstall</span></span>

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d638f-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d638f-130">-InformationAction</span></span>
<span data-ttu-id="d638f-131">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="d638f-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d638f-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d638f-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d638f-133">Продолжал</span><span class="sxs-lookup"><span data-stu-id="d638f-133">Continue</span></span>
- <span data-ttu-id="d638f-134">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="d638f-134">Ignore</span></span>
- <span data-ttu-id="d638f-135">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="d638f-135">Inquire</span></span>
- <span data-ttu-id="d638f-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d638f-136">SilentlyContinue</span></span>
- <span data-ttu-id="d638f-137">Остановить</span><span class="sxs-lookup"><span data-stu-id="d638f-137">Stop</span></span>
- <span data-ttu-id="d638f-138">Рвать</span><span class="sxs-lookup"><span data-stu-id="d638f-138">Suspend</span></span>

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

### <span data-ttu-id="d638f-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d638f-139">-InformationVariable</span></span>
<span data-ttu-id="d638f-140">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="d638f-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d638f-141">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d638f-141">-PrivateConfiguration</span></span>
<span data-ttu-id="d638f-142">Указывает частный текст конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d638f-142">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d638f-143">-Profile</span><span class="sxs-lookup"><span data-stu-id="d638f-143">-Profile</span></span>
<span data-ttu-id="d638f-144">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d638f-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d638f-145">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d638f-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d638f-146">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d638f-146">-ProviderNamespace</span></span>
<span data-ttu-id="d638f-147">Задает пространство имен поставщика расширения.</span><span class="sxs-lookup"><span data-stu-id="d638f-147">Specifies the Extension's Provider Namespace.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d638f-148">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="d638f-148">-PublicConfiguration</span></span>
<span data-ttu-id="d638f-149">Указывает общедоступный текст конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d638f-149">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d638f-150">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="d638f-150">-Role</span></span>
<span data-ttu-id="d638f-151">Задает необязательный массив ролей, для которого нужно указать конфигурацию удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="d638f-151">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="d638f-152">Если не указана конфигурация удаленных рабочих столов, она будет использоваться по умолчанию для всех ролей.</span><span class="sxs-lookup"><span data-stu-id="d638f-152">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="d638f-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="d638f-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="d638f-154">Указывает алгоритм хэширования отпечатков, который используется с отпечатком для идентификации сертификата.</span><span class="sxs-lookup"><span data-stu-id="d638f-154">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="d638f-155">Этот параметр является необязательным и значение по умолчанию — SHA1.</span><span class="sxs-lookup"><span data-stu-id="d638f-155">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="d638f-156">-Version</span><span class="sxs-lookup"><span data-stu-id="d638f-156">-Version</span></span>
<span data-ttu-id="d638f-157">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="d638f-157">Specifies the extension version.</span></span>

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

### <span data-ttu-id="d638f-158">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="d638f-158">-X509Certificate</span></span>
<span data-ttu-id="d638f-159">Указывает сертификат x509, который при указании будет автоматически передан в облачную службу и использоваться для шифрования закрытой конфигурации расширения.</span><span class="sxs-lookup"><span data-stu-id="d638f-159">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="d638f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d638f-160">CommonParameters</span></span>
<span data-ttu-id="d638f-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d638f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d638f-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d638f-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d638f-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d638f-163">INPUTS</span></span>

## <span data-ttu-id="d638f-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d638f-164">OUTPUTS</span></span>

## <span data-ttu-id="d638f-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="d638f-165">NOTES</span></span>

## <span data-ttu-id="d638f-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d638f-166">RELATED LINKS</span></span>

[<span data-ttu-id="d638f-167">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="d638f-167">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="d638f-168">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="d638f-168">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


