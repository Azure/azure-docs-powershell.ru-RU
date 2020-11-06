---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/update-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 860b58ce3be37eb2ef2277b627971adb301a02af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566501"
---
# <span data-ttu-id="f53e8-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="f53e8-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="f53e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f53e8-102">SYNOPSIS</span></span>
<span data-ttu-id="f53e8-103">Обновляет правило политики вычисления Data Lake Analytics для определенной сущности AAD.</span><span class="sxs-lookup"><span data-stu-id="f53e8-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f53e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f53e8-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f53e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f53e8-105">DESCRIPTION</span></span>
<span data-ttu-id="f53e8-106">**Обновление — AzureRmDataLakeAnalyticsComputePolicy** обновляет указанное правило политики вычислений для определенной сущности AAD в учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f53e8-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f53e8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f53e8-107">EXAMPLES</span></span>

### <span data-ttu-id="f53e8-108">Пример 1: обновление одного правила в политике вычислений</span><span class="sxs-lookup"><span data-stu-id="f53e8-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="f53e8-109">Эта команда обновляет политику с именем "myPolicy" в учетной записи "contosoadla", чтобы убедиться в том, что пользователь не может отправить задание с более чем 5 аналитических единиц.</span><span class="sxs-lookup"><span data-stu-id="f53e8-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="f53e8-110">Пример 2: Создание политики вычислений с обновлением и обоими правилами</span><span class="sxs-lookup"><span data-stu-id="f53e8-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="f53e8-111">Эта команда создает политику с именем "myPolicy" в учетной записи "contosoadla", чтобы убедиться в том, что пользователь не может отправить задание с более чем 5 аналитических единиц или с более низким приоритетом, чем 100</span><span class="sxs-lookup"><span data-stu-id="f53e8-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="f53e8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f53e8-112">PARAMETERS</span></span>

### <span data-ttu-id="f53e8-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="f53e8-113">-Account</span></span>
<span data-ttu-id="f53e8-114">Имя учетной записи, в которой нужно обновить политику вычисления.</span><span class="sxs-lookup"><span data-stu-id="f53e8-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="f53e8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53e8-115">-DefaultProfile</span></span>
<span data-ttu-id="f53e8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f53e8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f53e8-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="f53e8-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="f53e8-118">Максимальные поддерживаемые единицы аналитики для задания для этой политики.</span><span class="sxs-lookup"><span data-stu-id="f53e8-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="f53e8-119">Необходимо указать значение, MinPriorityPerJob или оба параметра.</span><span class="sxs-lookup"><span data-stu-id="f53e8-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="f53e8-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="f53e8-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="f53e8-121">Минимальный поддерживаемый приоритет для задания в этой политике.</span><span class="sxs-lookup"><span data-stu-id="f53e8-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="f53e8-122">Необходимо указать значение, MaxAnalyticsUnitsPerJob или оба параметра.</span><span class="sxs-lookup"><span data-stu-id="f53e8-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="f53e8-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f53e8-123">-Name</span></span>
<span data-ttu-id="f53e8-124">Имя обновляемой политики вычислений.</span><span class="sxs-lookup"><span data-stu-id="f53e8-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="f53e8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53e8-125">-ResourceGroupName</span></span>
<span data-ttu-id="f53e8-126">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="f53e8-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="f53e8-127">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="f53e8-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="f53e8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f53e8-128">-Confirm</span></span>
<span data-ttu-id="f53e8-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f53e8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f53e8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f53e8-130">-WhatIf</span></span>
<span data-ttu-id="f53e8-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f53e8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f53e8-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f53e8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f53e8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53e8-133">CommonParameters</span></span>
<span data-ttu-id="f53e8-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f53e8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53e8-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f53e8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53e8-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f53e8-136">INPUTS</span></span>

### <span data-ttu-id="f53e8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f53e8-137">System.String</span></span>

### <span data-ttu-id="f53e8-138">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f53e8-138">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f53e8-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f53e8-139">OUTPUTS</span></span>

### <span data-ttu-id="f53e8-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="f53e8-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="f53e8-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="f53e8-141">NOTES</span></span>

## <span data-ttu-id="f53e8-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f53e8-142">RELATED LINKS</span></span>
