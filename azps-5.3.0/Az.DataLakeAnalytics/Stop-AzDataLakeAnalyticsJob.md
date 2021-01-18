---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518718"
---
# <span data-ttu-id="7e0d8-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7e0d8-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="7e0d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e0d8-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0d8-103">Отмена задания.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-103">Cancels a job.</span></span>

## <span data-ttu-id="7e0d8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e0d8-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e0d8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e0d8-105">DESCRIPTION</span></span>
<span data-ttu-id="7e0d8-106">Для отмены задания Azure Data Lake Analytics будет отменено задание **Stop-AzDataLakeAnalyticsJob.**</span><span class="sxs-lookup"><span data-stu-id="7e0d8-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="7e0d8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e0d8-107">EXAMPLES</span></span>

### <span data-ttu-id="7e0d8-108">Пример 1. Отмена задания</span><span class="sxs-lookup"><span data-stu-id="7e0d8-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="7e0d8-109">Эта команда отменяет задание с указанным ИД.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="7e0d8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e0d8-110">PARAMETERS</span></span>

### <span data-ttu-id="7e0d8-111">-Account</span><span class="sxs-lookup"><span data-stu-id="7e0d8-111">-Account</span></span>
<span data-ttu-id="7e0d8-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="7e0d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0d8-113">-DefaultProfile</span></span>
<span data-ttu-id="7e0d8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7e0d8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e0d8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7e0d8-115">-Force</span></span>
<span data-ttu-id="7e0d8-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7e0d8-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="7e0d8-117">-JobId</span></span>
<span data-ttu-id="7e0d8-118">Определяет ИД отменяемого задания.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="7e0d8-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e0d8-119">-PassThru</span></span>
<span data-ttu-id="7e0d8-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7e0d8-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7e0d8-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e0d8-122">-Confirm</span></span>
<span data-ttu-id="7e0d8-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e0d8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e0d8-124">-WhatIf</span></span>
<span data-ttu-id="7e0d8-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e0d8-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e0d8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0d8-127">CommonParameters</span></span>
<span data-ttu-id="7e0d8-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e0d8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0d8-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e0d8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0d8-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e0d8-130">INPUTS</span></span>

### <span data-ttu-id="7e0d8-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7e0d8-131">System.String</span></span>

### <span data-ttu-id="7e0d8-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7e0d8-132">System.Guid</span></span>

### <span data-ttu-id="7e0d8-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7e0d8-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7e0d8-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e0d8-134">OUTPUTS</span></span>

### <span data-ttu-id="7e0d8-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7e0d8-135">System.Boolean</span></span>

## <span data-ttu-id="7e0d8-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e0d8-136">NOTES</span></span>

## <span data-ttu-id="7e0d8-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e0d8-137">RELATED LINKS</span></span>

[<span data-ttu-id="7e0d8-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7e0d8-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="7e0d8-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7e0d8-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="7e0d8-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="7e0d8-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


