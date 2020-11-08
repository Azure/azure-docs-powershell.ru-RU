---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075773"
---
# <span data-ttu-id="5f62e-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="5f62e-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="5f62e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f62e-102">SYNOPSIS</span></span>
<span data-ttu-id="5f62e-103">Начало создания плана миграции.</span><span class="sxs-lookup"><span data-stu-id="5f62e-103">Starts the creation of a migration plan.</span></span>

## <span data-ttu-id="5f62e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f62e-104">SYNTAX</span></span>

### <span data-ttu-id="5f62e-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="5f62e-105">MigrateSpecificContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5f62e-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="5f62e-106">MigrateAllContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5f62e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f62e-107">DESCRIPTION</span></span>
<span data-ttu-id="5f62e-108">Командлет **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** запускает создание плана миграции.</span><span class="sxs-lookup"><span data-stu-id="5f62e-108">The **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet starts the creation of a migration plan.</span></span>
<span data-ttu-id="5f62e-109">Создание плана миграции выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="5f62e-109">The creation of a migration plan is asynchronous.</span></span>
<span data-ttu-id="5f62e-110">Чтобы просмотреть состояние плана миграции, используйте командлет **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** .</span><span class="sxs-lookup"><span data-stu-id="5f62e-110">To see the status of the migration plan, use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet.</span></span>

## <span data-ttu-id="5f62e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f62e-111">EXAMPLES</span></span>

### <span data-ttu-id="5f62e-112">Пример 1: запуск плана миграции</span><span class="sxs-lookup"><span data-stu-id="5f62e-112">Example 1: Start a migration plan</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="5f62e-113">Эта команда запускает создание плана миграции для устаревшего контейнера с именем OneSDKAzureCloud.</span><span class="sxs-lookup"><span data-stu-id="5f62e-113">This command starts creation of a migration plan for the legacy container named OneSDKAzureCloud.</span></span>
<span data-ttu-id="5f62e-114">Команда возвращает сообщение о состоянии плана и использование командлета **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** для получения актуальной информации.</span><span class="sxs-lookup"><span data-stu-id="5f62e-114">The command returns a message about the status of the plan, and to use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet for up to date information.</span></span>

### <span data-ttu-id="5f62e-115">Пример 2: запуск плана миграции для всех контейнеров томов</span><span class="sxs-lookup"><span data-stu-id="5f62e-115">Example 2: Start migration plan for all volume containers</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="5f62e-116">Эта команда запускает создание плана миграции для всех устаревших контейнеров томов в импортируемом файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5f62e-116">This command starts creation of migration plan for all legacy volume containers in the configuration file that is imported.</span></span>

## <span data-ttu-id="5f62e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f62e-117">PARAMETERS</span></span>

### <span data-ttu-id="5f62e-118">-ALL</span><span class="sxs-lookup"><span data-stu-id="5f62e-118">-All</span></span>
<span data-ttu-id="5f62e-119">Указывает на то, что этот командлет запускает оценку времени миграции для всех контейнеров томов в импортированном файле конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5f62e-119">Indicates that this cmdlet starts migration time estimates for all volume containers in the imported configuration file.</span></span>

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

### <span data-ttu-id="5f62e-120">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="5f62e-120">-LegacyConfigId</span></span>
<span data-ttu-id="5f62e-121">Указывает уникальный идентификатор конфигурации устаревшего устройства.</span><span class="sxs-lookup"><span data-stu-id="5f62e-121">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="5f62e-122">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="5f62e-122">-LegacyContainerNames</span></span>
<span data-ttu-id="5f62e-123">Указывает массив имен контейнеров томов, для которых нужно создать план миграции.</span><span class="sxs-lookup"><span data-stu-id="5f62e-123">Specifies an array of volume container names for which to create a migration plan.</span></span>

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

### <span data-ttu-id="5f62e-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="5f62e-124">-Profile</span></span>
<span data-ttu-id="5f62e-125">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5f62e-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5f62e-126">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f62e-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5f62e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f62e-127">CommonParameters</span></span>
<span data-ttu-id="5f62e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f62e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f62e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f62e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f62e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f62e-130">INPUTS</span></span>

### <span data-ttu-id="5f62e-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="5f62e-131">None</span></span>

## <span data-ttu-id="5f62e-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f62e-132">OUTPUTS</span></span>

### <span data-ttu-id="5f62e-133">Подстрок</span><span class="sxs-lookup"><span data-stu-id="5f62e-133">String</span></span>
<span data-ttu-id="5f62e-134">Этот командлет возвращает состояние задания плана миграции, если оно было успешно запущено на устройстве.</span><span class="sxs-lookup"><span data-stu-id="5f62e-134">This cmdlet returns the status of the migration plan job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="5f62e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f62e-135">NOTES</span></span>

## <span data-ttu-id="5f62e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f62e-136">RELATED LINKS</span></span>

[<span data-ttu-id="5f62e-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="5f62e-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


