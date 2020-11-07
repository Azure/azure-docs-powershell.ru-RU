---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 2617ca54050f6a37fcc5714fe80e2f2d50e33e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734898"
---
# <span data-ttu-id="ab7a9-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="ab7a9-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="ab7a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ab7a9-103">Создает объект конфигурации для автоматической архивации SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab7a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab7a9-104">SYNTAX</span></span>

### <span data-ttu-id="ab7a9-105">StorageUriSqlServerAutoBackup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab7a9-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab7a9-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="ab7a9-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ab7a9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab7a9-107">DESCRIPTION</span></span>
<span data-ttu-id="ab7a9-108">Командлет **New-AzureVMSqlServerAutoBackupConfig** создает объект конфигурации для автоматической архивации SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="ab7a9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab7a9-109">EXAMPLES</span></span>

### <span data-ttu-id="ab7a9-110">Пример 1: создание конфигурации автоматической архивации с помощью URI хранилища и ключа учетной записи</span><span class="sxs-lookup"><span data-stu-id="ab7a9-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="ab7a9-111">Эта команда создает объект конфигурации автоматического резервного копирования, указав URI хранилища и ключ учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="ab7a9-112">Автоматическая архивация включена, и автоматические резервные копии будут храниться в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="ab7a9-113">Команда сохраняет результат в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="ab7a9-114">Вы можете указать этот элемент конфигурации для других командлетов, таких как командлеты Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="ab7a9-115">Пример 2: создание конфигурации автоматической архивации с помощью контекста хранилища</span><span class="sxs-lookup"><span data-stu-id="ab7a9-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="ab7a9-116">Первая команда создает контекст хранения, а затем сохраняет его в переменной $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="ab7a9-117">Дополнительные сведения можно найти в разделе New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="ab7a9-118">Вторая команда создает объект конфигурации автоматического резервного копирования, указав контекст хранилища в $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="ab7a9-119">Автоматическая архивация включена, и автоматические резервные копии будут храниться в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="ab7a9-120">Пример 3: создание конфигурации автоматической архивации с помощью контекста хранилища с шифрованием и паролем</span><span class="sxs-lookup"><span data-stu-id="ab7a9-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="ab7a9-121">Эта команда создает и сохраняет объект конфигурации для автоматического резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="ab7a9-122">Команда задает контекст хранения, созданный в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="ab7a9-123">Эта команда обеспечивает шифрование с помощью пароля.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-123">The command enables encryption with password.</span></span>
<span data-ttu-id="ab7a9-124">Пароль был ранее сохранен в качестве безопасной строки в переменной $CertificatePassword.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="ab7a9-125">Чтобы создать защищенную строку, используйте командлет ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="ab7a9-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab7a9-126">PARAMETERS</span></span>

### <span data-ttu-id="ab7a9-127">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="ab7a9-127">-Enable</span></span>
<span data-ttu-id="ab7a9-128">Указывает на то, что для виртуальной машины SQL Server включена автоматическая архивация.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-128">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="ab7a9-129">Если указать этот параметр, автоматическая архивация задает расписание резервного копирования для всех текущих и новых баз данных.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-129">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="ab7a9-130">Это обновит параметры управляемого резервного копирования таким образом, чтобы они выполнив это расписание.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-130">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-131">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ab7a9-131">-RetentionPeriodInDays</span></span>
<span data-ttu-id="ab7a9-132">Указывает количество дней, в течение которых будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-132">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-133">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="ab7a9-133">-EnableEncryption</span></span>
<span data-ttu-id="ab7a9-134">Указывает на то, что этот командлет включает шифрование.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-134">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ab7a9-135">-CertificatePassword</span></span>
<span data-ttu-id="ab7a9-136">Указывает пароль для шифрования сертификата, используемого для выполнения зашифрованных резервных копий SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-136">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-137">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="ab7a9-137">-StorageUri</span></span>
<span data-ttu-id="ab7a9-138">Задает универсальный код ресурса (URI) учетной записи хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-138">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-139">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="ab7a9-139">-StorageKey</span></span>
<span data-ttu-id="ab7a9-140">Указывает ключ хранилища для учетной записи хранения BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-140">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="ab7a9-141">-Profile</span></span>
<span data-ttu-id="ab7a9-142">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="ab7a9-143">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ab7a9-144">-InformationAction</span></span>
<span data-ttu-id="ab7a9-145">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="ab7a9-145">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ab7a9-146">-InformationVariable</span></span>
<span data-ttu-id="ab7a9-147">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="ab7a9-147">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ab7a9-148">-StorageContext</span></span>
<span data-ttu-id="ab7a9-149">Указывает учетную запись хранения, которая будет использоваться для хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-149">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="ab7a9-150">Чтобы получить объект **AzureStorageContext** , используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-150">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="ab7a9-151">По умолчанию используется учетная запись хранения, связанная с виртуальной машиной SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-151">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-152">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="ab7a9-152">-BackupScheduleType</span></span>
<span data-ttu-id="ab7a9-153">Тип расписания резервного копирования, ручной или автоматический</span><span class="sxs-lookup"><span data-stu-id="ab7a9-153">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-154">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="ab7a9-154">-BackupSystemDbs</span></span>
<span data-ttu-id="ab7a9-155">Резервное копирование системных баз данных</span><span class="sxs-lookup"><span data-stu-id="ab7a9-155">Backup system databases</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-156">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="ab7a9-156">-FullBackupFrequency</span></span>
<span data-ttu-id="ab7a9-157">Частота полного резервного копирования SQL Server, ежедневно или неделю</span><span class="sxs-lookup"><span data-stu-id="ab7a9-157">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-158">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="ab7a9-158">-FullBackupStartHour</span></span>
<span data-ttu-id="ab7a9-159">Часы суток (0-23), когда должна начинаться полная резервная копия SQL Server</span><span class="sxs-lookup"><span data-stu-id="ab7a9-159">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-160">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="ab7a9-160">-FullBackupWindowInHours</span></span>
<span data-ttu-id="ab7a9-161">Окно полного резервного копирования SQL Server в часах</span><span class="sxs-lookup"><span data-stu-id="ab7a9-161">Sql Server Full Backup window in hours</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-162">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="ab7a9-162">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="ab7a9-163">Частота резервного копирования журнала SQL Server каждые 1-60 минут</span><span class="sxs-lookup"><span data-stu-id="ab7a9-163">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7a9-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab7a9-164">CommonParameters</span></span>
<span data-ttu-id="ab7a9-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab7a9-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab7a9-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab7a9-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab7a9-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab7a9-167">INPUTS</span></span>

## <span data-ttu-id="ab7a9-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab7a9-168">OUTPUTS</span></span>

## <span data-ttu-id="ab7a9-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab7a9-169">NOTES</span></span>

## <span data-ttu-id="ab7a9-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab7a9-170">RELATED LINKS</span></span>

[<span data-ttu-id="ab7a9-171">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="ab7a9-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="ab7a9-172">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ab7a9-172">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


