---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 2365b806bd274bb9cc18f84c83a29423408780d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732401"
---
# <span data-ttu-id="f253f-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f253f-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="f253f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f253f-102">SYNOPSIS</span></span>
<span data-ttu-id="f253f-103">Возвращает сведения о операции для текущего хранилища веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="f253f-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f253f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f253f-104">SYNTAX</span></span>

### <span data-ttu-id="f253f-105">ByParam (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f253f-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f253f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f253f-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f253f-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="f253f-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f253f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f253f-108">DESCRIPTION</span></span>
<span data-ttu-id="f253f-109">Командлет **Get-AzureRmSiteRecoveryJob** получает задания Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f253f-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="f253f-110">Вы можете использовать этот командлет, чтобы просмотреть сведения об операции для текущего хранилища сайта для восстановления.</span><span class="sxs-lookup"><span data-stu-id="f253f-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="f253f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f253f-111">EXAMPLES</span></span>

## <span data-ttu-id="f253f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f253f-112">PARAMETERS</span></span>

### <span data-ttu-id="f253f-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f253f-113">-EndTime</span></span>
<span data-ttu-id="f253f-114">Указывает время окончания для заданий.</span><span class="sxs-lookup"><span data-stu-id="f253f-114">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="f253f-115">Этот командлет получает все задания, которые были запущены до указанного времени.</span><span class="sxs-lookup"><span data-stu-id="f253f-115">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="f253f-116">Чтобы получить объект **DateTime** для этого параметра, используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="f253f-116">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="f253f-117">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f253f-117">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f253f-118">-Job</span><span class="sxs-lookup"><span data-stu-id="f253f-118">-Job</span></span>
<span data-ttu-id="f253f-119">Указывает задание восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="f253f-119">Specifies the Site Recovery job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f253f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f253f-120">-Name</span></span>
<span data-ttu-id="f253f-121">Задает уникальное имя, идентифицирующее задание.</span><span class="sxs-lookup"><span data-stu-id="f253f-121">Specifies a unique name that identifies the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f253f-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f253f-122">-StartTime</span></span>
<span data-ttu-id="f253f-123">Задает время начала для заданий.</span><span class="sxs-lookup"><span data-stu-id="f253f-123">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="f253f-124">Этот командлет получает все задания, которые были запущены по истечении заданного времени.</span><span class="sxs-lookup"><span data-stu-id="f253f-124">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f253f-125">-State</span><span class="sxs-lookup"><span data-stu-id="f253f-125">-State</span></span>
<span data-ttu-id="f253f-126">Задает состояние ввода для задания по восстановлению сайта.</span><span class="sxs-lookup"><span data-stu-id="f253f-126">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="f253f-127">Этот командлет получает все задания, которые соответствуют указанному состоянию.</span><span class="sxs-lookup"><span data-stu-id="f253f-127">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="f253f-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f253f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f253f-129">NotStarted</span><span class="sxs-lookup"><span data-stu-id="f253f-129">NotStarted</span></span>
- <span data-ttu-id="f253f-130">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="f253f-130">InProgress</span></span>
- <span data-ttu-id="f253f-131">LSP</span><span class="sxs-lookup"><span data-stu-id="f253f-131">Succeeded</span></span>
- <span data-ttu-id="f253f-132">Другие</span><span class="sxs-lookup"><span data-stu-id="f253f-132">Other</span></span>
- <span data-ttu-id="f253f-133">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="f253f-133">Failed</span></span>
- <span data-ttu-id="f253f-134">Отменен</span><span class="sxs-lookup"><span data-stu-id="f253f-134">Cancelled</span></span>
- <span data-ttu-id="f253f-135">Остановить</span><span class="sxs-lookup"><span data-stu-id="f253f-135">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f253f-136">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="f253f-136">-TargetObjectId</span></span>
<span data-ttu-id="f253f-137">Указывает идентификатор объекта, для которого задано задание.</span><span class="sxs-lookup"><span data-stu-id="f253f-137">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f253f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f253f-138">-DefaultProfile</span></span>
<span data-ttu-id="f253f-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f253f-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f253f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f253f-140">CommonParameters</span></span>
<span data-ttu-id="f253f-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f253f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f253f-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f253f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f253f-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f253f-143">INPUTS</span></span>

### <span data-ttu-id="f253f-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="f253f-144">ASRJob</span></span>
<span data-ttu-id="f253f-145">Параметр "задание" принимает значение типа "ASRJob" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f253f-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="f253f-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f253f-146">OUTPUTS</span></span>

### <span data-ttu-id="f253f-147">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="f253f-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="f253f-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="f253f-148">NOTES</span></span>

## <span data-ttu-id="f253f-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f253f-149">RELATED LINKS</span></span>

[<span data-ttu-id="f253f-150">Restarting-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f253f-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="f253f-151">Возобновить — AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f253f-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="f253f-152">Остановить-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="f253f-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
