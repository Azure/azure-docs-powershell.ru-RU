---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076258"
---
# <span data-ttu-id="c0492-101">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="c0492-101">Import-AzureStorSimpleLegacyVolumeContainer</span></span>

## <span data-ttu-id="c0492-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0492-102">SYNOPSIS</span></span>
<span data-ttu-id="c0492-103">Запускает миграцию контейнеров томов.</span><span class="sxs-lookup"><span data-stu-id="c0492-103">Starts the migration of volume containers.</span></span>

## <span data-ttu-id="c0492-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0492-104">SYNTAX</span></span>

### <span data-ttu-id="c0492-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="c0492-105">MigrateSpecificContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c0492-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="c0492-106">MigrateAllContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c0492-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0492-107">DESCRIPTION</span></span>
<span data-ttu-id="c0492-108">Командлет **Import-AzureStorSimpleLegacyVolumeContainer** запускает миграцию контейнеров томов из устаревшего устройства в целевое устройство.</span><span class="sxs-lookup"><span data-stu-id="c0492-108">The **Import-AzureStorSimpleLegacyVolumeContainer** cmdlet starts the migration of volume containers from a legacy appliance to the target appliance.</span></span>

## <span data-ttu-id="c0492-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0492-109">EXAMPLES</span></span>

### <span data-ttu-id="c0492-110">Пример 1: Импорт контейнера тома с устаревшим набором томов</span><span class="sxs-lookup"><span data-stu-id="c0492-110">Example 1: Import a legacy volume container</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="c0492-111">Эта команда импортирует устаревший контейнер тома для именованного контейнера.</span><span class="sxs-lookup"><span data-stu-id="c0492-111">This command imports a legacy volume container for the named container.</span></span>
<span data-ttu-id="c0492-112">Командлет запускает импорт и возвращает сообщение.</span><span class="sxs-lookup"><span data-stu-id="c0492-112">The cmdlet starts the import, and then returns a message.</span></span>

### <span data-ttu-id="c0492-113">Пример 2: импорт всех устаревших контейнеров томов</span><span class="sxs-lookup"><span data-stu-id="c0492-113">Example 2: Import all legacy volume containers</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="c0492-114">Эта команда импортирует все старые контейнеры томов из файла конфигурации импортированы.</span><span class="sxs-lookup"><span data-stu-id="c0492-114">This command imports all legacy volume containers from configuration file imported.</span></span>
<span data-ttu-id="c0492-115">Командлет запускает импорт и возвращает сообщение.</span><span class="sxs-lookup"><span data-stu-id="c0492-115">The cmdlet starts the import, and then returns a message.</span></span>

## <span data-ttu-id="c0492-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0492-116">PARAMETERS</span></span>

### <span data-ttu-id="c0492-117">-ALL</span><span class="sxs-lookup"><span data-stu-id="c0492-117">-All</span></span>
<span data-ttu-id="c0492-118">Указывает на то, что этот командлет импортирует все контейнеры томов в импортированном файле конфигурации на целевое устройство.</span><span class="sxs-lookup"><span data-stu-id="c0492-118">Indicates that this cmdlet imports all volume containers in the imported configuration file to the target device.</span></span>

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

### <span data-ttu-id="c0492-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c0492-119">-Force</span></span>
<span data-ttu-id="c0492-120">Указывает на то, что этот командлет импортирует контейнер томов на другом устройстве, даже если контейнер томов импортирован на другое устройство.</span><span class="sxs-lookup"><span data-stu-id="c0492-120">Indicates that this cmdlet imports volume container on a different device, even if volume container has been imported on a different device.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0492-121">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="c0492-121">-LegacyConfigId</span></span>
<span data-ttu-id="c0492-122">Указывает уникальный идентификатор конфигурации устаревшего устройства.</span><span class="sxs-lookup"><span data-stu-id="c0492-122">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="c0492-123">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="c0492-123">-LegacyContainerNames</span></span>
<span data-ttu-id="c0492-124">Указывает массив имен контейнеров томов, к которым применяется план миграции.</span><span class="sxs-lookup"><span data-stu-id="c0492-124">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="c0492-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="c0492-125">-Profile</span></span>
<span data-ttu-id="c0492-126">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c0492-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c0492-127">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c0492-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c0492-128">-SkipACRs</span><span class="sxs-lookup"><span data-stu-id="c0492-128">-SkipACRs</span></span>
<span data-ttu-id="c0492-129">Указывает на то, что процесс импорта пропускает записи управления доступом для миграции.</span><span class="sxs-lookup"><span data-stu-id="c0492-129">Indicates that the import process skips access control records for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0492-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0492-130">CommonParameters</span></span>
<span data-ttu-id="c0492-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0492-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0492-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0492-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0492-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0492-133">INPUTS</span></span>

## <span data-ttu-id="c0492-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0492-134">OUTPUTS</span></span>

### <span data-ttu-id="c0492-135">Подстрок</span><span class="sxs-lookup"><span data-stu-id="c0492-135">String</span></span>
<span data-ttu-id="c0492-136">Эта команда возвращает состояние задания контейнера тома импорта миграции, если оно было успешно запущено на устройстве.</span><span class="sxs-lookup"><span data-stu-id="c0492-136">This command returns the status of the migration import volume container job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="c0492-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0492-137">NOTES</span></span>

## <span data-ttu-id="c0492-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0492-138">RELATED LINKS</span></span>

[<span data-ttu-id="c0492-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="c0492-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="c0492-140">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="c0492-140">Import-AzureStorSimpleLegacyApplianceConfig</span></span>](./Import-AzureStorSimpleLegacyApplianceConfig.md)


