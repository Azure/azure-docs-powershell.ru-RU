---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 3637709ca347a8e00433f247c80ec1c916e42017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560515"
---
# <span data-ttu-id="b3826-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="b3826-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="b3826-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3826-102">SYNOPSIS</span></span>
<span data-ttu-id="b3826-103">Создание политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="b3826-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3826-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3826-104">SYNTAX</span></span>

### <span data-ttu-id="b3826-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="b3826-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3826-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="b3826-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3826-107">MonthlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="b3826-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3826-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="b3826-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3826-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="b3826-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3826-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="b3826-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3826-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3826-111">DESCRIPTION</span></span>
<span data-ttu-id="b3826-112">Командлет **New-AzureRmBackupRetentionPolicyObject** создает политику хранения резервных копий Azure.</span><span class="sxs-lookup"><span data-stu-id="b3826-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="b3826-113">Политика хранения определяет, как долго резервная копия будет хранить точку восстановления.</span><span class="sxs-lookup"><span data-stu-id="b3826-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="b3826-114">Типы хранения описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="b3826-114">The types of retention are the following:</span></span> 

- <span data-ttu-id="b3826-115">За</span><span class="sxs-lookup"><span data-stu-id="b3826-115">Daily</span></span> 
- <span data-ttu-id="b3826-116">Запуск</span><span class="sxs-lookup"><span data-stu-id="b3826-116">Weekly</span></span> 
- <span data-ttu-id="b3826-117">Исходящем</span><span class="sxs-lookup"><span data-stu-id="b3826-117">Monthly</span></span> 
- <span data-ttu-id="b3826-118">Ежегодно</span><span class="sxs-lookup"><span data-stu-id="b3826-118">Yearly</span></span> 

<span data-ttu-id="b3826-119">Создайте одну политику хранения для каждого типа хранения, который вы планируете использовать.</span><span class="sxs-lookup"><span data-stu-id="b3826-119">Create one retention policy for each type of retention that you plan to use.</span></span>

<span data-ttu-id="b3826-120">Политика резервного копирования связана по крайней мере с одной политикой хранения.</span><span class="sxs-lookup"><span data-stu-id="b3826-120">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="b3826-121">Чтобы создать политику архивации, используйте командлет New-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="b3826-121">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="b3826-122">Вместо этого вы можете предоставить политику хранения для командлета Enable-AzureRmBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="b3826-122">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="b3826-123">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3826-123">EXAMPLES</span></span>

### <span data-ttu-id="b3826-124">Пример 1: Создание политики хранения для ежедневной сохранности</span><span class="sxs-lookup"><span data-stu-id="b3826-124">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="b3826-125">Первая команда создает политику хранения в течение 30 дней ежедневной сохранности, а затем сохраняет ее в переменной $Daily.</span><span class="sxs-lookup"><span data-stu-id="b3826-125">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="b3826-126">Вторая команда отображает содержимое $Daily.</span><span class="sxs-lookup"><span data-stu-id="b3826-126">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="b3826-127">Пример 2: создание ежемесячной политики хранения</span><span class="sxs-lookup"><span data-stu-id="b3826-127">Example 2: Create a monthly retention policy</span></span>
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

<span data-ttu-id="b3826-128">В первой команде создается политика хранения, которая хранит резервные копии на десятой и двадцатой части каждого месяца в течение двенадцати месяцев.</span><span class="sxs-lookup"><span data-stu-id="b3826-128">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="b3826-129">Эта команда сохраняет политику хранения в переменной $Monthly.</span><span class="sxs-lookup"><span data-stu-id="b3826-129">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="b3826-130">Вторая команда отображает содержимое $Monthly.</span><span class="sxs-lookup"><span data-stu-id="b3826-130">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="b3826-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3826-131">PARAMETERS</span></span>

### <span data-ttu-id="b3826-132">-DailyRetention</span><span class="sxs-lookup"><span data-stu-id="b3826-132">-DailyRetention</span></span>
<span data-ttu-id="b3826-133">Указывает на то, что этот командлет создает ежедневный параметр политики хранения.</span><span class="sxs-lookup"><span data-stu-id="b3826-133">Indicates that this cmdlet creates a Daily retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3826-134">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="b3826-134">-DaysOfMonth</span></span>
<span data-ttu-id="b3826-135">Задает дни месяца, которые определяют, какие из резервных точек восстановления хранятся и как долго.</span><span class="sxs-lookup"><span data-stu-id="b3826-135">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="b3826-136">Допустимые значения этого параметра: целые числа от 1 до 28 и последний.</span><span class="sxs-lookup"><span data-stu-id="b3826-136">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="b3826-137">Укажите этот параметр, если указаны параметры *DailyRetention* , *MonthlyRetentionInDailyFormat* и *YearlyRetentionInDailyFormat* .</span><span class="sxs-lookup"><span data-stu-id="b3826-137">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases: 
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3826-138">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b3826-138">-DaysOfWeek</span></span>
<span data-ttu-id="b3826-139">Указывает массив дней недели.</span><span class="sxs-lookup"><span data-stu-id="b3826-139">Specifies an array of days of the week.</span></span>
<span data-ttu-id="b3826-140">Дни, указанные этим командлетом, определяют, какие точки восстановления хранятся в резервной копии и как долго.</span><span class="sxs-lookup"><span data-stu-id="b3826-140">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="b3826-141">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b3826-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b3826-142">Вторник</span><span class="sxs-lookup"><span data-stu-id="b3826-142">Monday</span></span> 
- <span data-ttu-id="b3826-143">Вторник</span><span class="sxs-lookup"><span data-stu-id="b3826-143">Tuesday</span></span> 
- <span data-ttu-id="b3826-144">Четверг</span><span class="sxs-lookup"><span data-stu-id="b3826-144">Wednesday</span></span> 
- <span data-ttu-id="b3826-145">Вторник</span><span class="sxs-lookup"><span data-stu-id="b3826-145">Thursday</span></span> 
- <span data-ttu-id="b3826-146">Пт</span><span class="sxs-lookup"><span data-stu-id="b3826-146">Friday</span></span> 
- <span data-ttu-id="b3826-147">Субботам</span><span class="sxs-lookup"><span data-stu-id="b3826-147">Saturday</span></span> 
- <span data-ttu-id="b3826-148">Воскресеньям</span><span class="sxs-lookup"><span data-stu-id="b3826-148">Sunday</span></span>

