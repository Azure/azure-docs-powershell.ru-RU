---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: ce4550d4b0b0206db3a28f11a58ac4384ecbac60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558555"
---
# <span data-ttu-id="094fc-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="094fc-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="094fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="094fc-102">SYNOPSIS</span></span>
<span data-ttu-id="094fc-103">Создание политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="094fc-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="094fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="094fc-104">SYNTAX</span></span>

### <span data-ttu-id="094fc-105">NoScheduleParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="094fc-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="094fc-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="094fc-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="094fc-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="094fc-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="094fc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="094fc-108">DESCRIPTION</span></span>
<span data-ttu-id="094fc-109">Командлет **New-AzureRmBackupProtectionPolicy** создает политику архивации Azure как объект Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="094fc-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>
<span data-ttu-id="094fc-110">Политика архивации определяет периодичность и частоту резервного копирования элемента.</span><span class="sxs-lookup"><span data-stu-id="094fc-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="094fc-111">Командлет Enable-AzureRmBackupProtection использует политику резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="094fc-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="094fc-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="094fc-112">EXAMPLES</span></span>

### <span data-ttu-id="094fc-113">Пример 1: создание ежедневной политики резервного копирования с ежедневной и ежемесячной удержанием</span><span class="sxs-lookup"><span data-stu-id="094fc-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="094fc-114">Первая команда получает хранилище с именем Vault03 с помощью командлета Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="094fc-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="094fc-115">Команда сохраняет этот объект в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="094fc-115">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="094fc-116">Вторая команда создает политику хранения в течение 30 дней ежедневной сохранности, а затем сохраняет ее в переменной $Daily.</span><span class="sxs-lookup"><span data-stu-id="094fc-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>
<span data-ttu-id="094fc-117">Третья команда создает политику хранения, которая хранит резервные копии на десятой и двадцатой части каждого месяца в течение двенадцати месяцев.</span><span class="sxs-lookup"><span data-stu-id="094fc-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="094fc-118">Эта команда сохраняет политику хранения в переменной $Monthly.</span><span class="sxs-lookup"><span data-stu-id="094fc-118">The command stores the retention policy in the $Monthly variable.</span></span>
<span data-ttu-id="094fc-119">Последняя команда создает политику резервного копирования для хранилища в $Vault, в которой время ежедневного резервного копирования 3:00 PM.</span><span class="sxs-lookup"><span data-stu-id="094fc-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="094fc-120">Команда назначает политики хранения, хранящиеся в $Daily и $Monthly.</span><span class="sxs-lookup"><span data-stu-id="094fc-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="094fc-121">Команда сохраняет результат в переменной $ProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="094fc-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="094fc-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="094fc-122">PARAMETERS</span></span>

