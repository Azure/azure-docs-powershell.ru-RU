---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: da85c91aea3c47c2b3ba0e9ff19938980dbc80d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567807"
---
# <span data-ttu-id="289c4-101">New-AzureRmVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="289c4-101">New-AzureRmVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="289c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="289c4-102">SYNOPSIS</span></span>
<span data-ttu-id="289c4-103">Создает объект конфигурации для автоматической архивации SQL Server.</span><span class="sxs-lookup"><span data-stu-id="289c4-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="289c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="289c4-104">SYNTAX</span></span>

### <span data-ttu-id="289c4-105">StorageUriSqlServerAutoBackup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="289c4-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="289c4-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="289c4-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="289c4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="289c4-107">DESCRIPTION</span></span>
<span data-ttu-id="289c4-108">Командлет **New-AzureRmVMSqlServerAutoBackupConfig** создает объект конфигурации для автоматической архивации SQL Server.</span><span class="sxs-lookup"><span data-stu-id="289c4-108">The **New-AzureRmVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="289c4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="289c4-109">EXAMPLES</span></span>

### <span data-ttu-id="289c4-110">Пример 1: создание конфигурации автоматической архивации с помощью URI хранилища и ключа учетной записи</span><span class="sxs-lookup"><span data-stu-id="289c4-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="289c4-111">Эта команда создает объект конфигурации автоматического резервного копирования, указав URI хранилища и ключ учетной записи.</span><span class="sxs-lookup"><span data-stu-id="289c4-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="289c4-112">Автоматическая архивация включена, и автоматические резервные копии будут храниться в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="289c4-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="289c4-113">Команда сохраняет результат в переменной $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="289c4-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="289c4-114">Вы можете указать этот элемент конфигурации для других командлетов, таких как командлеты Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="289c4-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="289c4-115">Пример 2: создание конфигурации автоматической архивации с помощью контекста хранилища</span><span class="sxs-lookup"><span data-stu-id="289c4-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="289c4-116">Первая команда создает контекст хранения, а затем сохраняет его в переменной $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="289c4-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="289c4-117">Дополнительные сведения можно найти в разделе New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="289c4-117">For more information, see New-AzureStorageContext.</span></span>
<span data-ttu-id="289c4-118">Вторая команда создает объект конфигурации автоматического резервного копирования, указав контекст хранилища в $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="289c4-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="289c4-119">Автоматическая архивация включена, и автоматические резервные копии будут храниться в течение 10 дней.</span><span class="sxs-lookup"><span data-stu-id="289c4-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="289c4-120">Пример 3: создание конфигурации автоматической архивации с помощью контекста хранилища с шифрованием и паролем</span><span class="sxs-lookup"><span data-stu-id="289c4-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="289c4-121">Эта команда создает и сохраняет объект конфигурации для автоматического резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="289c4-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="289c4-122">Команда задает контекст хранения, созданный в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="289c4-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="289c4-123">Эта команда обеспечивает шифрование с помощью пароля.</span><span class="sxs-lookup"><span data-stu-id="289c4-123">The command enables encryption with password.</span></span>
<span data-ttu-id="289c4-124">Пароль был ранее сохранен в качестве безопасной строки в переменной $CertificatePassword.</span><span class="sxs-lookup"><span data-stu-id="289c4-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="289c4-125">Чтобы создать защищенную строку, используйте командлет ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="289c4-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="289c4-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="289c4-126">PARAMETERS</span></span>

### <span data-ttu-id="289c4-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="289c4-127">-BackupScheduleType</span></span>
<span data-ttu-id="289c4-128">Тип расписания резервного копирования, ручной или автоматический</span><span class="sxs-lookup"><span data-stu-id="289c4-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="289c4-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="289c4-129">-BackupSystemDbs</span></span>
<span data-ttu-id="289c4-130">Резервное копирование системных баз данных</span><span class="sxs-lookup"><span data-stu-id="289c4-130">Backup system databases</span></span>

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

