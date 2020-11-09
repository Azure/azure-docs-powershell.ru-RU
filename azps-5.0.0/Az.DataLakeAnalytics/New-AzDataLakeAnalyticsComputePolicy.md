---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 76df1cb780220a09ccc0d571fd88223e746eefe6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313562"
---
# <span data-ttu-id="54c83-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="54c83-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="54c83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54c83-102">SYNOPSIS</span></span>
<span data-ttu-id="54c83-103">Создает правило политики COMPUTE Data Lake Analytics для определенной сущности AAD.</span><span class="sxs-lookup"><span data-stu-id="54c83-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="54c83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54c83-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c83-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54c83-105">DESCRIPTION</span></span>
<span data-ttu-id="54c83-106">**Новый параметр-AzDataLakeAnalyticsComputePolicy** создает указанное правило политики вычислений для определенной сущности AAD в учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="54c83-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="54c83-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54c83-107">EXAMPLES</span></span>

### <span data-ttu-id="54c83-108">Пример 1: Создание политики вычислений с одним правилом</span><span class="sxs-lookup"><span data-stu-id="54c83-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="54c83-109">Эта команда создает политику с именем "myPolicy" в учетной записи "contosoadla" для пользователя с идентификатором "83cb7ad2-3523-4b82-b909-d478b0d8aea3", гарантирующий, что он не сможет отправлять задания с более чем 5 единицами аналитики.</span><span class="sxs-lookup"><span data-stu-id="54c83-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="54c83-110">Пример 2: Создание политики вычислений с обоими наборами правил</span><span class="sxs-lookup"><span data-stu-id="54c83-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="54c83-111">Эта команда создает политику с именем "myPolicy" в учетной записи "contosoadla" для пользователя с идентификатором "83cb7ad2-3523-4b82-b909-d478b0d8aea3", гарантирующий, что он не сможет отправлять задания с более чем 5 аналитических единиц или с более низким приоритетом, чем 100</span><span class="sxs-lookup"><span data-stu-id="54c83-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="54c83-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54c83-112">PARAMETERS</span></span>

### <span data-ttu-id="54c83-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="54c83-113">-Account</span></span>
<span data-ttu-id="54c83-114">Имя учетной записи, в которую нужно добавить политику вычисления.</span><span class="sxs-lookup"><span data-stu-id="54c83-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="54c83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c83-115">-DefaultProfile</span></span>
<span data-ttu-id="54c83-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="54c83-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54c83-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="54c83-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="54c83-118">Максимальные поддерживаемые единицы аналитики для задания для этой политики.</span><span class="sxs-lookup"><span data-stu-id="54c83-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="54c83-119">Необходимо указать значение, MinPriorityPerJob или оба параметра.</span><span class="sxs-lookup"><span data-stu-id="54c83-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="54c83-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="54c83-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="54c83-121">Минимальный поддерживаемый приоритет для задания в этой политике.</span><span class="sxs-lookup"><span data-stu-id="54c83-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="54c83-122">Необходимо указать значение, MaxAnalyticsUnitsPerJob или оба параметра.</span><span class="sxs-lookup"><span data-stu-id="54c83-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="54c83-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54c83-123">-Name</span></span>
<span data-ttu-id="54c83-124">Имя создаваемой политики вычислений.</span><span class="sxs-lookup"><span data-stu-id="54c83-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="54c83-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="54c83-125">-ObjectId</span></span>
<span data-ttu-id="54c83-126">Идентификатор объекта Azure Active Directory для пользователя или группы, к которой применяется политика.</span><span class="sxs-lookup"><span data-stu-id="54c83-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c83-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="54c83-127">-ObjectType</span></span>
<span data-ttu-id="54c83-128">Тип объекта Azure Active Directory для переданного идентификатора объекта.</span><span class="sxs-lookup"><span data-stu-id="54c83-128">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c83-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c83-129">-ResourceGroupName</span></span>
<span data-ttu-id="54c83-130">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="54c83-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="54c83-131">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="54c83-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="54c83-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54c83-132">-Confirm</span></span>
<span data-ttu-id="54c83-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54c83-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c83-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c83-134">-WhatIf</span></span>
<span data-ttu-id="54c83-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54c83-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54c83-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54c83-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c83-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c83-137">CommonParameters</span></span>
<span data-ttu-id="54c83-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54c83-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c83-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54c83-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c83-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54c83-140">INPUTS</span></span>

### <span data-ttu-id="54c83-141">System. String</span><span class="sxs-lookup"><span data-stu-id="54c83-141">System.String</span></span>

### <span data-ttu-id="54c83-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="54c83-142">System.Guid</span></span>

### <span data-ttu-id="54c83-143">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="54c83-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="54c83-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54c83-144">OUTPUTS</span></span>

### <span data-ttu-id="54c83-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="54c83-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="54c83-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="54c83-146">NOTES</span></span>

## <span data-ttu-id="54c83-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54c83-147">RELATED LINKS</span></span>