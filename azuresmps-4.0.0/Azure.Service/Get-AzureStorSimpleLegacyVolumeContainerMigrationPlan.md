---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075556"
---
# <span data-ttu-id="00981-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="00981-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="00981-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00981-102">SYNOPSIS</span></span>
<span data-ttu-id="00981-103">Возвращает планы миграции для устаревших контейнеров.</span><span class="sxs-lookup"><span data-stu-id="00981-103">Gets migration plans for legacy containers.</span></span>

## <span data-ttu-id="00981-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00981-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00981-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00981-105">DESCRIPTION</span></span>
<span data-ttu-id="00981-106">Командлет **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** получает планы миграции для устаревших контейнеров.</span><span class="sxs-lookup"><span data-stu-id="00981-106">The **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet gets migration plans for legacy containers.</span></span>
<span data-ttu-id="00981-107">Укажите план миграции по его устаревшему ИД конфигурации.</span><span class="sxs-lookup"><span data-stu-id="00981-107">Specify a migration plan by its legacy configuration ID.</span></span>
<span data-ttu-id="00981-108">Если создание плана миграции еще не завершено, этот командлет получает состояние плана миграции.</span><span class="sxs-lookup"><span data-stu-id="00981-108">If creation of the migration plan is still in progress, this cmdlet gets the status of the migration plan.</span></span>
<span data-ttu-id="00981-109">Если план миграции завершен, этот командлет возвращает реальный план миграции для набора устаревших контейнеров.</span><span class="sxs-lookup"><span data-stu-id="00981-109">If the migration plan is completed, this cmdlet returns the actual migration plan for the set of legacy containers.</span></span>
<span data-ttu-id="00981-110">Если параметр *LegacyConfigId* не указан, этот командлет возвращает список идентификаторов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="00981-110">If you do not specify the *LegacyConfigId* parameter, this cmdlet returns a list of configuration IDs.</span></span>

## <span data-ttu-id="00981-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00981-111">EXAMPLES</span></span>

### <span data-ttu-id="00981-112">Пример 1: получение состояния плана</span><span class="sxs-lookup"><span data-stu-id="00981-112">Example 1: Get the status of a plan</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

<span data-ttu-id="00981-113">Эта команда возвращает состояние плана миграции.</span><span class="sxs-lookup"><span data-stu-id="00981-113">This command gets the status of the migration plan.</span></span>
<span data-ttu-id="00981-114">Этот статус включает предполагаемую пропускную способность, предполагаемое время и связанную информацию.</span><span class="sxs-lookup"><span data-stu-id="00981-114">The status includes assumed bandwidth, estimated time and, related information.</span></span>

### <span data-ttu-id="00981-115">Пример 2: получение идентификаторов существующих планов</span><span class="sxs-lookup"><span data-stu-id="00981-115">Example 2: Get the IDs of existing plans</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

<span data-ttu-id="00981-116">Эта команда получает все идентификаторы конфигурации планов миграции.</span><span class="sxs-lookup"><span data-stu-id="00981-116">This command gets all the configuration IDs of migration plans.</span></span>

## <span data-ttu-id="00981-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00981-117">PARAMETERS</span></span>

### <span data-ttu-id="00981-118">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="00981-118">-LegacyConfigId</span></span>
<span data-ttu-id="00981-119">Указывает уникальный идентификатор конфигурации устаревшего устройства.</span><span class="sxs-lookup"><span data-stu-id="00981-119">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="00981-120">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="00981-120">-LegacyContainerNames</span></span>
<span data-ttu-id="00981-121">Указывает массив имен контейнеров томов, для которых этот командлет получает план миграции.</span><span class="sxs-lookup"><span data-stu-id="00981-121">Specifies an array of volume container names for which this cmdlet gets a migration plan.</span></span>

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

### <span data-ttu-id="00981-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="00981-122">-Profile</span></span>
<span data-ttu-id="00981-123">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="00981-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="00981-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00981-124">CommonParameters</span></span>
<span data-ttu-id="00981-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00981-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00981-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00981-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00981-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00981-127">INPUTS</span></span>

### <span data-ttu-id="00981-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="00981-128">None</span></span>

## <span data-ttu-id="00981-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00981-129">OUTPUTS</span></span>

### <span data-ttu-id="00981-130">MigrationPlanMsg</span><span class="sxs-lookup"><span data-stu-id="00981-130">MigrationPlanMsg</span></span>
<span data-ttu-id="00981-131">Этот командлет возвращает объект **MigrationPlanMsg** , содержащий состояние задания плана миграции, предполагаемая пропускная способность в мегабит в секунду и предполагаемое время в минутах.</span><span class="sxs-lookup"><span data-stu-id="00981-131">This cmdlet returns a **MigrationPlanMsg** object that contains the status of the migration plan job, assumed bandwidth in megabits per second, and estimated time in minutes.</span></span>

## <span data-ttu-id="00981-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="00981-132">NOTES</span></span>

## <span data-ttu-id="00981-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00981-133">RELATED LINKS</span></span>

[<span data-ttu-id="00981-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="00981-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


