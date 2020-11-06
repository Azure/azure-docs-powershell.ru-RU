---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: caf6394ce84b18bd8e36b4504173fe7f7bb07fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561147"
---
# <span data-ttu-id="a08b5-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a08b5-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="a08b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a08b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a08b5-103">Изменение существующей политики защиты.</span><span class="sxs-lookup"><span data-stu-id="a08b5-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a08b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a08b5-104">SYNTAX</span></span>

### <span data-ttu-id="a08b5-105">NoScheduleParamSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a08b5-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a08b5-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="a08b5-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a08b5-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="a08b5-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a08b5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a08b5-108">DESCRIPTION</span></span>
<span data-ttu-id="a08b5-109">Командлет **Set-AzureRmBackupProtectionPolicy** изменяет существующую политику защиты в резервной копии Azure.</span><span class="sxs-lookup"><span data-stu-id="a08b5-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="a08b5-110">Вы можете изменить следующие компоненты политики защиты:</span><span class="sxs-lookup"><span data-stu-id="a08b5-110">You can modify the following protection policy components:</span></span> 
- <span data-ttu-id="a08b5-111">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="a08b5-111">Name</span></span>
- <span data-ttu-id="a08b5-112">Расписание резервного копирования</span><span class="sxs-lookup"><span data-stu-id="a08b5-112">Backup schedule</span></span>
- <span data-ttu-id="a08b5-113">Политики хранения изменения могут повлиять на резервное копирование и хранение элементов, связанных с политикой.</span><span class="sxs-lookup"><span data-stu-id="a08b5-113">Retention policies Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="a08b5-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a08b5-114">EXAMPLES</span></span>

## <span data-ttu-id="a08b5-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a08b5-115">PARAMETERS</span></span>

### <span data-ttu-id="a08b5-116">Время простоя</span><span class="sxs-lookup"><span data-stu-id="a08b5-116">-BackupTime</span></span>
<span data-ttu-id="a08b5-117">Задает новое время архивации в качестве объекта **DateTime** для политики.</span><span class="sxs-lookup"><span data-stu-id="a08b5-117">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="a08b5-118">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="a08b5-118">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="a08b5-119">Для получения сведений об объектах **DateTime** введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="a08b5-119">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a08b5-120">-Ежедневно</span><span class="sxs-lookup"><span data-stu-id="a08b5-120">-Daily</span></span>
<span data-ttu-id="a08b5-121">Указывает на то, что операция резервного копирования выполняется в ежедневном расписании.</span><span class="sxs-lookup"><span data-stu-id="a08b5-121">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a08b5-122">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a08b5-122">-DaysOfWeek</span></span>
<span data-ttu-id="a08b5-123">Указывает массив дней недели.</span><span class="sxs-lookup"><span data-stu-id="a08b5-123">Specifies an array of days of the week.</span></span>
<span data-ttu-id="a08b5-124">Эта политика запускает резервное копирование в дни, заданные этим параметром.</span><span class="sxs-lookup"><span data-stu-id="a08b5-124">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="a08b5-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a08b5-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a08b5-126">Вторник</span><span class="sxs-lookup"><span data-stu-id="a08b5-126">Monday</span></span> 
- <span data-ttu-id="a08b5-127">Вторник</span><span class="sxs-lookup"><span data-stu-id="a08b5-127">Tuesday</span></span> 
- <span data-ttu-id="a08b5-128">Четверг</span><span class="sxs-lookup"><span data-stu-id="a08b5-128">Wednesday</span></span> 
- <span data-ttu-id="a08b5-129">Вторник</span><span class="sxs-lookup"><span data-stu-id="a08b5-129">Thursday</span></span> 
- <span data-ttu-id="a08b5-130">Пт</span><span class="sxs-lookup"><span data-stu-id="a08b5-130">Friday</span></span> 
- <span data-ttu-id="a08b5-131">Субботам</span><span class="sxs-lookup"><span data-stu-id="a08b5-131">Saturday</span></span> 
- <span data-ttu-id="a08b5-132">Воскресеньям</span><span class="sxs-lookup"><span data-stu-id="a08b5-132">Sunday</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a08b5-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a08b5-133">-DefaultProfile</span></span>
<span data-ttu-id="a08b5-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a08b5-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a08b5-135">-NewName</span><span class="sxs-lookup"><span data-stu-id="a08b5-135">-NewName</span></span>
<span data-ttu-id="a08b5-136">Задает новое имя для политики.</span><span class="sxs-lookup"><span data-stu-id="a08b5-136">Specifies the new name for the policy.</span></span>
<span data-ttu-id="a08b5-137">Это имя должно быть уникальным в хранилище.</span><span class="sxs-lookup"><span data-stu-id="a08b5-137">This name must be unique in a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a08b5-138">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a08b5-138">-ProtectionPolicy</span></span>
<span data-ttu-id="a08b5-139">Задает политику защиты, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a08b5-139">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="a08b5-140">Чтобы получить объект **AzureRmBackupProtectionPolicy** , используйте командлет Get-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a08b5-140">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a08b5-141">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a08b5-141">-RetentionPolicy</span></span>
<span data-ttu-id="a08b5-142">Указывает массив политик хранения для политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a08b5-142">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="a08b5-143">Чтобы получить объекты **AzureRmBackupRetentionPolicy** , используйте командлет New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="a08b5-143">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a08b5-144">-Еженедельно</span><span class="sxs-lookup"><span data-stu-id="a08b5-144">-Weekly</span></span>
<span data-ttu-id="a08b5-145">Указывает на то, что операция резервного копирования выполняется в недельном расписании.</span><span class="sxs-lookup"><span data-stu-id="a08b5-145">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a08b5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a08b5-146">CommonParameters</span></span>
<span data-ttu-id="a08b5-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a08b5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a08b5-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a08b5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a08b5-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a08b5-149">INPUTS</span></span>

### <span data-ttu-id="a08b5-150">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a08b5-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>
<span data-ttu-id="a08b5-151">Параметры: ProtectionPolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a08b5-151">Parameters: ProtectionPolicy (ByValue)</span></span>

## <span data-ttu-id="a08b5-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a08b5-152">OUTPUTS</span></span>

### <span data-ttu-id="a08b5-153">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="a08b5-153">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="a08b5-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="a08b5-154">NOTES</span></span>

## <span data-ttu-id="a08b5-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a08b5-155">RELATED LINKS</span></span>

[<span data-ttu-id="a08b5-156">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a08b5-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


