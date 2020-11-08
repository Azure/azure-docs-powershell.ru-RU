---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075700"
---
# <span data-ttu-id="1251d-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="1251d-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="1251d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1251d-102">SYNOPSIS</span></span>
<span data-ttu-id="1251d-103">Инициирует фиксацию или откат контейнеров томов, которые переносятся.</span><span class="sxs-lookup"><span data-stu-id="1251d-103">Initiates the commit or rollback of the volume containers that are migrated.</span></span>

## <span data-ttu-id="1251d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1251d-104">SYNTAX</span></span>

### <span data-ttu-id="1251d-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="1251d-105">MigrateSpecificContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1251d-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="1251d-106">MigrateAllContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1251d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1251d-107">DESCRIPTION</span></span>
<span data-ttu-id="1251d-108">Командлет **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** инициирует фиксацию или откат контейнеров томов, перенесенных в рамках устаревшего переноса.</span><span class="sxs-lookup"><span data-stu-id="1251d-108">The **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet initiates the commit or rollback of the volume containers that are migrated as part of a legacy migration.</span></span>
<span data-ttu-id="1251d-109">Функция ROLLBACK восстанавливает исходное владение устройства.</span><span class="sxs-lookup"><span data-stu-id="1251d-109">The rollback restores the appliance to the original ownership.</span></span>
<span data-ttu-id="1251d-110">Фиксация назначает владение оконечному устройству.</span><span class="sxs-lookup"><span data-stu-id="1251d-110">The commit assigns the ownership to the target appliance.</span></span>

## <span data-ttu-id="1251d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1251d-111">EXAMPLES</span></span>

### <span data-ttu-id="1251d-112">Пример 1: запуск операции фиксации для определенного контейнера тома</span><span class="sxs-lookup"><span data-stu-id="1251d-112">Example 1: Initiate a commit operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="1251d-113">Эта команда инициирует операцию фиксации в указанном контейнере тома для указанного идентификатора прежней конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1251d-113">This command initiates a commit operation on the specified volume container for the specified legacy configuration ID.</span></span>
<span data-ttu-id="1251d-114">Чтобы просмотреть состояние операции, используйте командлет **Get-AzureStorSimpleLegacyVolumeContainerStatus** .</span><span class="sxs-lookup"><span data-stu-id="1251d-114">To see the status of the operation, use the **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet.</span></span>

### <span data-ttu-id="1251d-115">Пример 2: запуск операции отката для определенного контейнера тома</span><span class="sxs-lookup"><span data-stu-id="1251d-115">Example 2: Initiate a rollback operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="1251d-116">Эта команда инициирует операцию отката для указанного контейнера тома для указанного идентификатора прежней конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1251d-116">This command initiates a rollback operation on the specified volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="1251d-117">Пример 3: запуск операции фиксации для всех контейнеров томов</span><span class="sxs-lookup"><span data-stu-id="1251d-117">Example 3: Initiate a commit operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="1251d-118">Эта команда инициирует операцию фиксации для всего контейнера тома для указанного идентификатора прежней конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1251d-118">This command initiates a commit operation on all volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="1251d-119">Пример 4: запуск операции отката для всех контейнеров томов</span><span class="sxs-lookup"><span data-stu-id="1251d-119">Example 4: Initiate a rollback operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="1251d-120">Эта команда инициирует операцию отката для всех контейнеров томов для указанного ИД прежней конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1251d-120">This command initiates a rollback operation on all volume containers for the specified legacy configuration ID.</span></span>

## <span data-ttu-id="1251d-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1251d-121">PARAMETERS</span></span>

### <span data-ttu-id="1251d-122">-ALL</span><span class="sxs-lookup"><span data-stu-id="1251d-122">-All</span></span>
<span data-ttu-id="1251d-123">Указывает на то, что этот командлет инициирует откат или операцию COMMIT для всех контейнеров томов в импортированном файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1251d-123">Indicates that this cmdlet initiates a roll back or commit operation on all volume containers in the imported configuration file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1251d-124">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="1251d-124">-LegacyConfigId</span></span>
<span data-ttu-id="1251d-125">Указывает уникальный идентификатор конфигурации устаревшего устройства.</span><span class="sxs-lookup"><span data-stu-id="1251d-125">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1251d-126">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="1251d-126">-LegacyContainerNames</span></span>
<span data-ttu-id="1251d-127">Указывает массив имен контейнеров томов, к которым применяется план миграции.</span><span class="sxs-lookup"><span data-stu-id="1251d-127">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1251d-128">-MigrationOperation</span><span class="sxs-lookup"><span data-stu-id="1251d-128">-MigrationOperation</span></span>
<span data-ttu-id="1251d-129">Указывает, выполняет ли этот командлет фиксацию или откат.</span><span class="sxs-lookup"><span data-stu-id="1251d-129">Specifies whether this cmdlet performs a commit or rollback.</span></span>
<span data-ttu-id="1251d-130">Допустимые значения: Commit и Rollback.</span><span class="sxs-lookup"><span data-stu-id="1251d-130">Valid values are: Commit and Rollback.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1251d-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="1251d-131">-Profile</span></span>
<span data-ttu-id="1251d-132">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1251d-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1251d-133">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1251d-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1251d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1251d-134">CommonParameters</span></span>
<span data-ttu-id="1251d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1251d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1251d-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1251d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1251d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1251d-137">INPUTS</span></span>

## <span data-ttu-id="1251d-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1251d-138">OUTPUTS</span></span>

## <span data-ttu-id="1251d-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1251d-139">NOTES</span></span>

## <span data-ttu-id="1251d-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1251d-140">RELATED LINKS</span></span>

[<span data-ttu-id="1251d-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="1251d-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="1251d-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="1251d-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[<span data-ttu-id="1251d-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="1251d-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