### <span data-ttu-id="289c4-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="289c4-131">-CertificatePassword</span></span>
<span data-ttu-id="289c4-132">Указывает пароль для шифрования сертификата, используемого для выполнения зашифрованных резервных копий SQL Server.</span><span class="sxs-lookup"><span data-stu-id="289c4-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="289c4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="289c4-133">-DefaultProfile</span></span>
<span data-ttu-id="289c4-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="289c4-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="289c4-135">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="289c4-135">-Enable</span></span>
<span data-ttu-id="289c4-136">Указывает на то, что для виртуальной машины SQL Server включена автоматическая архивация.</span><span class="sxs-lookup"><span data-stu-id="289c4-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="289c4-137">Если указать этот параметр, автоматическая архивация задает расписание резервного копирования для всех текущих и новых баз данных.</span><span class="sxs-lookup"><span data-stu-id="289c4-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="289c4-138">Это обновит параметры управляемого резервного копирования таким образом, чтобы они выполнив это расписание.</span><span class="sxs-lookup"><span data-stu-id="289c4-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="289c4-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="289c4-139">-EnableEncryption</span></span>
<span data-ttu-id="289c4-140">Указывает на то, что этот командлет включает шифрование.</span><span class="sxs-lookup"><span data-stu-id="289c4-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="289c4-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="289c4-141">-FullBackupFrequency</span></span>
<span data-ttu-id="289c4-142">Частота полных резервных копий SQL Server, ежедневно или еженедельно</span><span class="sxs-lookup"><span data-stu-id="289c4-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="289c4-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="289c4-143">-FullBackupStartHour</span></span>
<span data-ttu-id="289c4-144">Часы суток (0-23), когда должна начинаться полная резервная копия SQL Server</span><span class="sxs-lookup"><span data-stu-id="289c4-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="289c4-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="289c4-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="289c4-146">Окно полного резервного копирования SQL Server в часах</span><span class="sxs-lookup"><span data-stu-id="289c4-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="289c4-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="289c4-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="289c4-148">Частота резервного копирования журнала SQL Server каждые 1-60 минут</span><span class="sxs-lookup"><span data-stu-id="289c4-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="289c4-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="289c4-149">-ResourceGroupName</span></span>
<span data-ttu-id="289c4-150">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="289c4-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="289c4-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="289c4-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="289c4-152">Указывает количество дней, в течение которых будет храниться резервная копия.</span><span class="sxs-lookup"><span data-stu-id="289c4-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="289c4-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="289c4-153">-StorageContext</span></span>
<span data-ttu-id="289c4-154">Указывает учетную запись хранения, которая будет использоваться для хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="289c4-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="289c4-155">Чтобы получить объект **AzureStorageContext** , используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="289c4-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="289c4-156">По умолчанию используется учетная запись хранения, связанная с виртуальной машиной SQL Server.</span><span class="sxs-lookup"><span data-stu-id="289c4-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

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

### <span data-ttu-id="289c4-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="289c4-157">-StorageKey</span></span>
<span data-ttu-id="289c4-158">Указывает ключ хранилища для учетной записи хранения BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="289c4-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="289c4-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="289c4-159">-StorageUri</span></span>
<span data-ttu-id="289c4-160">Задает универсальный код ресурса (URI) учетной записи хранилища BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="289c4-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="289c4-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="289c4-161">CommonParameters</span></span>
<span data-ttu-id="289c4-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="289c4-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="289c4-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="289c4-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="289c4-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="289c4-164">INPUTS</span></span>

### <span data-ttu-id="289c4-165">System. String</span><span class="sxs-lookup"><span data-stu-id="289c4-165">System.String</span></span>

### <span data-ttu-id="289c4-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="289c4-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="289c4-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="289c4-167">System.Int32</span></span>

### <span data-ttu-id="289c4-168">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="289c4-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="289c4-169">System. URI</span><span class="sxs-lookup"><span data-stu-id="289c4-169">System.Uri</span></span>

### <span data-ttu-id="289c4-170">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="289c4-170">System.Security.SecureString</span></span>

### <span data-ttu-id="289c4-171">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="289c4-171">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="289c4-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="289c4-172">OUTPUTS</span></span>

### <span data-ttu-id="289c4-173">Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="289c4-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="289c4-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="289c4-174">NOTES</span></span>

## <span data-ttu-id="289c4-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="289c4-175">RELATED LINKS</span></span>

[<span data-ttu-id="289c4-176">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="289c4-176">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="289c4-177">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="289c4-177">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


