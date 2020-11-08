---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 55E097F4-1F49-4196-9A8B-949FD5D9108A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4035487fa0363e6a7802966d9bc6422429723d94
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076199"
---
# <span data-ttu-id="eb459-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="eb459-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="eb459-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb459-102">SYNOPSIS</span></span>
<span data-ttu-id="eb459-103">Создает объект конфигурации для автоматической архивации SQL Server.</span><span class="sxs-lookup"><span data-stu-id="eb459-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="eb459-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb459-104">SYNTAX</span></span>

### <span data-ttu-id="eb459-105">StorageUriSqlServerAutoBackup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eb459-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb459-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="eb459-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eb459-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb459-107">DESCRIPTION</span></span>
<span data-ttu-id="eb459-108">Командлет **New-AzureVMSqlServerAutoBackupConfig** создает объект конфигурации для автоматической архивации SQL Server.</span><span class="sxs-lookup"><span data-stu-id="eb459-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="eb459-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb459-109">EXAMPLES</span></span>

### <span data-ttu-id="eb459-110">Пример 1: создание конфигурации автоматического резервного копирования с помощью URI хранилища и ключа учетной записи</span><span class="sxs-lookup"><span data-stu-id="eb459-110">Example 1: Create an auto-backup configuration using storage URI and account key</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="eb459-111">Эта команда создает объект конфигурации автоматического резервного копирования, указывая URL-адрес хранилища и ключ учетной записи.</span><span class="sxs-lookup"><span data-stu-id="eb459-111">This command creates an auto-backup configuration object by specifying storage URL and account key.</span></span>

### <span data-ttu-id="eb459-112">Пример 2: создание конфигурации автоматического резервного копирования с помощью контекста хранилища</span><span class="sxs-lookup"><span data-stu-id="eb459-112">Example 2: Create an auto-backup configuration using storage context</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="eb459-113">Эта команда создает объект конфигурации автоматического резервного копирования, указав контекст хранилища.</span><span class="sxs-lookup"><span data-stu-id="eb459-113">This command creates an auto-backup configuration object by specifying storage context.</span></span>

### <span data-ttu-id="eb459-114">Пример 3: создание конфигурации автоматического резервного копирования с помощью контекста хранилища с шифрованием и паролем</span><span class="sxs-lookup"><span data-stu-id="eb459-114">Example 3: Create an auto-backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertPasswd
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="eb459-115">Эта команда создает объект конфигурации для автоматического резервного копирования, указав контекст хранилища и включив параметр шифрования с паролем.</span><span class="sxs-lookup"><span data-stu-id="eb459-115">This command creates an auto-backup configuration object by specifying Storage context and enabling encryption option with password.</span></span>
<span data-ttu-id="eb459-116">IST certificatepassword, сохраненный в переменной с именем $CertPasswd.</span><span class="sxs-lookup"><span data-stu-id="eb459-116">The certificatepassword ist stored in the variable named $CertPasswd.</span></span>

## <span data-ttu-id="eb459-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb459-117">PARAMETERS</span></span>

