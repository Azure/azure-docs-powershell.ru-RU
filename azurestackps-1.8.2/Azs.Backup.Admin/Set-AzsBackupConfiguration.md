---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b6e8139f201a69684d4236a5e84e89f6607c5c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076802"
---
# <span data-ttu-id="11434-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="11434-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="11434-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11434-102">SYNOPSIS</span></span>
<span data-ttu-id="11434-103">Настройте конфигурацию резервного копирования в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="11434-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="11434-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11434-104">SYNTAX</span></span>

### <span data-ttu-id="11434-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11434-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11434-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="11434-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11434-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="11434-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11434-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11434-108">DESCRIPTION</span></span>
<span data-ttu-id="11434-109">Настройте конфигурацию резервного копирования в указанном месте.</span><span class="sxs-lookup"><span data-stu-id="11434-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="11434-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11434-110">EXAMPLES</span></span>

### <span data-ttu-id="11434-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="11434-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="11434-112">Настройте параметры резервного копирования стеков Azure.</span><span class="sxs-lookup"><span data-stu-id="11434-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="11434-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11434-113">PARAMETERS</span></span>

### <span data-ttu-id="11434-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11434-114">-AsJob</span></span>
<span data-ttu-id="11434-115">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="11434-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11434-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="11434-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="11434-117">Интервал (в часах) для частоты, из-за которой планировщик выполняет резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="11434-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11434-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="11434-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="11434-119">Срок хранения (в днях) для резервного копирования в местоположении хранения.</span><span class="sxs-lookup"><span data-stu-id="11434-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11434-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="11434-120">-EncryptionKey</span></span>
<span data-ttu-id="11434-121">Ключ шифрования, используемый для шифрования резервных копий.</span><span class="sxs-lookup"><span data-stu-id="11434-121">Encryption key used to encrypt backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11434-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11434-122">-InputObject</span></span>
<span data-ttu-id="11434-123">Конфигурация местоположения резервных копий, возвращенная функцией Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="11434-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11434-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="11434-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="11434-125">Должен ли быть включен планировщик резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="11434-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11434-126">-Location</span><span class="sxs-lookup"><span data-stu-id="11434-126">-Location</span></span>
<span data-ttu-id="11434-127">Расположение для настройки.</span><span class="sxs-lookup"><span data-stu-id="11434-127">Location to configure.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11434-128">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="11434-128">-Password</span></span>
<span data-ttu-id="11434-129">Требуется пароль для доступа к расположению резервной копии.</span><span class="sxs-lookup"><span data-stu-id="11434-129">Password required to access backup location.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11434-130">-Path</span><span class="sxs-lookup"><span data-stu-id="11434-130">-Path</span></span>
<span data-ttu-id="11434-131">Расположение, в котором будут храниться резервные копии.</span><span class="sxs-lookup"><span data-stu-id="11434-131">Location where backups will be stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11434-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11434-132">-ResourceGroupName</span></span>
<span data-ttu-id="11434-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11434-133">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11434-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11434-134">-ResourceId</span></span>
<span data-ttu-id="11434-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="11434-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11434-136">-Username</span><span class="sxs-lookup"><span data-stu-id="11434-136">-Username</span></span>
<span data-ttu-id="11434-137">Для доступа к расположению резервной копии требуется имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="11434-137">Username required to access backup location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11434-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11434-138">-Confirm</span></span>
<span data-ttu-id="11434-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11434-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11434-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11434-140">-WhatIf</span></span>
<span data-ttu-id="11434-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11434-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11434-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11434-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11434-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11434-143">CommonParameters</span></span>
<span data-ttu-id="11434-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11434-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11434-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11434-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11434-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11434-146">INPUTS</span></span>

## <span data-ttu-id="11434-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11434-147">OUTPUTS</span></span>

### <span data-ttu-id="11434-148">Microsoft. AzureStack. Management. Backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="11434-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="11434-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="11434-149">NOTES</span></span>

## <span data-ttu-id="11434-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11434-150">RELATED LINKS</span></span>

