---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: cd173d17b0867fb5c635b77ee6c72847dc845cb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072971"
---
# <span data-ttu-id="b6680-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="b6680-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="b6680-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6680-102">SYNOPSIS</span></span>
<span data-ttu-id="b6680-103">Запускает оценку соответствия политике для всех ресурсов в подписке или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6680-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="b6680-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6680-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6680-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6680-105">DESCRIPTION</span></span>
<span data-ttu-id="b6680-106">Командлет **Start-AzPolicyComplianceScan** запускает оценку соответствия политике для подписки или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6680-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="b6680-107">Состояние соответствия для всех ресурсов в этой области будет оценено для всех назначенных политик.</span><span class="sxs-lookup"><span data-stu-id="b6680-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="b6680-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6680-108">EXAMPLES</span></span>

### <span data-ttu-id="b6680-109">Пример 1: Начало проверки соответствия требованиям в области подписки</span><span class="sxs-lookup"><span data-stu-id="b6680-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="b6680-110">Эта команда запускает оценку соответствия политике для активной подписки.</span><span class="sxs-lookup"><span data-stu-id="b6680-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="b6680-111">Пример 2: Начало проверки соответствия на уровне группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b6680-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="b6680-112">Эта команда запускает оценку соответствия политике для группы ресурсов "myRG" в активной подписке.</span><span class="sxs-lookup"><span data-stu-id="b6680-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="b6680-113">Пример 3: Начало проверки соответствия требованиям и ожидание ее завершения в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b6680-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan
PS C:\> $job | Wait-Job
```

<span data-ttu-id="b6680-114">Эта команда запускает оценку соответствия политике для активной подписки.</span><span class="sxs-lookup"><span data-stu-id="b6680-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="b6680-115">Она будет ждать завершения сканирования.</span><span class="sxs-lookup"><span data-stu-id="b6680-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="b6680-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6680-116">PARAMETERS</span></span>

### <span data-ttu-id="b6680-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6680-117">-AsJob</span></span>
<span data-ttu-id="b6680-118">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="b6680-118">Run cmdlet in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6680-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6680-119">-DefaultProfile</span></span>
<span data-ttu-id="b6680-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6680-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6680-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6680-121">-PassThru</span></span>
<span data-ttu-id="b6680-122">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b6680-122">Return True if the command completes successfully.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6680-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6680-123">-ResourceGroupName</span></span>
<span data-ttu-id="b6680-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b6680-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6680-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6680-125">-Confirm</span></span>
<span data-ttu-id="b6680-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b6680-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6680-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6680-127">-WhatIf</span></span>
<span data-ttu-id="b6680-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b6680-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6680-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b6680-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6680-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6680-130">CommonParameters</span></span>
<span data-ttu-id="b6680-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6680-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6680-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6680-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6680-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6680-133">INPUTS</span></span>

### <span data-ttu-id="b6680-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b6680-134">System.String</span></span>

## <span data-ttu-id="b6680-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6680-135">OUTPUTS</span></span>

### <span data-ttu-id="b6680-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6680-136">System.Boolean</span></span>

## <span data-ttu-id="b6680-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6680-137">NOTES</span></span>

## <span data-ttu-id="b6680-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6680-138">RELATED LINKS</span></span>
