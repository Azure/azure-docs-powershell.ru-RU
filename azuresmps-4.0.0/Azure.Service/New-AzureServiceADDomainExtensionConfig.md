---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: DFD4BA63-A7DE-49DD-878C-68062EF17873
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4d4830d049ab01142c75847b4afd5419729f14d1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075897"
---
# <span data-ttu-id="953d6-101">New-AzureServiceADDomainExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="953d6-101">New-AzureServiceADDomainExtensionConfig</span></span>

## <span data-ttu-id="953d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="953d6-102">SYNOPSIS</span></span>
<span data-ttu-id="953d6-103">Создает конфигурацию для расширения доменных имен AD для облачных служб.</span><span class="sxs-lookup"><span data-stu-id="953d6-103">Generates the configuration for the AD domain extension for cloud services.</span></span>

## <span data-ttu-id="953d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="953d6-104">SYNTAX</span></span>

### <span data-ttu-id="953d6-105">JoinDomainUsingEnumOptions (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="953d6-105">JoinDomainUsingEnumOptions (Default)</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="953d6-106">JoinDomainUsingJoinOption</span><span class="sxs-lookup"><span data-stu-id="953d6-106">JoinDomainUsingJoinOption</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="953d6-107">WorkGroupName</span><span class="sxs-lookup"><span data-stu-id="953d6-107">WorkGroupName</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="953d6-108">JoinDomainUsingEnumOptionsAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="953d6-108">JoinDomainUsingEnumOptionsAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [[-Options] <JoinOptions>] [[-OUPath] <String>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="953d6-109">JoinDomainUsingJoinOptionAndThumbprint</span><span class="sxs-lookup"><span data-stu-id="953d6-109">JoinDomainUsingJoinOptionAndThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-DomainName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-UnjoinDomainCredential] <PSCredential>] [-JoinOption] <UInt32> [[-OUPath] <String>] [[-Version] <String>]
 [[-ExtensionId] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="953d6-110">WorkGroupNameThumbprint</span><span class="sxs-lookup"><span data-stu-id="953d6-110">WorkGroupNameThumbprint</span></span>
```
New-AzureServiceADDomainExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-WorkgroupName] <String> [-Restart] [[-Credential] <PSCredential>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="953d6-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="953d6-111">DESCRIPTION</span></span>
<span data-ttu-id="953d6-112">Командлет **New-AzureServiceADDomainExtensionConfig** создает конфигурацию для расширения домена Active Directory (AD) для облачных служб.</span><span class="sxs-lookup"><span data-stu-id="953d6-112">The **New-AzureServiceADDomainExtensionConfig** cmdlet generates the configuration for the Active Directory (AD) domain extension for cloud services.</span></span>

## <span data-ttu-id="953d6-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="953d6-113">EXAMPLES</span></span>

### <span data-ttu-id="953d6-114">Пример 1: указание конфигурации домена доменных служб</span><span class="sxs-lookup"><span data-stu-id="953d6-114">Example 1: Specify an AD domain configuration</span></span>
```
PS C:\> $ExtensionCfg = New-AzureServiceADDomainExtensionConfig -Role WorkerRole1 -DomainName $Domain -Credential $Cred -JoinOption 35;

PS C:\> New-AzureDeployment -ServiceName $CloudSvc -Slot "Production" -Package $Pkg -Configuration $Config -ExtensionConfiguration $ExtensionCfg;
```

<span data-ttu-id="953d6-115">Эта команда создает конфигурацию для расширения доменной рекламы.</span><span class="sxs-lookup"><span data-stu-id="953d6-115">This command generates a configuration for the AD domain extension.</span></span>

## <span data-ttu-id="953d6-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="953d6-116">PARAMETERS</span></span>

### <span data-ttu-id="953d6-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="953d6-117">-CertificateThumbprint</span></span>
<span data-ttu-id="953d6-118">Указывает отпечаток сертификата, который будет использоваться для шифрования частной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="953d6-118">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="953d6-119">Этот сертификат уже должен существовать в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="953d6-119">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="953d6-120">Если вы не указали сертификат, этот командлет создаст сертификат.</span><span class="sxs-lookup"><span data-stu-id="953d6-120">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d6-121">-Credential</span><span class="sxs-lookup"><span data-stu-id="953d6-121">-Credential</span></span>
<span data-ttu-id="953d6-122">Указывает учетные данные, которые следует использовать для присоединения к домену доменных данных.</span><span class="sxs-lookup"><span data-stu-id="953d6-122">Specifies the credentials to use to join the AD domain.</span></span>
<span data-ttu-id="953d6-123">Учетные данные включают имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="953d6-123">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d6-124">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="953d6-124">-DomainName</span></span>
<span data-ttu-id="953d6-125">Указывает имя домена доменных имен.</span><span class="sxs-lookup"><span data-stu-id="953d6-125">Specifies the AD domain name.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d6-126">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="953d6-126">-ExtensionId</span></span>
<span data-ttu-id="953d6-127">Указывает код расширения.</span><span class="sxs-lookup"><span data-stu-id="953d6-127">Specifies the extension ID.</span></span>

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

### <span data-ttu-id="953d6-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="953d6-128">-InformationAction</span></span>
<span data-ttu-id="953d6-129">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="953d6-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="953d6-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="953d6-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="953d6-131">Продолжал</span><span class="sxs-lookup"><span data-stu-id="953d6-131">Continue</span></span>
- <span data-ttu-id="953d6-132">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="953d6-132">Ignore</span></span>
- <span data-ttu-id="953d6-133">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="953d6-133">Inquire</span></span>
- <span data-ttu-id="953d6-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="953d6-134">SilentlyContinue</span></span>
- <span data-ttu-id="953d6-135">Остановить</span><span class="sxs-lookup"><span data-stu-id="953d6-135">Stop</span></span>
- <span data-ttu-id="953d6-136">Рвать</span><span class="sxs-lookup"><span data-stu-id="953d6-136">Suspend</span></span>

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

### <span data-ttu-id="953d6-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="953d6-137">-InformationVariable</span></span>
<span data-ttu-id="953d6-138">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="953d6-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="953d6-139">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="953d6-139">-JoinOption</span></span>
<span data-ttu-id="953d6-140">Задает перечисление параметров соединения.</span><span class="sxs-lookup"><span data-stu-id="953d6-140">Specifies the join option enumeration.</span></span>

```yaml
Type: UInt32
Parameter Sets: JoinDomainUsingJoinOption, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d6-141">-Параметры</span><span class="sxs-lookup"><span data-stu-id="953d6-141">-Options</span></span>
<span data-ttu-id="953d6-142">Указывает параметр соединения "целое число без знака".</span><span class="sxs-lookup"><span data-stu-id="953d6-142">Specifies the unsigned integer join option.</span></span>

```yaml
Type: JoinOptions
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingEnumOptionsAndThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d6-143">-OUPath</span><span class="sxs-lookup"><span data-stu-id="953d6-143">-OUPath</span></span>
<span data-ttu-id="953d6-144">Задает путь к организационному подразделению (OU) для операции присоединения к домену AD.</span><span class="sxs-lookup"><span data-stu-id="953d6-144">Specifies the organization unit (OU) path for AD domain join operation.</span></span>

```yaml
Type: String
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d6-145">-Profile</span><span class="sxs-lookup"><span data-stu-id="953d6-145">-Profile</span></span>
<span data-ttu-id="953d6-146">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="953d6-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="953d6-147">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="953d6-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="953d6-148">-Restart</span><span class="sxs-lookup"><span data-stu-id="953d6-148">-Restart</span></span>
<span data-ttu-id="953d6-149">Указывает, следует ли перезагружать компьютер при успешном выполнении операции присоединения.</span><span class="sxs-lookup"><span data-stu-id="953d6-149">Specifies whether to restart the computer if the join operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d6-150">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="953d6-150">-Role</span></span>
<span data-ttu-id="953d6-151">Задает необязательный массив ролей для задания конфигурации удаленных рабочих столов для конфигурации домена доменных данных.</span><span class="sxs-lookup"><span data-stu-id="953d6-151">Specifies an optional array of roles to specify the remote desktop configuration for the AD domain configuration.</span></span>
<span data-ttu-id="953d6-152">Если этот параметр не указан, Конфигурация домена AD применяется по умолчанию для всех ролей.</span><span class="sxs-lookup"><span data-stu-id="953d6-152">If you do not specify this parameter, the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="953d6-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="953d6-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="953d6-154">Указывает алгоритм хэширования отпечатка, который используется с отпечатком для идентификации сертификата.</span><span class="sxs-lookup"><span data-stu-id="953d6-154">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="953d6-155">Этот параметр является необязательным и значение по умолчанию — SHA1.</span><span class="sxs-lookup"><span data-stu-id="953d6-155">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="953d6-156">-UnjoinDomainCredential</span><span class="sxs-lookup"><span data-stu-id="953d6-156">-UnjoinDomainCredential</span></span>
<span data-ttu-id="953d6-157">Задает учетные данные (имя пользователя и пароль) для отсоединения домена доменных имен.</span><span class="sxs-lookup"><span data-stu-id="953d6-157">Specifies the credentials (user name and password) to unjoin the AD domain.</span></span>

```yaml
Type: PSCredential
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, JoinDomainUsingEnumOptionsAndThumbprint, JoinDomainUsingJoinOptionAndThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d6-158">-Version</span><span class="sxs-lookup"><span data-stu-id="953d6-158">-Version</span></span>
<span data-ttu-id="953d6-159">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="953d6-159">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d6-160">-WorkgroupName</span><span class="sxs-lookup"><span data-stu-id="953d6-160">-WorkgroupName</span></span>
<span data-ttu-id="953d6-161">Указывает имя рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="953d6-161">Specifies the workgroup name.</span></span>

```yaml
Type: String
Parameter Sets: WorkGroupName, WorkGroupNameThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d6-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="953d6-162">-X509Certificate</span></span>
<span data-ttu-id="953d6-163">Указывает сертификат X. 509, который автоматически отправляется в облачную службу и используется для шифрования закрытой конфигурации расширения.</span><span class="sxs-lookup"><span data-stu-id="953d6-163">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: JoinDomainUsingEnumOptions, JoinDomainUsingJoinOption, WorkGroupName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953d6-164">CommonParameters</span></span>
<span data-ttu-id="953d6-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="953d6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953d6-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="953d6-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953d6-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="953d6-167">INPUTS</span></span>

## <span data-ttu-id="953d6-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="953d6-168">OUTPUTS</span></span>

## <span data-ttu-id="953d6-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="953d6-169">NOTES</span></span>

## <span data-ttu-id="953d6-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="953d6-170">RELATED LINKS</span></span>

[<span data-ttu-id="953d6-171">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="953d6-171">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="953d6-172">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="953d6-172">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


