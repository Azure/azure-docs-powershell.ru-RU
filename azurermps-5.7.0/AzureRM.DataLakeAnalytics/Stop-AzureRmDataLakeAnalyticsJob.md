---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/stop-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 956e263f402a3b6cb78631f8337d46fc1effdd98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563572"
---
# <span data-ttu-id="6030a-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6030a-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="6030a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6030a-102">SYNOPSIS</span></span>
<span data-ttu-id="6030a-103">Отменяет задание.</span><span class="sxs-lookup"><span data-stu-id="6030a-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6030a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6030a-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6030a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6030a-105">DESCRIPTION</span></span>
<span data-ttu-id="6030a-106">Командлет **Stop-AzureRmDataLakeAnalyticsJob** отменяет задание Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6030a-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="6030a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6030a-107">EXAMPLES</span></span>

### <span data-ttu-id="6030a-108">Пример 1: Отмена задания</span><span class="sxs-lookup"><span data-stu-id="6030a-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="6030a-109">Эта команда отменяет задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="6030a-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="6030a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6030a-110">PARAMETERS</span></span>

### <span data-ttu-id="6030a-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6030a-111">-Account</span></span>
<span data-ttu-id="6030a-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6030a-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6030a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6030a-113">-DefaultProfile</span></span>
<span data-ttu-id="6030a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6030a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6030a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6030a-115">-Force</span></span>
<span data-ttu-id="6030a-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6030a-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6030a-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="6030a-117">-JobId</span></span>
<span data-ttu-id="6030a-118">Указывает идентификатор задания, которое нужно отменить.</span><span class="sxs-lookup"><span data-stu-id="6030a-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6030a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6030a-119">-PassThru</span></span>
<span data-ttu-id="6030a-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="6030a-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6030a-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6030a-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6030a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6030a-122">-Confirm</span></span>
<span data-ttu-id="6030a-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6030a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6030a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6030a-124">-WhatIf</span></span>
<span data-ttu-id="6030a-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6030a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6030a-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6030a-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6030a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6030a-127">CommonParameters</span></span>
<span data-ttu-id="6030a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6030a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6030a-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6030a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6030a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6030a-130">INPUTS</span></span>

### <span data-ttu-id="6030a-131">GUID</span><span class="sxs-lookup"><span data-stu-id="6030a-131">Guid</span></span>
<span data-ttu-id="6030a-132">Параметр "JobId" принимает значение типа "GUID" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="6030a-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="6030a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6030a-133">OUTPUTS</span></span>

### <span data-ttu-id="6030a-134">логических</span><span class="sxs-lookup"><span data-stu-id="6030a-134">bool</span></span>
<span data-ttu-id="6030a-135">Если указана функция PassThru, возвращает значение истина после завершения операции.</span><span class="sxs-lookup"><span data-stu-id="6030a-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="6030a-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="6030a-136">NOTES</span></span>

## <span data-ttu-id="6030a-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6030a-137">RELATED LINKS</span></span>

[<span data-ttu-id="6030a-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6030a-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="6030a-139">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6030a-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="6030a-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6030a-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


