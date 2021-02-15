---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 047d0c7c9b141f10ee3f1be2ba1e739960f2e5bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228780"
---
# <span data-ttu-id="21b82-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="21b82-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="21b82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21b82-102">SYNOPSIS</span></span>
<span data-ttu-id="21b82-103">Ожидание завершения задания.</span><span class="sxs-lookup"><span data-stu-id="21b82-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="21b82-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="21b82-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21b82-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21b82-105">DESCRIPTION</span></span>
<span data-ttu-id="21b82-106">Для выполнения задания Azure Data Lake Analytics выполнится cmdlet **Wait-AzDataLakeAnalyticsJob.**</span><span class="sxs-lookup"><span data-stu-id="21b82-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="21b82-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="21b82-107">EXAMPLES</span></span>

### <span data-ttu-id="21b82-108">Пример 1. Ожидание завершения задания</span><span class="sxs-lookup"><span data-stu-id="21b82-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="21b82-109">Следующая команда ждет завершения задания с указанным ид.</span><span class="sxs-lookup"><span data-stu-id="21b82-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="21b82-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21b82-110">PARAMETERS</span></span>

### <span data-ttu-id="21b82-111">-Account</span><span class="sxs-lookup"><span data-stu-id="21b82-111">-Account</span></span>
<span data-ttu-id="21b82-112">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="21b82-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="21b82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21b82-113">-DefaultProfile</span></span>
<span data-ttu-id="21b82-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="21b82-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21b82-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="21b82-115">-JobId</span></span>
<span data-ttu-id="21b82-116">Определяет ИД задания, для которого нужно подождать.</span><span class="sxs-lookup"><span data-stu-id="21b82-116">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="21b82-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="21b82-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="21b82-118">Определяет, сколько секунд нужно подождать, прежде чем выйти из операции ожидания.</span><span class="sxs-lookup"><span data-stu-id="21b82-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21b82-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="21b82-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="21b82-120">Укажите количество секунд, которое будет отстать от каждой проверки состояния задания.</span><span class="sxs-lookup"><span data-stu-id="21b82-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21b82-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b82-121">CommonParameters</span></span>
<span data-ttu-id="21b82-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21b82-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b82-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21b82-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b82-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21b82-124">INPUTS</span></span>

### <span data-ttu-id="21b82-125">System.String</span><span class="sxs-lookup"><span data-stu-id="21b82-125">System.String</span></span>

### <span data-ttu-id="21b82-126">System.Guid</span><span class="sxs-lookup"><span data-stu-id="21b82-126">System.Guid</span></span>

### <span data-ttu-id="21b82-127">System.Int32</span><span class="sxs-lookup"><span data-stu-id="21b82-127">System.Int32</span></span>

## <span data-ttu-id="21b82-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="21b82-128">OUTPUTS</span></span>

### <span data-ttu-id="21b82-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span><span class="sxs-lookup"><span data-stu-id="21b82-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="21b82-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="21b82-130">NOTES</span></span>

## <span data-ttu-id="21b82-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21b82-131">RELATED LINKS</span></span>

[<span data-ttu-id="21b82-132">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="21b82-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="21b82-133">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="21b82-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="21b82-134">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="21b82-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)


