---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 350638E1-636E-484B-88EB-91F48129D80B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c665288d12897e4ab7277dd4ccf4bc5d975c037
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076048"
---
# <span data-ttu-id="191ce-101">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="191ce-101">Set-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="191ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="191ce-102">SYNOPSIS</span></span>
<span data-ttu-id="191ce-103">Включает расширение доменных имен AD для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="191ce-103">Enables an AD Domain extension for a cloud service.</span></span>

## <span data-ttu-id="191ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="191ce-104">SYNTAX</span></span>

### <span data-ttu-id="191ce-105">JoinDomainUsingEnumOptions (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="191ce-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="191ce-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="191ce-106">JoinDomainUsingJoinOption</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="191ce-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="191ce-107">WorkGroupName</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="191ce-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="191ce-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>]
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="191ce-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="191ce-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32>
 [[-OUPath] <String>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="191ce-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="191ce-110">WorkGroupNameThumbprint</span></span>
```
Set-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart]
 [[-Credential] <PSCredential>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="191ce-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="191ce-111">DESCRIPTION</span></span>
<span data-ttu-id="191ce-112">Командлет **Set-AzureServiceADDomainExtension** включает расширение домена AD (Active Directory) для облачной службы.</span><span class="sxs-lookup"><span data-stu-id="191ce-112">The **Set-AzureServiceADDomainExtension** cmdlet enables an AD (Active Directory) Domain extension for a cloud service.</span></span>

## <span data-ttu-id="191ce-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="191ce-113">EXAMPLES</span></span>

### <span data-ttu-id="191ce-114">1:</span><span class="sxs-lookup"><span data-stu-id="191ce-114">1:</span></span>
```

```

## <span data-ttu-id="191ce-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="191ce-115">PARAMETERS</span></span>

### <span data-ttu-id="191ce-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="191ce-116">-CertificateThumbprint</span></span>
<span data-ttu-id="191ce-117">Указывает отпечаток сертификата, который будет использоваться для шифрования частной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="191ce-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="191ce-118">Этот сертификат уже должен существовать в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="191ce-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="191ce-119">Если вы не указали сертификат, этот командлет создаст сертификат.</span><span class="sxs-lookup"><span data-stu-id="191ce-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191ce-120">-Credential</span><span class="sxs-lookup"><span data-stu-id="191ce-120">-Credential</span></span>
<span data-ttu-id="191ce-121">Указывает учетные данные для присоединения к домену доменных данных.</span><span class="sxs-lookup"><span data-stu-id="191ce-121">Specifies the credentials to join the AD domain.</span></span>
<span data-ttu-id="191ce-122">Учетные данные включают имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="191ce-122">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191ce-123">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="191ce-123">-DomainName</span></span>
<span data-ttu-id="191ce-124">Указывает имя домена доменных имен.</span><span class="sxs-lookup"><span data-stu-id="191ce-124">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191ce-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="191ce-125">-ExtensionId</span></span>
<span data-ttu-id="191ce-126">Указывает код расширения.</span><span class="sxs-lookup"><span data-stu-id="191ce-126">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191ce-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="191ce-127">-InformationAction</span></span>
<span data-ttu-id="191ce-128">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="191ce-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="191ce-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="191ce-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="191ce-130">Продолжал</span><span class="sxs-lookup"><span data-stu-id="191ce-130">Continue</span></span>
- <span data-ttu-id="191ce-131">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="191ce-131">Ignore</span></span>
- <span data-ttu-id="191ce-132">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="191ce-132">Inquire</span></span>
- <span data-ttu-id="191ce-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="191ce-133">SilentlyContinue</span></span>
- <span data-ttu-id="191ce-134">Остановить</span><span class="sxs-lookup"><span data-stu-id="191ce-134">Stop</span></span>
- <span data-ttu-id="191ce-135">Рвать</span><span class="sxs-lookup"><span data-stu-id="191ce-135">Suspend</span></span>

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

### <span data-ttu-id="191ce-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="191ce-136">-InformationVariable</span></span>
<span data-ttu-id="191ce-137">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="191ce-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="191ce-138">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="191ce-138">-JoinOption</span></span>
<span data-ttu-id="191ce-139">Задает перечисление параметров соединения.</span><span class="sxs-lookup"><span data-stu-id="191ce-139">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191ce-140">-Параметры</span><span class="sxs-lookup"><span data-stu-id="191ce-140">-Options</span></span>
<span data-ttu-id="191ce-141">Указывает параметр соединения "целое число без знака".</span><span class="sxs-lookup"><span data-stu-id="191ce-141">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191ce-142">-OUPath</span><span class="sxs-lookup"><span data-stu-id="191ce-142">-OUPath</span></span>
<span data-ttu-id="191ce-143">Задает путь к организационному подразделению (OU) для операции присоединения к домену AD.</span><span class="sxs-lookup"><span data-stu-id="191ce-143">Specifies the Organization Unit (OU) path for the AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191ce-144">-Profile</span><span class="sxs-lookup"><span data-stu-id="191ce-144">-Profile</span></span>
<span data-ttu-id="191ce-145">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="191ce-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="191ce-146">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="191ce-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="191ce-147">-Restart</span><span class="sxs-lookup"><span data-stu-id="191ce-147">-Restart</span></span>
<span data-ttu-id="191ce-148">Указывает, следует ли перезагружать компьютер при успешном выполнении операции присоединения.</span><span class="sxs-lookup"><span data-stu-id="191ce-148">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191ce-149">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="191ce-149">-Role</span></span>
<span data-ttu-id="191ce-150">Задает необязательный массив ролей, для которого нужно задать конфигурацию удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="191ce-150">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="191ce-151">Если не указано, Конфигурация домена AD применяется как конфигурация по умолчанию для всех ролей.</span><span class="sxs-lookup"><span data-stu-id="191ce-151">If not specified the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="191ce-152">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="191ce-152">-ServiceName</span></span>
<span data-ttu-id="191ce-153">Указывает имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="191ce-153">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="191ce-154">-Slot</span><span class="sxs-lookup"><span data-stu-id="191ce-154">-Slot</span></span>
<span data-ttu-id="191ce-155">Задает среду развертывания, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="191ce-155">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="191ce-156">Допустимые значения этого параметра: "производственный" или "промежуточный".</span><span class="sxs-lookup"><span data-stu-id="191ce-156">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="191ce-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="191ce-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="191ce-158">Указывает алгоритм хэширования отпечатков, который используется с отпечатком для идентификации сертификата.</span><span class="sxs-lookup"><span data-stu-id="191ce-158">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="191ce-159">Этот параметр является необязательным и значение по умолчанию — SHA1.</span><span class="sxs-lookup"><span data-stu-id="191ce-159">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="191ce-160">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="191ce-160">-UnjoinDomainCredential</span></span>
<span data-ttu-id="191ce-161">Задает учетные данные (имя пользователя и пароль) для отсоединения домена доменных имен.</span><span class="sxs-lookup"><span data-stu-id="191ce-161">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191ce-162">-Version</span><span class="sxs-lookup"><span data-stu-id="191ce-162">-Version</span></span>
<span data-ttu-id="191ce-163">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="191ce-163">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191ce-164">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="191ce-164">-WorkgroupName</span></span>
<span data-ttu-id="191ce-165">Указывает имя рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="191ce-165">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191ce-166">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="191ce-166">-X509Certificate</span></span>
<span data-ttu-id="191ce-167">Указывает сертификат x509, который при указании будет автоматически передан в облачную службу и использоваться для шифрования закрытой конфигурации расширения.</span><span class="sxs-lookup"><span data-stu-id="191ce-167">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="191ce-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="191ce-168">CommonParameters</span></span>
<span data-ttu-id="191ce-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="191ce-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="191ce-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="191ce-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="191ce-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="191ce-171">INPUTS</span></span>

## <span data-ttu-id="191ce-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="191ce-172">OUTPUTS</span></span>

## <span data-ttu-id="191ce-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="191ce-173">NOTES</span></span>

## <span data-ttu-id="191ce-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="191ce-174">RELATED LINKS</span></span>

[<span data-ttu-id="191ce-175">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="191ce-175">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="191ce-176">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="191ce-176">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="191ce-177">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="191ce-177">New-AzureServiceADDomainExtensionConfig</span></span>](./New-AzureServiceADDomainExtensionConfig.md)


