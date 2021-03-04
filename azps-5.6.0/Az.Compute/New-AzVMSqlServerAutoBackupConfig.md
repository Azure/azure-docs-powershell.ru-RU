---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 6d9047679f4286e0e2212ca8e599237825326dd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975923"
---
# <span data-ttu-id="c66c5-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="c66c5-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="c66c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c66c5-102">SYNOPSIS</span></span>
<span data-ttu-id="c66c5-103">Создает объект конфигурации для автоматического SQL Server резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="c66c5-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="c66c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c66c5-104">SYNTAX</span></span>

### <span data-ttu-id="c66c5-105">StorageUriSqlServerAutoBackup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c66c5-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c66c5-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="c66c5-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c66c5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c66c5-107">DESCRIPTION</span></span>
<span data-ttu-id="c66c5-108">Для автоматического резервного копирования создается объект конфигурации для SQL Server **AzVMSqlServerAutoBackupConfig.**</span><span class="sxs-lookup"><span data-stu-id="c66c5-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="c66c5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c66c5-109">EXAMPLES</span></span>

### <span data-ttu-id="c66c5-110">Пример 1. Создание автоматической настройки резервного копирования с использованием URI хранилища и ключа учетной записи</span><span class="sxs-lookup"><span data-stu-id="c66c5-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="c66c5-111">Эта команда создает объект автоматической резервной копии с указанием URI хранилища и ключа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c66c5-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="c66c5-112">Автоматическое резервное копирование включено, и автоматическое резервное копирование хранится в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="c66c5-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="c66c5-113">Команда сохраняет результат в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="c66c5-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="c66c5-114">Вы можете указать этот элемент конфигурации для других Set-AzVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="c66c5-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="c66c5-115">Пример 2. Создание автоматической настройки резервного копирования с использованием контекста хранилища</span><span class="sxs-lookup"><span data-stu-id="c66c5-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="c66c5-116">Первая команда создает контекст хранилища, а затем сохраняет его в $StorageContext переменной.</span><span class="sxs-lookup"><span data-stu-id="c66c5-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="c66c5-117">Дополнительные сведения см. в new-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c66c5-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="c66c5-118">Вторая команда создает объект автоматической резервной копии путем указания контекста хранилища в $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="c66c5-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="c66c5-119">Автоматическое резервное копирование включено, и автоматическое резервное копирование хранится в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="c66c5-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="c66c5-120">Пример 3. Создание автоматической резервной копии с использованием контекста хранилища с шифрованием и паролем</span><span class="sxs-lookup"><span data-stu-id="c66c5-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="c66c5-121">Эта команда создает и сохраняет объект автоматической резервной копии.</span><span class="sxs-lookup"><span data-stu-id="c66c5-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="c66c5-122">Команда определяет контекст хранилища, созданный в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="c66c5-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="c66c5-123">Она позволяет использовать шифрование с помощью пароля.</span><span class="sxs-lookup"><span data-stu-id="c66c5-123">The command enables encryption with password.</span></span>
<span data-ttu-id="c66c5-124">Пароль ранее хранился как безопасная строка в переменной $CertificatePassword.</span><span class="sxs-lookup"><span data-stu-id="c66c5-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="c66c5-125">Чтобы создать безопасную строку, используйте ConvertTo-SecureString- и безопасную строку.</span><span class="sxs-lookup"><span data-stu-id="c66c5-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="c66c5-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c66c5-126">PARAMETERS</span></span>

### <span data-ttu-id="c66c5-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="c66c5-127">-BackupScheduleType</span></span>
<span data-ttu-id="c66c5-128">Тип расписания резервного копирования, вручную или автоматически</span><span class="sxs-lookup"><span data-stu-id="c66c5-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="c66c5-129">-BackupSystemDbs</span></span>
<span data-ttu-id="c66c5-130">Резервное копирование системных баз данных</span><span class="sxs-lookup"><span data-stu-id="c66c5-130">Backup system databases</span></span>

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

