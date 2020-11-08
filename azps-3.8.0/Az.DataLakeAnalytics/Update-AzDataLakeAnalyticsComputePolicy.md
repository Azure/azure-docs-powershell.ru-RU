---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065002"
---
# <span data-ttu-id="03003-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="03003-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="03003-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03003-102">SYNOPSIS</span></span>
<span data-ttu-id="03003-103">Обновляет правило политики вычисления Data Lake Analytics для определенной сущности AAD.</span><span class="sxs-lookup"><span data-stu-id="03003-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="03003-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03003-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03003-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03003-105">DESCRIPTION</span></span>
<span data-ttu-id="03003-106">**Обновление — AzDataLakeAnalyticsComputePolicy** обновляет указанное правило политики вычислений для определенной сущности AAD в учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="03003-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="03003-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03003-107">EXAMPLES</span></span>

### <span data-ttu-id="03003-108">Пример 1: обновление одного правила в политике вычислений</span><span class="sxs-lookup"><span data-stu-id="03003-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="03003-109">Эта команда обновляет политику с именем "myPolicy" в учетной записи "contosoadla", чтобы убедиться в том, что пользователь не может отправить задание с более чем 5 аналитических единиц.</span><span class="sxs-lookup"><span data-stu-id="03003-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="03003-110">Пример 2: Создание политики вычислений с обновлением и обоими правилами</span><span class="sxs-lookup"><span data-stu-id="03003-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="03003-111">Эта команда создает политику с именем "myPolicy" в учетной записи "contosoadla", чтобы убедиться в том, что пользователь не может отправить задание с более чем 5 аналитических единиц или с более низким приоритетом, чем 100</span><span class="sxs-lookup"><span data-stu-id="03003-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="03003-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03003-112">PARAMETERS</span></span>

### <span data-ttu-id="03003-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="03003-113">-Account</span></span>
<span data-ttu-id="03003-114">Имя учетной записи, в которой нужно обновить политику вычисления.</span><span class="sxs-lookup"><span data-stu-id="03003-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="03003-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03003-115">-DefaultProfile</span></span>
<span data-ttu-id="03003-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="03003-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03003-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="03003-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="03003-118">Максимальные поддерживаемые единицы аналитики для задания для этой политики.</span><span class="sxs-lookup"><span data-stu-id="03003-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="03003-119">Необходимо указать значение, MinPriorityPerJob или оба параметра.</span><span class="sxs-lookup"><span data-stu-id="03003-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03003-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="03003-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="03003-121">Минимальный поддерживаемый приоритет для задания в этой политике.</span><span class="sxs-lookup"><span data-stu-id="03003-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="03003-122">Необходимо указать значение, MaxAnalyticsUnitsPerJob или оба параметра.</span><span class="sxs-lookup"><span data-stu-id="03003-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03003-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="03003-123">-Name</span></span>
<span data-ttu-id="03003-124">Имя обновляемой политики вычислений.</span><span class="sxs-lookup"><span data-stu-id="03003-124">Name of the compute policy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03003-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03003-125">-ResourceGroupName</span></span>
<span data-ttu-id="03003-126">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="03003-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="03003-127">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="03003-127">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03003-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03003-128">-Confirm</span></span>
<span data-ttu-id="03003-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03003-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03003-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03003-130">-WhatIf</span></span>
<span data-ttu-id="03003-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="03003-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03003-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03003-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03003-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03003-133">CommonParameters</span></span>
<span data-ttu-id="03003-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03003-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03003-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03003-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03003-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03003-136">INPUTS</span></span>

### <span data-ttu-id="03003-137">System. String</span><span class="sxs-lookup"><span data-stu-id="03003-137">System.String</span></span>

### <span data-ttu-id="03003-138">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="03003-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="03003-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03003-139">OUTPUTS</span></span>

### <span data-ttu-id="03003-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="03003-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="03003-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="03003-141">NOTES</span></span>

## <span data-ttu-id="03003-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03003-142">RELATED LINKS</span></span>
