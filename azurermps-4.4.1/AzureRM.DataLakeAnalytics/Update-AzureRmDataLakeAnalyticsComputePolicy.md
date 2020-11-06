---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 67cffe7f0cdaebc655eb98321166bb7805844a5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568078"
---
# <span data-ttu-id="b67a5-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="b67a5-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="b67a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b67a5-102">SYNOPSIS</span></span>
<span data-ttu-id="b67a5-103">Обновляет правило политики вычисления Data Lake Analytics для определенной сущности AAD.</span><span class="sxs-lookup"><span data-stu-id="b67a5-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b67a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b67a5-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b67a5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b67a5-105">DESCRIPTION</span></span>
<span data-ttu-id="b67a5-106">**Обновление — AzureRmDataLakeAnalyticsComputePolicy** обновляет указанное правило политики вычислений для определенной сущности AAD в учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b67a5-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="b67a5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b67a5-107">EXAMPLES</span></span>

### <span data-ttu-id="b67a5-108">Пример 1: обновление одного правила в политике вычислений</span><span class="sxs-lookup"><span data-stu-id="b67a5-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="b67a5-109">Эта команда обновляет политику с именем "myPolicy" в учетной записи "contosoadla", чтобы убедиться в том, что пользователь не может отправить задание с более чем 5 параллелизмом.</span><span class="sxs-lookup"><span data-stu-id="b67a5-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="b67a5-110">Пример 2: Создание политики вычислений с обновлением и обоими правилами</span><span class="sxs-lookup"><span data-stu-id="b67a5-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="b67a5-111">Эта команда создает политику с именем "myPolicy" в учетной записи "contosoadla", чтобы убедиться в том, что пользователь не может отправить задание с более чем 5 параллелизмом или с приоритетом ниже 100</span><span class="sxs-lookup"><span data-stu-id="b67a5-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="b67a5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b67a5-112">PARAMETERS</span></span>

### <span data-ttu-id="b67a5-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="b67a5-113">-Account</span></span>
<span data-ttu-id="b67a5-114">Имя учетной записи, в которой нужно обновить политику вычисления.</span><span class="sxs-lookup"><span data-stu-id="b67a5-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="b67a5-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="b67a5-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="b67a5-116">Максимальная поддерживаемая степень параллелизма для задания в этой политике.</span><span class="sxs-lookup"><span data-stu-id="b67a5-116">The maximum supported degree of parallelism per job for this policy.</span></span> <span data-ttu-id="b67a5-117">Необходимо указать значение, MinPriorityPerJob или оба параметра.</span><span class="sxs-lookup"><span data-stu-id="b67a5-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="b67a5-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="b67a5-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="b67a5-119">Минимальный поддерживаемый приоритет для задания в этой политике.</span><span class="sxs-lookup"><span data-stu-id="b67a5-119">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="b67a5-120">Необходимо указать значение, MaxDegreeOfParallelismPerJob или оба параметра.</span><span class="sxs-lookup"><span data-stu-id="b67a5-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="b67a5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b67a5-121">-Name</span></span>
<span data-ttu-id="b67a5-122">Имя обновляемой политики вычислений.</span><span class="sxs-lookup"><span data-stu-id="b67a5-122">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="b67a5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b67a5-123">-ResourceGroupName</span></span>
<span data-ttu-id="b67a5-124">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="b67a5-124">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="b67a5-125">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="b67a5-125">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="b67a5-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b67a5-126">-Confirm</span></span>
<span data-ttu-id="b67a5-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b67a5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b67a5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b67a5-128">-WhatIf</span></span>
<span data-ttu-id="b67a5-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b67a5-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b67a5-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b67a5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b67a5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b67a5-131">-DefaultProfile</span></span>
<span data-ttu-id="b67a5-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b67a5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b67a5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b67a5-133">CommonParameters</span></span>
<span data-ttu-id="b67a5-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b67a5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b67a5-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b67a5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b67a5-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b67a5-136">INPUTS</span></span>

### <span data-ttu-id="b67a5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b67a5-137">System.String</span></span>
<span data-ttu-id="b67a5-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b67a5-138">System.Int32</span></span>

## <span data-ttu-id="b67a5-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b67a5-139">OUTPUTS</span></span>

### <span data-ttu-id="b67a5-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="b67a5-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="b67a5-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="b67a5-141">NOTES</span></span>

## <span data-ttu-id="b67a5-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b67a5-142">RELATED LINKS</span></span>