<span data-ttu-id="b3826-149">Укажите этот параметр, если указаны параметры *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* и *YearlyRetentionInWeeklyFormat* .</span><span class="sxs-lookup"><span data-stu-id="b3826-149">Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>

<span data-ttu-id="b3826-150">Убедитесь в том, что дни недели, которые вы выбрали для резервного копирования и для хранения, выровнены.</span><span class="sxs-lookup"><span data-stu-id="b3826-150">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="b3826-151">Например, если для резервной копии задано значение "Суббота", политики хранения должны также использовать субботу.</span><span class="sxs-lookup"><span data-stu-id="b3826-151">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3826-152">-MonthlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="b3826-152">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="b3826-153">Указывает на то, что этот командлет создает месячную политику в ежедневном формате.</span><span class="sxs-lookup"><span data-stu-id="b3826-153">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3826-154">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="b3826-154">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="b3826-155">Указывает на то, что этот командлет создает месячную политику в еженедельном формате.</span><span class="sxs-lookup"><span data-stu-id="b3826-155">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3826-156">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="b3826-156">-MonthsOfYear</span></span>
<span data-ttu-id="b3826-157">Указывает, в каких месяцах года должны быть точки восстановления, которые будут храниться в течение ежегодной базы данных.</span><span class="sxs-lookup"><span data-stu-id="b3826-157">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="b3826-158">Допустимые значения этого параметра: названия месяцев, например Январь или февраль.</span><span class="sxs-lookup"><span data-stu-id="b3826-158">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3826-159">-Хранение</span><span class="sxs-lookup"><span data-stu-id="b3826-159">-Retention</span></span>
<span data-ttu-id="b3826-160">Указывает срок хранения (в днях, месяцах или годах), для которого резервная копия хранит резервную точку.</span><span class="sxs-lookup"><span data-stu-id="b3826-160">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="b3826-161">Единица зависит от того, выбрал ли этот командлет ежедневные, ежемесячные или ежегодные параметры хранения.</span><span class="sxs-lookup"><span data-stu-id="b3826-161">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="b3826-162">Например, если указать параметр *DailyRetention* , командлет интерпретирует текущий параметр как количество дней.</span><span class="sxs-lookup"><span data-stu-id="b3826-162">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3826-163">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="b3826-163">-WeeklyRetention</span></span>
<span data-ttu-id="b3826-164">Указывает на то, что этот командлет создает еженедельную политику хранения.</span><span class="sxs-lookup"><span data-stu-id="b3826-164">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3826-165">-WeekNumber</span><span class="sxs-lookup"><span data-stu-id="b3826-165">-WeekNumber</span></span>
<span data-ttu-id="b3826-166">Указывает недели месяца, которые определяют, какие из резервных точек восстановления хранятся и как долго.</span><span class="sxs-lookup"><span data-stu-id="b3826-166">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="b3826-167">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b3826-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b3826-168">Первич</span><span class="sxs-lookup"><span data-stu-id="b3826-168">First</span></span> 
- <span data-ttu-id="b3826-169">2</span><span class="sxs-lookup"><span data-stu-id="b3826-169">Second</span></span> 
- <span data-ttu-id="b3826-170">Третьего</span><span class="sxs-lookup"><span data-stu-id="b3826-170">Third</span></span> 
- <span data-ttu-id="b3826-171">Заканчива</span><span class="sxs-lookup"><span data-stu-id="b3826-171">Fourth</span></span> 
- <span data-ttu-id="b3826-172">Времени</span><span class="sxs-lookup"><span data-stu-id="b3826-172">Last</span></span>

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3826-173">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="b3826-173">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="b3826-174">Указывает на то, что этот командлет создает политику хранения ежегодно в ежедневном формате.</span><span class="sxs-lookup"><span data-stu-id="b3826-174">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3826-175">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="b3826-175">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="b3826-176">Указывает на то, что этот командлет создает политику хранения ежегодно в недельном формате.</span><span class="sxs-lookup"><span data-stu-id="b3826-176">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3826-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3826-177">-DefaultProfile</span></span>
<span data-ttu-id="b3826-178">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3826-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3826-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3826-179">CommonParameters</span></span>
<span data-ttu-id="b3826-180">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3826-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3826-181">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3826-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3826-182">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3826-182">INPUTS</span></span>

### <span data-ttu-id="b3826-183">Ничего</span><span class="sxs-lookup"><span data-stu-id="b3826-183">None</span></span>

## <span data-ttu-id="b3826-184">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3826-184">OUTPUTS</span></span>

### <span data-ttu-id="b3826-185">AzureRmBackupRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3826-185">AzureRmBackupRetentionPolicy</span></span>

## <span data-ttu-id="b3826-186">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3826-186">NOTES</span></span>
* <span data-ttu-id="b3826-187">Ничего</span><span class="sxs-lookup"><span data-stu-id="b3826-187">None</span></span>

## <span data-ttu-id="b3826-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3826-188">RELATED LINKS</span></span>

[<span data-ttu-id="b3826-189">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="b3826-189">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="b3826-190">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3826-190">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


