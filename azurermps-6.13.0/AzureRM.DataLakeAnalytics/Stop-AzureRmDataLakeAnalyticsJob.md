---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/stop-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 4fc5c20cf43fbafb89007328307c69d4820b2127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732962"
---
# <span data-ttu-id="0ffc8-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0ffc8-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="0ffc8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ffc8-102">SYNOPSIS</span></span>
<span data-ttu-id="0ffc8-103">Отменяет задание.</span><span class="sxs-lookup"><span data-stu-id="0ffc8-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ffc8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ffc8-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ffc8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ffc8-105">DESCRIPTION</span></span>
<span data-ttu-id="0ffc8-106">Командлет **Stop-AzureRmDataLakeAnalyticsJob** отменяет задание Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0ffc8-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="0ffc8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ffc8-107">EXAMPLES</span></span>

### <span data-ttu-id="0ffc8-108">Пример 1: Отмена задания</span><span class="sxs-lookup"><span data-stu-id="0ffc8-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="0ffc8-109">Эта команда отменяет задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="0ffc8-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="0ffc8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ffc8-110">PARAMETERS</span></span>

### <span data-ttu-id="0ffc8-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="0ffc8-111">-Account</span></span>
<span data-ttu-id="0ffc8-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="0ffc8-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="0ffc8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ffc8-113">-DefaultProfile</span></span>
<span data-ttu-id="0ffc8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0ffc8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ffc8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0ffc8-115">-Force</span></span>
<span data-ttu-id="0ffc8-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0ffc8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0ffc8-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="0ffc8-117">-JobId</span></span>
<span data-ttu-id="0ffc8-118">Указывает идентификатор задания, которое нужно отменить.</span><span class="sxs-lookup"><span data-stu-id="0ffc8-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="0ffc8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ffc8-119">-PassThru</span></span>
<span data-ttu-id="0ffc8-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="0ffc8-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0ffc8-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0ffc8-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0ffc8-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ffc8-122">-Confirm</span></span>
<span data-ttu-id="0ffc8-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0ffc8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ffc8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ffc8-124">-WhatIf</span></span>
<span data-ttu-id="0ffc8-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0ffc8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ffc8-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0ffc8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ffc8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ffc8-127">CommonParameters</span></span>
<span data-ttu-id="0ffc8-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ffc8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ffc8-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ffc8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ffc8-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ffc8-130">INPUTS</span></span>

### <span data-ttu-id="0ffc8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0ffc8-131">System.String</span></span>

### <span data-ttu-id="0ffc8-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="0ffc8-132">System.Guid</span></span>

### <span data-ttu-id="0ffc8-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0ffc8-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0ffc8-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ffc8-134">OUTPUTS</span></span>

### <span data-ttu-id="0ffc8-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0ffc8-135">System.Boolean</span></span>

## <span data-ttu-id="0ffc8-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ffc8-136">NOTES</span></span>

## <span data-ttu-id="0ffc8-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ffc8-137">RELATED LINKS</span></span>

[<span data-ttu-id="0ffc8-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0ffc8-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="0ffc8-139">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0ffc8-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="0ffc8-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0ffc8-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


