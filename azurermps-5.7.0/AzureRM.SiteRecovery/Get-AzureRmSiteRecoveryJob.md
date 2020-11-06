---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: dc8a1e6cfe8c3d68af0f8c413a0e96cac9feaee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566094"
---
# <span data-ttu-id="92027-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="92027-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="92027-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="92027-102">SYNOPSIS</span></span>
<span data-ttu-id="92027-103">Возвращает сведения о операции для текущего хранилища веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="92027-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92027-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="92027-104">SYNTAX</span></span>

### <span data-ttu-id="92027-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92027-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92027-106">ByName</span><span class="sxs-lookup"><span data-stu-id="92027-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92027-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="92027-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92027-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92027-108">DESCRIPTION</span></span>
<span data-ttu-id="92027-109">Командлет **Get-AzureRmSiteRecoveryJob** получает задания Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="92027-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="92027-110">Вы можете использовать этот командлет, чтобы просмотреть сведения об операции для текущего хранилища сайта для восстановления.</span><span class="sxs-lookup"><span data-stu-id="92027-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="92027-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="92027-111">EXAMPLES</span></span>

## <span data-ttu-id="92027-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="92027-112">PARAMETERS</span></span>

### <span data-ttu-id="92027-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92027-113">-DefaultProfile</span></span>
<span data-ttu-id="92027-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92027-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92027-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="92027-115">-EndTime</span></span>
<span data-ttu-id="92027-116">Указывает время окончания для заданий.</span><span class="sxs-lookup"><span data-stu-id="92027-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="92027-117">Этот командлет получает все задания, которые были запущены до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="92027-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="92027-118">Чтобы получить объект **DateTime** для этого параметра, используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="92027-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="92027-119">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="92027-119">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92027-120">-Job</span><span class="sxs-lookup"><span data-stu-id="92027-120">-Job</span></span>
<span data-ttu-id="92027-121">Указывает задание восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="92027-121">Specifies the Site Recovery job.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92027-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="92027-122">-Name</span></span>
<span data-ttu-id="92027-123">Задает уникальное имя, идентифицирующее задание.</span><span class="sxs-lookup"><span data-stu-id="92027-123">Specifies a unique name that identifies the job.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92027-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="92027-124">-StartTime</span></span>
<span data-ttu-id="92027-125">Задает время начала для заданий.</span><span class="sxs-lookup"><span data-stu-id="92027-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="92027-126">Этот командлет получает все задания, которые были запущены по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="92027-126">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92027-127">-State</span><span class="sxs-lookup"><span data-stu-id="92027-127">-State</span></span>
<span data-ttu-id="92027-128">Задает состояние ввода для задания по восстановлению сайта.</span><span class="sxs-lookup"><span data-stu-id="92027-128">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="92027-129">Этот командлет получает все задания, которые соответствуют указанному состоянию.</span><span class="sxs-lookup"><span data-stu-id="92027-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="92027-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="92027-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="92027-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="92027-131">NotStarted</span></span>
- <span data-ttu-id="92027-132">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="92027-132">InProgress</span></span>
- <span data-ttu-id="92027-133">LSP</span><span class="sxs-lookup"><span data-stu-id="92027-133">Succeeded</span></span>
- <span data-ttu-id="92027-134">Другие</span><span class="sxs-lookup"><span data-stu-id="92027-134">Other</span></span>
- <span data-ttu-id="92027-135">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="92027-135">Failed</span></span>
- <span data-ttu-id="92027-136">Отменен</span><span class="sxs-lookup"><span data-stu-id="92027-136">Cancelled</span></span>
- <span data-ttu-id="92027-137">Остановить</span><span class="sxs-lookup"><span data-stu-id="92027-137">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92027-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="92027-138">-TargetObjectId</span></span>
<span data-ttu-id="92027-139">Указывает идентификатор объекта, для которого задано задание.</span><span class="sxs-lookup"><span data-stu-id="92027-139">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92027-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92027-140">CommonParameters</span></span>
<span data-ttu-id="92027-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="92027-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92027-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92027-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92027-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="92027-143">INPUTS</span></span>

### <span data-ttu-id="92027-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="92027-144">ASRJob</span></span>
<span data-ttu-id="92027-145">Параметр "задание" принимает значение типа "ASRJob" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="92027-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="92027-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="92027-146">OUTPUTS</span></span>

### <span data-ttu-id="92027-147">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="92027-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="92027-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="92027-148">NOTES</span></span>

## <span data-ttu-id="92027-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92027-149">RELATED LINKS</span></span>

[<span data-ttu-id="92027-150">Restarting-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="92027-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="92027-151">Возобновить — AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="92027-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="92027-152">Остановить-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="92027-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
