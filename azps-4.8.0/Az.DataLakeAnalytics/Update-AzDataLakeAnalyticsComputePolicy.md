---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077859"
---
# <span data-ttu-id="d1c42-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="d1c42-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="d1c42-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1c42-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c42-103">Обновляет правило политики вычисления Data Lake Analytics для определенной сущности AAD.</span><span class="sxs-lookup"><span data-stu-id="d1c42-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="d1c42-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1c42-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1c42-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1c42-105">DESCRIPTION</span></span>
<span data-ttu-id="d1c42-106">**Обновление — AzDataLakeAnalyticsComputePolicy** обновляет указанное правило политики вычислений для определенной сущности AAD в учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d1c42-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d1c42-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1c42-107">EXAMPLES</span></span>

### <span data-ttu-id="d1c42-108">Пример 1: обновление одного правила в политике вычислений</span><span class="sxs-lookup"><span data-stu-id="d1c42-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="d1c42-109">Эта команда обновляет политику с именем "myPolicy" в учетной записи "contosoadla", чтобы убедиться в том, что пользователь не может отправить задание с более чем 5 аналитических единиц.</span><span class="sxs-lookup"><span data-stu-id="d1c42-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="d1c42-110">Пример 2: Создание политики вычислений с обновлением и обоими правилами</span><span class="sxs-lookup"><span data-stu-id="d1c42-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="d1c42-111">Эта команда создает политику с именем "myPolicy" в учетной записи "contosoadla", чтобы убедиться в том, что пользователь не может отправить задание с более чем 5 аналитических единиц или с более низким приоритетом, чем 100</span><span class="sxs-lookup"><span data-stu-id="d1c42-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="d1c42-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1c42-112">PARAMETERS</span></span>

### <span data-ttu-id="d1c42-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d1c42-113">-Account</span></span>
<span data-ttu-id="d1c42-114">Имя учетной записи, в которой нужно обновить политику вычисления.</span><span class="sxs-lookup"><span data-stu-id="d1c42-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="d1c42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c42-115">-DefaultProfile</span></span>
<span data-ttu-id="d1c42-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d1c42-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1c42-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="d1c42-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="d1c42-118">Максимальные поддерживаемые единицы аналитики для задания для этой политики.</span><span class="sxs-lookup"><span data-stu-id="d1c42-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="d1c42-119">Необходимо указать значение, MinPriorityPerJob или оба параметра.</span><span class="sxs-lookup"><span data-stu-id="d1c42-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="d1c42-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="d1c42-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="d1c42-121">Минимальный поддерживаемый приоритет для задания в этой политике.</span><span class="sxs-lookup"><span data-stu-id="d1c42-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="d1c42-122">Необходимо указать значение, MaxAnalyticsUnitsPerJob или оба параметра.</span><span class="sxs-lookup"><span data-stu-id="d1c42-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="d1c42-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d1c42-123">-Name</span></span>
<span data-ttu-id="d1c42-124">Имя обновляемой политики вычислений.</span><span class="sxs-lookup"><span data-stu-id="d1c42-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="d1c42-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c42-125">-ResourceGroupName</span></span>
<span data-ttu-id="d1c42-126">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="d1c42-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="d1c42-127">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="d1c42-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="d1c42-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1c42-128">-Confirm</span></span>
<span data-ttu-id="d1c42-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d1c42-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1c42-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1c42-130">-WhatIf</span></span>
<span data-ttu-id="d1c42-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d1c42-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1c42-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d1c42-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1c42-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c42-133">CommonParameters</span></span>
<span data-ttu-id="d1c42-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1c42-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c42-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1c42-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c42-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1c42-136">INPUTS</span></span>

### <span data-ttu-id="d1c42-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d1c42-137">System.String</span></span>

### <span data-ttu-id="d1c42-138">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d1c42-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d1c42-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1c42-139">OUTPUTS</span></span>

### <span data-ttu-id="d1c42-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="d1c42-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="d1c42-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1c42-141">NOTES</span></span>

## <span data-ttu-id="d1c42-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1c42-142">RELATED LINKS</span></span>