### <span data-ttu-id="eb459-118">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="eb459-118">-BackupScheduleType</span></span>
<span data-ttu-id="eb459-119">Тип расписания резервного копирования, ручной или автоматический</span><span class="sxs-lookup"><span data-stu-id="eb459-119">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-120">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="eb459-120">-BackupSystemDbs</span></span>
<span data-ttu-id="eb459-121">Резервное копирование системных баз данных</span><span class="sxs-lookup"><span data-stu-id="eb459-121">Backup system databases</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="eb459-122">-CertificatePassword</span></span>
<span data-ttu-id="eb459-123">Указывает пароль для шифрования сертификата, используемого для выполнения зашифрованных резервных копий SQL Server.</span><span class="sxs-lookup"><span data-stu-id="eb459-123">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-124">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="eb459-124">-Enable</span></span>
<span data-ttu-id="eb459-125">Указывает на то, что для виртуальной машины SQL Server включена автоматическая архивация.</span><span class="sxs-lookup"><span data-stu-id="eb459-125">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="eb459-126">При использовании этого параметра Автоматическая архивация задает расписание архивации для всех текущих и новых баз данных.</span><span class="sxs-lookup"><span data-stu-id="eb459-126">If you use this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="eb459-127">Это обновит параметры управляемого резервного копирования таким образом, чтобы они выполнив это расписание.</span><span class="sxs-lookup"><span data-stu-id="eb459-127">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-128">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="eb459-128">-EnableEncryption</span></span>
<span data-ttu-id="eb459-129">Указывает, что шифрование включено.</span><span class="sxs-lookup"><span data-stu-id="eb459-129">Indicates that encryption is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-130">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="eb459-130">-FullBackupFrequency</span></span>
<span data-ttu-id="eb459-131">Частота полного резервного копирования SQL Server, ежедневно или неделю</span><span class="sxs-lookup"><span data-stu-id="eb459-131">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-132">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="eb459-132">-FullBackupStartHour</span></span>
<span data-ttu-id="eb459-133">Часы суток (0-23), когда должна начинаться полная резервная копия SQL Server</span><span class="sxs-lookup"><span data-stu-id="eb459-133">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-134">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="eb459-134">-FullBackupWindowInHours</span></span>
<span data-ttu-id="eb459-135">Окно полного резервного копирования SQL Server в часах</span><span class="sxs-lookup"><span data-stu-id="eb459-135">Sql Server Full Backup window in hours</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="eb459-136">-InformationAction</span></span>
<span data-ttu-id="eb459-137">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="eb459-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eb459-138">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="eb459-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb459-139">Продолжал</span><span class="sxs-lookup"><span data-stu-id="eb459-139">Continue</span></span>
- <span data-ttu-id="eb459-140">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="eb459-140">Ignore</span></span>
- <span data-ttu-id="eb459-141">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="eb459-141">Inquire</span></span>
- <span data-ttu-id="eb459-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eb459-142">SilentlyContinue</span></span>
- <span data-ttu-id="eb459-143">Остановить</span><span class="sxs-lookup"><span data-stu-id="eb459-143">Stop</span></span>
- <span data-ttu-id="eb459-144">Рвать</span><span class="sxs-lookup"><span data-stu-id="eb459-144">Suspend</span></span>

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

### <span data-ttu-id="eb459-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eb459-145">-InformationVariable</span></span>
<span data-ttu-id="eb459-146">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="eb459-146">Specifies an information variable.</span></span>

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

### <span data-ttu-id="eb459-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="eb459-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="eb459-148">Частота резервного копирования журнала SQL Server каждые 1-60 минут</span><span class="sxs-lookup"><span data-stu-id="eb459-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-149">-Profile</span><span class="sxs-lookup"><span data-stu-id="eb459-149">-Profile</span></span>
<span data-ttu-id="eb459-150">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eb459-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eb459-151">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eb459-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eb459-152">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="eb459-152">-RetentionPeriodInDays</span></span>
<span data-ttu-id="eb459-153">Указывает продолжительность периода хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="eb459-153">Specifies the length of the retention period in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-154">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="eb459-154">-StorageContext</span></span>
<span data-ttu-id="eb459-155">Указывает учетную запись хранения, которая будет использоваться для хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="eb459-155">Specifies the storage account to be used to store backups.</span></span>
<span data-ttu-id="eb459-156">По умолчанию — учетная запись хранилища, связанная с виртуальной машиной SQL Server.</span><span class="sxs-lookup"><span data-stu-id="eb459-156">Default is the storage account associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="eb459-157">-StorageKey</span></span>
<span data-ttu-id="eb459-158">Указывает ключ хранилища для учетной записи хранения BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="eb459-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="eb459-159">-StorageUri</span></span>
<span data-ttu-id="eb459-160">Задает универсальный код ресурса (URI) для учетной записи хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="eb459-160">Specifies a URI to the blob storage account.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb459-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb459-161">CommonParameters</span></span>
<span data-ttu-id="eb459-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb459-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb459-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb459-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb459-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb459-164">INPUTS</span></span>

## <span data-ttu-id="eb459-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb459-165">OUTPUTS</span></span>

## <span data-ttu-id="eb459-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb459-166">NOTES</span></span>

## <span data-ttu-id="eb459-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb459-167">RELATED LINKS</span></span>

[<span data-ttu-id="eb459-168">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="eb459-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)


