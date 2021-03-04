---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: db51cfdf499fcf3d6c81f47d977978a6ff4bf8cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989075"
---
# <span data-ttu-id="f4f34-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="f4f34-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="f4f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f34-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f34-103">Запуск оценки соответствия политике для всех ресурсов в группе подписок или ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4f34-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="f4f34-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f4f34-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4f34-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4f34-105">DESCRIPTION</span></span>
<span data-ttu-id="f4f34-106">Для подписки или группы ресурсов запускается проектлет **Start-AzPolicyComplianceScan,** который начинает оценку соответствия политике.</span><span class="sxs-lookup"><span data-stu-id="f4f34-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="f4f34-107">Для всех ресурсов в этой области будет оцениваться их состояние соответствия всем политикам.</span><span class="sxs-lookup"><span data-stu-id="f4f34-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="f4f34-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f4f34-108">EXAMPLES</span></span>

### <span data-ttu-id="f4f34-109">Пример 1. Запуск проверки соответствия требованиям в области подписки</span><span class="sxs-lookup"><span data-stu-id="f4f34-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="f4f34-110">Эта команда запускает оценку соответствия политике для активной подписки.</span><span class="sxs-lookup"><span data-stu-id="f4f34-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="f4f34-111">Пример 2. Запуск проверки соответствия требованиям в области группировки ресурсов</span><span class="sxs-lookup"><span data-stu-id="f4f34-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="f4f34-112">Эта команда запускает оценку соответствия политике для группы ресурсов myRG в активной подписке.</span><span class="sxs-lookup"><span data-stu-id="f4f34-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="f4f34-113">Пример 3. Запуск проверки соответствия требованиям и ее завершение в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f4f34-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="f4f34-114">Эта команда запускает оценку соответствия политике для активной подписки.</span><span class="sxs-lookup"><span data-stu-id="f4f34-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="f4f34-115">Проверка будет завершена.</span><span class="sxs-lookup"><span data-stu-id="f4f34-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="f4f34-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4f34-116">PARAMETERS</span></span>

### <span data-ttu-id="f4f34-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4f34-117">-AsJob</span></span>
<span data-ttu-id="f4f34-118">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="f4f34-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f4f34-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f34-119">-DefaultProfile</span></span>
<span data-ttu-id="f4f34-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f34-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4f34-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4f34-121">-PassThru</span></span>
<span data-ttu-id="f4f34-122">Если команда успешно завершена, возвращается "Истина".</span><span class="sxs-lookup"><span data-stu-id="f4f34-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="f4f34-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f34-123">-ResourceGroupName</span></span>
<span data-ttu-id="f4f34-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4f34-124">Resource group name.</span></span>

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

### <span data-ttu-id="f4f34-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4f34-125">-Confirm</span></span>
<span data-ttu-id="f4f34-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4f34-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4f34-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4f34-127">-WhatIf</span></span>
<span data-ttu-id="f4f34-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4f34-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4f34-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f4f34-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4f34-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f34-130">CommonParameters</span></span>
<span data-ttu-id="f4f34-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4f34-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f34-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4f34-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f34-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4f34-133">INPUTS</span></span>

### <span data-ttu-id="f4f34-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f4f34-134">System.String</span></span>

## <span data-ttu-id="f4f34-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4f34-135">OUTPUTS</span></span>

### <span data-ttu-id="f4f34-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f4f34-136">System.Boolean</span></span>

## <span data-ttu-id="f4f34-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f4f34-137">NOTES</span></span>

## <span data-ttu-id="f4f34-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4f34-138">RELATED LINKS</span></span>
