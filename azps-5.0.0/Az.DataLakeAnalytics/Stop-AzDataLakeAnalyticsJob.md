---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313496"
---
# <span data-ttu-id="8c853-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8c853-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="8c853-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c853-102">SYNOPSIS</span></span>
<span data-ttu-id="8c853-103">Отменяет задание.</span><span class="sxs-lookup"><span data-stu-id="8c853-103">Cancels a job.</span></span>

## <span data-ttu-id="8c853-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c853-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c853-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c853-105">DESCRIPTION</span></span>
<span data-ttu-id="8c853-106">Командлет **Stop-AzDataLakeAnalyticsJob** отменяет задание Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8c853-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="8c853-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c853-107">EXAMPLES</span></span>

### <span data-ttu-id="8c853-108">Пример 1: Отмена задания</span><span class="sxs-lookup"><span data-stu-id="8c853-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="8c853-109">Эта команда отменяет задание с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="8c853-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="8c853-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c853-110">PARAMETERS</span></span>

### <span data-ttu-id="8c853-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8c853-111">-Account</span></span>
<span data-ttu-id="8c853-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8c853-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="8c853-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c853-113">-DefaultProfile</span></span>
<span data-ttu-id="8c853-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8c853-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c853-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8c853-115">-Force</span></span>
<span data-ttu-id="8c853-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8c853-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8c853-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="8c853-117">-JobId</span></span>
<span data-ttu-id="8c853-118">Указывает идентификатор задания, которое нужно отменить.</span><span class="sxs-lookup"><span data-stu-id="8c853-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="8c853-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c853-119">-PassThru</span></span>
<span data-ttu-id="8c853-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8c853-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8c853-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8c853-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c853-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c853-122">-Confirm</span></span>
<span data-ttu-id="8c853-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8c853-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c853-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c853-124">-WhatIf</span></span>
<span data-ttu-id="8c853-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8c853-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c853-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8c853-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c853-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c853-127">CommonParameters</span></span>
<span data-ttu-id="8c853-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c853-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c853-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c853-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c853-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c853-130">INPUTS</span></span>

### <span data-ttu-id="8c853-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8c853-131">System.String</span></span>

### <span data-ttu-id="8c853-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8c853-132">System.Guid</span></span>

### <span data-ttu-id="8c853-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c853-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8c853-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c853-134">OUTPUTS</span></span>

### <span data-ttu-id="8c853-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c853-135">System.Boolean</span></span>

## <span data-ttu-id="8c853-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c853-136">NOTES</span></span>

## <span data-ttu-id="8c853-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c853-137">RELATED LINKS</span></span>

[<span data-ttu-id="8c853-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8c853-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="8c853-139">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8c853-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="8c853-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8c853-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)

