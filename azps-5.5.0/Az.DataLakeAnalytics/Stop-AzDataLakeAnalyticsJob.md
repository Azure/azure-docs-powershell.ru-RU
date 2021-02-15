---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228804"
---
# <span data-ttu-id="77993-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="77993-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="77993-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77993-102">SYNOPSIS</span></span>
<span data-ttu-id="77993-103">Отмена задания.</span><span class="sxs-lookup"><span data-stu-id="77993-103">Cancels a job.</span></span>

## <span data-ttu-id="77993-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="77993-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77993-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77993-105">DESCRIPTION</span></span>
<span data-ttu-id="77993-106">Для отмены задания Azure Data Lake Analytics будет отменено задание **Stop-AzDataLakeAnalyticsJob.**</span><span class="sxs-lookup"><span data-stu-id="77993-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="77993-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="77993-107">EXAMPLES</span></span>

### <span data-ttu-id="77993-108">Пример 1. Отмена задания</span><span class="sxs-lookup"><span data-stu-id="77993-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="77993-109">Эта команда отменяет задание с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="77993-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="77993-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77993-110">PARAMETERS</span></span>

### <span data-ttu-id="77993-111">-Account</span><span class="sxs-lookup"><span data-stu-id="77993-111">-Account</span></span>
<span data-ttu-id="77993-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="77993-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="77993-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77993-113">-DefaultProfile</span></span>
<span data-ttu-id="77993-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="77993-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77993-115">-Force</span><span class="sxs-lookup"><span data-stu-id="77993-115">-Force</span></span>
<span data-ttu-id="77993-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="77993-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="77993-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="77993-117">-JobId</span></span>
<span data-ttu-id="77993-118">Определяет ИД отменяемого задания.</span><span class="sxs-lookup"><span data-stu-id="77993-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="77993-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77993-119">-PassThru</span></span>
<span data-ttu-id="77993-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="77993-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="77993-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="77993-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="77993-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77993-122">-Confirm</span></span>
<span data-ttu-id="77993-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77993-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77993-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77993-124">-WhatIf</span></span>
<span data-ttu-id="77993-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77993-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77993-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="77993-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77993-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77993-127">CommonParameters</span></span>
<span data-ttu-id="77993-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77993-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77993-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77993-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77993-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77993-130">INPUTS</span></span>

### <span data-ttu-id="77993-131">System.String</span><span class="sxs-lookup"><span data-stu-id="77993-131">System.String</span></span>

### <span data-ttu-id="77993-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="77993-132">System.Guid</span></span>

### <span data-ttu-id="77993-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="77993-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="77993-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77993-134">OUTPUTS</span></span>

### <span data-ttu-id="77993-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77993-135">System.Boolean</span></span>

## <span data-ttu-id="77993-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="77993-136">NOTES</span></span>

## <span data-ttu-id="77993-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77993-137">RELATED LINKS</span></span>

[<span data-ttu-id="77993-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="77993-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="77993-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="77993-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="77993-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="77993-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


