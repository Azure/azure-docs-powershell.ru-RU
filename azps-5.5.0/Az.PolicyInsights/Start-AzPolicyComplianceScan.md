---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240325"
---
# <span data-ttu-id="ee214-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="ee214-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="ee214-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee214-102">SYNOPSIS</span></span>
<span data-ttu-id="ee214-103">Запуск оценки соответствия политике для всех ресурсов в группе подписок или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee214-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="ee214-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ee214-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee214-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee214-105">DESCRIPTION</span></span>
<span data-ttu-id="ee214-106">Для подписки или группы ресурсов запускается проектлет **Start-AzPolicyComplianceScan,** который начинает оценку соответствия политике.</span><span class="sxs-lookup"><span data-stu-id="ee214-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="ee214-107">Для всех ресурсов в этой области будет оцениваться их состояние соответствия всем политикам.</span><span class="sxs-lookup"><span data-stu-id="ee214-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="ee214-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ee214-108">EXAMPLES</span></span>

### <span data-ttu-id="ee214-109">Пример 1. Запуск проверки соответствия требованиям в области подписки</span><span class="sxs-lookup"><span data-stu-id="ee214-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="ee214-110">Эта команда начинает оценку соответствия политике для активной подписки.</span><span class="sxs-lookup"><span data-stu-id="ee214-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="ee214-111">Пример 2. Запуск проверки соответствия требованиям в области группировки ресурсов</span><span class="sxs-lookup"><span data-stu-id="ee214-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="ee214-112">Эта команда запускает оценку соответствия политике для группы ресурсов MyRG в активной подписке.</span><span class="sxs-lookup"><span data-stu-id="ee214-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="ee214-113">Пример 3. Запуск проверки соответствия требованиям и ее завершение в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ee214-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="ee214-114">Эта команда начинает оценку соответствия политике для активной подписки.</span><span class="sxs-lookup"><span data-stu-id="ee214-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="ee214-115">Проверка будет завершена.</span><span class="sxs-lookup"><span data-stu-id="ee214-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="ee214-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee214-116">PARAMETERS</span></span>

### <span data-ttu-id="ee214-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee214-117">-AsJob</span></span>
<span data-ttu-id="ee214-118">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="ee214-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ee214-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee214-119">-DefaultProfile</span></span>
<span data-ttu-id="ee214-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee214-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee214-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee214-121">-PassThru</span></span>
<span data-ttu-id="ee214-122">Если команда успешно завершена, возвращается "Истина".</span><span class="sxs-lookup"><span data-stu-id="ee214-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="ee214-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee214-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee214-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee214-124">Resource group name.</span></span>

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

### <span data-ttu-id="ee214-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee214-125">-Confirm</span></span>
<span data-ttu-id="ee214-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ee214-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee214-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee214-127">-WhatIf</span></span>
<span data-ttu-id="ee214-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee214-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee214-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ee214-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee214-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee214-130">CommonParameters</span></span>
<span data-ttu-id="ee214-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee214-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee214-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee214-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee214-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee214-133">INPUTS</span></span>

### <span data-ttu-id="ee214-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ee214-134">System.String</span></span>

## <span data-ttu-id="ee214-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee214-135">OUTPUTS</span></span>

### <span data-ttu-id="ee214-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee214-136">System.Boolean</span></span>

## <span data-ttu-id="ee214-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ee214-137">NOTES</span></span>

## <span data-ttu-id="ee214-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee214-138">RELATED LINKS</span></span>
