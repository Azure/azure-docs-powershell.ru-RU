---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 3B4630C1-9885-4BE4-B41E-D98AF5CCD7C3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185072d1bc0d0895d4b6cfaea9470bac107d651a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076553"
---
# <span data-ttu-id="2f36f-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="2f36f-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>

## <span data-ttu-id="2f36f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f36f-102">SYNOPSIS</span></span>
<span data-ttu-id="2f36f-103">Получает состояние операции фиксации или отката.</span><span class="sxs-lookup"><span data-stu-id="2f36f-103">Gets the status of a commit or rollback operation.</span></span>

## <span data-ttu-id="2f36f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f36f-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId <String>
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2f36f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f36f-105">DESCRIPTION</span></span>
<span data-ttu-id="2f36f-106">Командлет **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** получает состояние операции фиксации или отката.</span><span class="sxs-lookup"><span data-stu-id="2f36f-106">The **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** cmdlet gets the status of the commit or rollback operation.</span></span>

## <span data-ttu-id="2f36f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f36f-107">EXAMPLES</span></span>

### <span data-ttu-id="2f36f-108">Пример 1: получение состояния завершенной операции фиксации</span><span class="sxs-lookup"><span data-stu-id="2f36f-108">Example 1: Get the status of a completed commit operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Commit
                             PercentageCompleted    : 100
                             Messages               : 

CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : None
RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="2f36f-109">Эта команда возвращает состояние операции фиксации для именованного контейнера.</span><span class="sxs-lookup"><span data-stu-id="2f36f-109">This command gets the status of a commit operation for the named container.</span></span>
<span data-ttu-id="2f36f-110">У этой операции есть состояние "завершено".</span><span class="sxs-lookup"><span data-stu-id="2f36f-110">This operation has a status of completed.</span></span>

### <span data-ttu-id="2f36f-111">Пример 2: получение состояния завершенной операции отката</span><span class="sxs-lookup"><span data-stu-id="2f36f-111">Example 2: Get the status of a completed rollback operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : None
CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Rollback
                             PercentageCompleted    : 100
                             Messages               : 

RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="2f36f-112">Эта команда возвращает состояние операции отката для именованного контейнера.</span><span class="sxs-lookup"><span data-stu-id="2f36f-112">This command gets the status of a rollback operation for the named container.</span></span>
<span data-ttu-id="2f36f-113">У этой операции есть состояние "завершено".</span><span class="sxs-lookup"><span data-stu-id="2f36f-113">This operation has a status of completed.</span></span>

## <span data-ttu-id="2f36f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f36f-114">PARAMETERS</span></span>

### <span data-ttu-id="2f36f-115">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="2f36f-115">-LegacyConfigId</span></span>
<span data-ttu-id="2f36f-116">Указывает уникальный идентификатор конфигурации устаревшего устройства.</span><span class="sxs-lookup"><span data-stu-id="2f36f-116">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="2f36f-117">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="2f36f-117">-LegacyContainerNames</span></span>
<span data-ttu-id="2f36f-118">Указывает массив имен контейнеров томов, к которым применяется план миграции.</span><span class="sxs-lookup"><span data-stu-id="2f36f-118">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="2f36f-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="2f36f-119">-Profile</span></span>
<span data-ttu-id="2f36f-120">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="2f36f-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="2f36f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f36f-121">CommonParameters</span></span>
<span data-ttu-id="2f36f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f36f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f36f-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f36f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f36f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f36f-124">INPUTS</span></span>

### <span data-ttu-id="2f36f-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="2f36f-125">None</span></span>

## <span data-ttu-id="2f36f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f36f-126">OUTPUTS</span></span>

### <span data-ttu-id="2f36f-127">ConfirmMigrationStatusMsg</span><span class="sxs-lookup"><span data-stu-id="2f36f-127">ConfirmMigrationStatusMsg</span></span>
<span data-ttu-id="2f36f-128">Этот командлет возвращает состояние выполняемой операции подтверждения миграции.</span><span class="sxs-lookup"><span data-stu-id="2f36f-128">This cmdlet returns the status of the confirm migration operation that is performed.</span></span>

## <span data-ttu-id="2f36f-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f36f-129">NOTES</span></span>

## <span data-ttu-id="2f36f-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f36f-130">RELATED LINKS</span></span>

[<span data-ttu-id="2f36f-131">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="2f36f-131">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="2f36f-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="2f36f-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

