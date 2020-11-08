---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A736738A-C6B3-4E5A-B9BA-D6559A27A667
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95e604c6c3f6766ccfc89bd9018dbe2241fb5b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076550"
---
# <span data-ttu-id="c4915-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="c4915-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="c4915-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4915-102">SYNOPSIS</span></span>
<span data-ttu-id="c4915-103">Получает состояние миграции контейнеров томов.</span><span class="sxs-lookup"><span data-stu-id="c4915-103">Gets the migration status of the volume containers.</span></span>

## <span data-ttu-id="c4915-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4915-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> [-LegacyContainerNames <String[]>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c4915-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4915-105">DESCRIPTION</span></span>
<span data-ttu-id="c4915-106">Командлет **Get-AzureStorSimpleLegacyVolumeContainerStatus** получает состояние миграции контейнеров томов.</span><span class="sxs-lookup"><span data-stu-id="c4915-106">The **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet gets the migration status of the volume containers.</span></span>
<span data-ttu-id="c4915-107">Этот командлет возвращает сведения о состоянии, которые включают в том, что миграция контейнера тома по-прежнему выполняется, выполнена или завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="c4915-107">This cmdlet returns status information which includes whether the volume container migration is still in progress, completed, or failed.</span></span>

## <span data-ttu-id="c4915-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4915-108">EXAMPLES</span></span>

### <span data-ttu-id="c4915-109">Пример 1: получение состояния для неудачной миграции</span><span class="sxs-lookup"><span data-stu-id="c4915-109">Example 1: Get status for a failed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : No Cloud Configuration(s)  are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : Cloud Configuration Name: OneSDKAzureCloud
                       PercentageCompleted : 0
                       MigrationStatus : Failed
                       No Backup sets found
```

<span data-ttu-id="c4915-110">Эта команда возвращает состояние миграции для именованного контейнера прежних версий.</span><span class="sxs-lookup"><span data-stu-id="c4915-110">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="c4915-111">В результатах миграции показано, что миграция завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="c4915-111">The results show that the migration failed.</span></span>

### <span data-ttu-id="c4915-112">Пример 2: получение состояния для выполнения миграции</span><span class="sxs-lookup"><span data-stu-id="c4915-112">Example 2: Get status for a migration in progress</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : CloudConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 10
                       MigrationStatus : InProgress
                       BackupSets : 
                           Policy : OneSDKBackupPolicy, Status : InProgress
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="c4915-113">Эта команда возвращает состояние миграции для именованного контейнера прежних версий.</span><span class="sxs-lookup"><span data-stu-id="c4915-113">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="c4915-114">Результат показывает, что миграция выполняется.</span><span class="sxs-lookup"><span data-stu-id="c4915-114">The results show that the migration is in progress.</span></span>

### <span data-ttu-id="c4915-115">Пример 3: получение состояния для завершенной миграции</span><span class="sxs-lookup"><span data-stu-id="c4915-115">Example 3: Get status for a completed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4 -LegacyContainerNames OneSDKAzureCloud
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : Cloud ConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 100
                       MigrationStatus : Completed
                       BackupSets : 
                          Policy : vg1p1, Created On : 04/06/2015 11:22:00, Status : Completed
                          Policy : vg1p1, Created On : 03/30/2015 11:22:00, Status : Completed
                          Policy : c1v1-Auto-Daily-CloudSnapshot, Created On : 03/30/2015 03:30:00, Status : Completed
MigrationInprogress  : No Cloud Configuration(s) are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="c4915-116">Эта команда возвращает состояние миграции для именованного контейнера прежних версий.</span><span class="sxs-lookup"><span data-stu-id="c4915-116">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="c4915-117">Результат показывает, что миграция завершена.</span><span class="sxs-lookup"><span data-stu-id="c4915-117">The results show that the migration is completed.</span></span>

## <span data-ttu-id="c4915-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4915-118">PARAMETERS</span></span>

### <span data-ttu-id="c4915-119">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="c4915-119">-LegacyConfigId</span></span>
<span data-ttu-id="c4915-120">Указывает уникальный идентификатор конфигурации устаревшего устройства.</span><span class="sxs-lookup"><span data-stu-id="c4915-120">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="c4915-121">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="c4915-121">-LegacyContainerNames</span></span>
<span data-ttu-id="c4915-122">Указывает массив имен контейнеров томов, к которым применяется план миграции.</span><span class="sxs-lookup"><span data-stu-id="c4915-122">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4915-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="c4915-123">-Profile</span></span>
<span data-ttu-id="c4915-124">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="c4915-124">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="c4915-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4915-125">CommonParameters</span></span>
<span data-ttu-id="c4915-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4915-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4915-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4915-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4915-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4915-128">INPUTS</span></span>

## <span data-ttu-id="c4915-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4915-129">OUTPUTS</span></span>

## <span data-ttu-id="c4915-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4915-130">NOTES</span></span>

## <span data-ttu-id="c4915-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4915-131">RELATED LINKS</span></span>

[<span data-ttu-id="c4915-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="c4915-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="c4915-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="c4915-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)