### <span data-ttu-id="094fc-123">Время простоя</span><span class="sxs-lookup"><span data-stu-id="094fc-123">-BackupTime</span></span>
<span data-ttu-id="094fc-124">Задает время суток в качестве объекта **DateTime** для операции резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="094fc-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="094fc-125">Чтобы получить **значение даты и времени** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="094fc-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="094fc-126">Для получения сведений об объектах **DateTime** введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="094fc-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094fc-127">-Ежедневно</span><span class="sxs-lookup"><span data-stu-id="094fc-127">-Daily</span></span>
<span data-ttu-id="094fc-128">Указывает на то, что операция резервного копирования выполняется в ежедневном расписании.</span><span class="sxs-lookup"><span data-stu-id="094fc-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="094fc-129">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="094fc-129">-DaysOfWeek</span></span>
<span data-ttu-id="094fc-130">Указывает массив дней недели.</span><span class="sxs-lookup"><span data-stu-id="094fc-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="094fc-131">Эта политика запускает резервное копирование в дни, заданные этим параметром.</span><span class="sxs-lookup"><span data-stu-id="094fc-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="094fc-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="094fc-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="094fc-133">Вторник</span><span class="sxs-lookup"><span data-stu-id="094fc-133">Monday</span></span> 
- <span data-ttu-id="094fc-134">Вторник</span><span class="sxs-lookup"><span data-stu-id="094fc-134">Tuesday</span></span> 
- <span data-ttu-id="094fc-135">Четверг</span><span class="sxs-lookup"><span data-stu-id="094fc-135">Wednesday</span></span> 
- <span data-ttu-id="094fc-136">Вторник</span><span class="sxs-lookup"><span data-stu-id="094fc-136">Thursday</span></span> 
- <span data-ttu-id="094fc-137">Пт</span><span class="sxs-lookup"><span data-stu-id="094fc-137">Friday</span></span> 
- <span data-ttu-id="094fc-138">Субботам</span><span class="sxs-lookup"><span data-stu-id="094fc-138">Saturday</span></span> 
- <span data-ttu-id="094fc-139">Воскресенье, если указан параметр *Weekly* , укажите этот параметр.</span><span class="sxs-lookup"><span data-stu-id="094fc-139">Sunday If you specify the *Weekly* parameter, specify this parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NoScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094fc-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="094fc-140">-DefaultProfile</span></span>
<span data-ttu-id="094fc-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="094fc-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="094fc-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="094fc-142">-Name</span></span>
<span data-ttu-id="094fc-143">Задает имя для политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="094fc-143">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="094fc-144">Выберите уникальное имя в хранилище.</span><span class="sxs-lookup"><span data-stu-id="094fc-144">Select a name that is unique in the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="094fc-145">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="094fc-145">-RetentionPolicy</span></span>
<span data-ttu-id="094fc-146">Указывает массив политик хранения для политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="094fc-146">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="094fc-147">Чтобы получить **AzureRmBackupRetentionPolicy** , используйте командлет New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="094fc-147">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094fc-148">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="094fc-148">-Type</span></span>
<span data-ttu-id="094fc-149">Указывает тип элемента резервной копии, к которому применяется политика.</span><span class="sxs-lookup"><span data-stu-id="094fc-149">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="094fc-150">В настоящее время единственным поддерживаемым значением является значение AzureVM.</span><span class="sxs-lookup"><span data-stu-id="094fc-150">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="094fc-151">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="094fc-151">-Vault</span></span>
<span data-ttu-id="094fc-152">Указывает хранилище архивации Azure, к которому относится политика резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="094fc-152">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="094fc-153">Чтобы получить объект **AzureRmBackupVault** , используйте командлет Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="094fc-153">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="094fc-154">-Еженедельно</span><span class="sxs-lookup"><span data-stu-id="094fc-154">-Weekly</span></span>
<span data-ttu-id="094fc-155">Указывает на то, что политика резервного копирования инициируется еженедельно за один или несколько дней недели.</span><span class="sxs-lookup"><span data-stu-id="094fc-155">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="094fc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="094fc-156">CommonParameters</span></span>
<span data-ttu-id="094fc-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="094fc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="094fc-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="094fc-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="094fc-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="094fc-159">INPUTS</span></span>

### <span data-ttu-id="094fc-160">System. String</span><span class="sxs-lookup"><span data-stu-id="094fc-160">System.String</span></span>

### <span data-ttu-id="094fc-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="094fc-161">System.DateTime</span></span>

### <span data-ttu-id="094fc-162">System. String []</span><span class="sxs-lookup"><span data-stu-id="094fc-162">System.String[]</span></span>

### <span data-ttu-id="094fc-163">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupRetentionPolicy []</span><span class="sxs-lookup"><span data-stu-id="094fc-163">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]</span></span>

### <span data-ttu-id="094fc-164">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="094fc-164">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="094fc-165">Параметры: хранилище (ByValue)</span><span class="sxs-lookup"><span data-stu-id="094fc-165">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="094fc-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="094fc-166">OUTPUTS</span></span>

### <span data-ttu-id="094fc-167">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="094fc-167">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>

## <span data-ttu-id="094fc-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="094fc-168">NOTES</span></span>
* <span data-ttu-id="094fc-169">Ничего</span><span class="sxs-lookup"><span data-stu-id="094fc-169">None</span></span>

## <span data-ttu-id="094fc-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="094fc-170">RELATED LINKS</span></span>

[<span data-ttu-id="094fc-171">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="094fc-171">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="094fc-172">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="094fc-172">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="094fc-173">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="094fc-173">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="094fc-174">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="094fc-174">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="094fc-175">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="094fc-175">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="094fc-176">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="094fc-176">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