### <span data-ttu-id="c66c5-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c66c5-131">-CertificatePassword</span></span>
<span data-ttu-id="c66c5-132">Пароль для шифрования сертификата, используемого для SQL Server архивации.</span><span class="sxs-lookup"><span data-stu-id="c66c5-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c66c5-133">-DefaultProfile</span></span>
<span data-ttu-id="c66c5-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c66c5-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="c66c5-135">-Enable</span></span>
<span data-ttu-id="c66c5-136">Означает, что автоматическое резервное копирование SQL Server виртуальной машине включено.</span><span class="sxs-lookup"><span data-stu-id="c66c5-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="c66c5-137">Если этот параметр указан, автоматическое резервное копирование создает расписание резервного копирования для всех текущих и новых баз данных.</span><span class="sxs-lookup"><span data-stu-id="c66c5-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="c66c5-138">Это обновление параметров управляемого резервного копирования в следуйте этому расписанию.</span><span class="sxs-lookup"><span data-stu-id="c66c5-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="c66c5-139">-EnableEncryption</span></span>
<span data-ttu-id="c66c5-140">Указывает на то, что этот cmdlet включает шифрование.</span><span class="sxs-lookup"><span data-stu-id="c66c5-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="c66c5-141">-FullBackupFrequency</span></span>
<span data-ttu-id="c66c5-142">Периодичность полной резервной копии Sql Server : ежедневно или еженедельно</span><span class="sxs-lookup"><span data-stu-id="c66c5-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="c66c5-143">-FullBackupStartHour</span></span>
<span data-ttu-id="c66c5-144">Час дня (0–23), когда должна начаться полная резервная копия Sql Server</span><span class="sxs-lookup"><span data-stu-id="c66c5-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="c66c5-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="c66c5-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="c66c5-146">Окно полной резервной копии В часах в Sql Server</span><span class="sxs-lookup"><span data-stu-id="c66c5-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="c66c5-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="c66c5-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="c66c5-148">Частота резервного копирования журнала Sql Server каждые 1–60 минут</span><span class="sxs-lookup"><span data-stu-id="c66c5-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="c66c5-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c66c5-149">-ResourceGroupName</span></span>
<span data-ttu-id="c66c5-150">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c66c5-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c66c5-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="c66c5-152">Количество дней для сохранения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="c66c5-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="c66c5-153">-StorageContext</span></span>
<span data-ttu-id="c66c5-154">Указывает учетную запись хранения, которая будет использоваться для хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="c66c5-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="c66c5-155">Чтобы получить объект **AzureStorageContext,** используйте New-AzStorageContext..</span><span class="sxs-lookup"><span data-stu-id="c66c5-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="c66c5-156">По умолчанию это учетная запись хранения, связанная с виртуальной SQL Server компьютера.</span><span class="sxs-lookup"><span data-stu-id="c66c5-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="c66c5-157">-StorageKey</span></span>
<span data-ttu-id="c66c5-158">Указывает ключ хранилища для учетной записи хранилища BLOB-хранилищ.</span><span class="sxs-lookup"><span data-stu-id="c66c5-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="c66c5-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="c66c5-159">-StorageUri</span></span>
<span data-ttu-id="c66c5-160">Указывает URI учетной записи хранилища BLOB-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c66c5-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="c66c5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c66c5-161">CommonParameters</span></span>
<span data-ttu-id="c66c5-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c66c5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c66c5-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c66c5-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c66c5-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c66c5-164">INPUTS</span></span>

### <span data-ttu-id="c66c5-165">System.String</span><span class="sxs-lookup"><span data-stu-id="c66c5-165">System.String</span></span>

### <span data-ttu-id="c66c5-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c66c5-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c66c5-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c66c5-167">System.Int32</span></span>

### <span data-ttu-id="c66c5-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c66c5-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="c66c5-169">System.Uri</span><span class="sxs-lookup"><span data-stu-id="c66c5-169">System.Uri</span></span>

### <span data-ttu-id="c66c5-170">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="c66c5-170">System.Security.SecureString</span></span>

### <span data-ttu-id="c66c5-171">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c66c5-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c66c5-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c66c5-172">OUTPUTS</span></span>

### <span data-ttu-id="c66c5-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="c66c5-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="c66c5-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c66c5-174">NOTES</span></span>

## <span data-ttu-id="c66c5-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c66c5-175">RELATED LINKS</span></span>

[<span data-ttu-id="c66c5-176">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="c66c5-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="c66c5-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="c66c5-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


