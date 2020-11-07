---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35b937b810da65cc3cc2ed330198011ec108f9d6
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "93913076"
---
# <span data-ttu-id="8e086-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="8e086-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="8e086-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e086-102">SYNOPSIS</span></span>
<span data-ttu-id="8e086-103">Восстановите резервную копию.</span><span class="sxs-lookup"><span data-stu-id="8e086-103">Restore a backup.</span></span>

## <span data-ttu-id="8e086-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e086-104">SYNTAX</span></span>

### <span data-ttu-id="8e086-105">Backups_Restore (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e086-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>]
 -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e086-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e086-106">ResourceId</span></span>
```
Restore-AzsBackup -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e086-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e086-107">DESCRIPTION</span></span>
<span data-ttu-id="8e086-108">Восстановите резервную копию.</span><span class="sxs-lookup"><span data-stu-id="8e086-108">Restore a backup.</span></span>

## <span data-ttu-id="8e086-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e086-109">EXAMPLES</span></span>

### <span data-ttu-id="8e086-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="8e086-110">EXAMPLE 1</span></span>
```
Restore-AzsBackup -Name 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword
```

<span data-ttu-id="8e086-111">Восстановление из резервной копии стека Azure.</span><span class="sxs-lookup"><span data-stu-id="8e086-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="8e086-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e086-112">PARAMETERS</span></span>

### <span data-ttu-id="8e086-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e086-113">-AsJob</span></span>
<span data-ttu-id="8e086-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="8e086-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e086-115">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="8e086-115">-DecryptionCertPassword</span></span>
<span data-ttu-id="8e086-116">Пароль сертификата расшифровки.</span><span class="sxs-lookup"><span data-stu-id="8e086-116">Password of the decryption cert.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e086-117">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="8e086-117">-DecryptionCertPath</span></span>
<span data-ttu-id="8e086-118">Путь к файлу сертификата расшифровки с закрытым ключом (PFX).</span><span class="sxs-lookup"><span data-stu-id="8e086-118">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e086-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8e086-119">-Force</span></span>
<span data-ttu-id="8e086-120">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="8e086-120">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e086-121">-Location</span><span class="sxs-lookup"><span data-stu-id="8e086-121">-Location</span></span>
<span data-ttu-id="8e086-122">Имя расположения для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="8e086-122">Name of location to backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e086-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e086-123">-Name</span></span>
<span data-ttu-id="8e086-124">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="8e086-124">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e086-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e086-125">-ResourceGroupName</span></span>
<span data-ttu-id="8e086-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e086-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e086-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e086-127">-ResourceId</span></span>
<span data-ttu-id="8e086-128">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="8e086-128">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e086-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e086-129">-Confirm</span></span>
<span data-ttu-id="8e086-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8e086-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e086-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e086-131">-WhatIf</span></span>
<span data-ttu-id="8e086-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8e086-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e086-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8e086-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e086-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e086-134">CommonParameters</span></span>
<span data-ttu-id="8e086-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e086-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e086-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e086-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e086-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e086-137">INPUTS</span></span>

## <span data-ttu-id="8e086-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e086-138">OUTPUTS</span></span>

## <span data-ttu-id="8e086-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e086-139">NOTES</span></span>

## <span data-ttu-id="8e086-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e086-140">RELATED LINKS</span></span>
