---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: a0848ffc888b4812a28198749417d0b0894a5d98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734565"
---
# <span data-ttu-id="524bc-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="524bc-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="524bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="524bc-102">SYNOPSIS</span></span>
<span data-ttu-id="524bc-103">Отменяет задание.</span><span class="sxs-lookup"><span data-stu-id="524bc-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="524bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="524bc-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="524bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="524bc-105">DESCRIPTION</span></span>
<span data-ttu-id="524bc-106">Командлет **Stop-AzureRmDataLakeAnalyticsJob** отменяет задание Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="524bc-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="524bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="524bc-107">EXAMPLES</span></span>

### <span data-ttu-id="524bc-108">Пример 1: Отмена задания</span><span class="sxs-lookup"><span data-stu-id="524bc-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="524bc-109">Эта команда отменяет задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="524bc-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="524bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="524bc-110">PARAMETERS</span></span>

### <span data-ttu-id="524bc-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="524bc-111">-Account</span></span>
<span data-ttu-id="524bc-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="524bc-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="524bc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="524bc-113">-Force</span></span>
<span data-ttu-id="524bc-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="524bc-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="524bc-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="524bc-115">-JobId</span></span>
<span data-ttu-id="524bc-116">Указывает идентификатор задания, которое нужно отменить.</span><span class="sxs-lookup"><span data-stu-id="524bc-116">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="524bc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="524bc-117">-PassThru</span></span>
<span data-ttu-id="524bc-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="524bc-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="524bc-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="524bc-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="524bc-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="524bc-120">-Confirm</span></span>
<span data-ttu-id="524bc-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="524bc-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="524bc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="524bc-122">-WhatIf</span></span>
<span data-ttu-id="524bc-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="524bc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="524bc-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="524bc-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="524bc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="524bc-125">-DefaultProfile</span></span>
<span data-ttu-id="524bc-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="524bc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="524bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="524bc-127">CommonParameters</span></span>
<span data-ttu-id="524bc-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="524bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="524bc-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="524bc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="524bc-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="524bc-130">INPUTS</span></span>

### <span data-ttu-id="524bc-131">GUID</span><span class="sxs-lookup"><span data-stu-id="524bc-131">Guid</span></span>
<span data-ttu-id="524bc-132">Параметр "JobId" принимает значение типа "GUID" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="524bc-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="524bc-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="524bc-133">OUTPUTS</span></span>

### <span data-ttu-id="524bc-134">логических</span><span class="sxs-lookup"><span data-stu-id="524bc-134">bool</span></span>
<span data-ttu-id="524bc-135">Если указана функция PassThru, возвращает значение истина после завершения операции.</span><span class="sxs-lookup"><span data-stu-id="524bc-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="524bc-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="524bc-136">NOTES</span></span>

## <span data-ttu-id="524bc-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="524bc-137">RELATED LINKS</span></span>

[<span data-ttu-id="524bc-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="524bc-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="524bc-139">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="524bc-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="524bc-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="524bc-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


