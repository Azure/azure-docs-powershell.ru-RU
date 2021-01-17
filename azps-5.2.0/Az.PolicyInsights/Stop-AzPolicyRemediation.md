---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 9dfb3ff2f50df7a858ab8194ec86fa312501dcff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417900"
---
# <span data-ttu-id="1498a-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="1498a-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="1498a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1498a-102">SYNOPSIS</span></span>
<span data-ttu-id="1498a-103">Отмена выполнения исправлений политики.</span><span class="sxs-lookup"><span data-stu-id="1498a-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="1498a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1498a-104">SYNTAX</span></span>

### <span data-ttu-id="1498a-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1498a-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1498a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1498a-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1498a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1498a-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1498a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1498a-108">DESCRIPTION</span></span>
<span data-ttu-id="1498a-109">Из-за выполнения исправлений политика **Stop-AzPolicyRemediation** отменяется.</span><span class="sxs-lookup"><span data-stu-id="1498a-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="1498a-110">Активные развертывания будут отменены, а новые развертывания не будут созданы.</span><span class="sxs-lookup"><span data-stu-id="1498a-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="1498a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1498a-111">EXAMPLES</span></span>

### <span data-ttu-id="1498a-112">Пример 1. Отмена исправлений политики в области группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1498a-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="1498a-113">Эта команда отменяет исправление с именем "исправление1" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="1498a-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="1498a-114">Пример 2. Отмена исправлений для группы управления с помощью piping</span><span class="sxs-lookup"><span data-stu-id="1498a-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="1498a-115">Эта команда отменяет исправление с именем "исправление1" в группе управления "mg1".</span><span class="sxs-lookup"><span data-stu-id="1498a-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="1498a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1498a-116">PARAMETERS</span></span>

### <span data-ttu-id="1498a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1498a-117">-AsJob</span></span>
<span data-ttu-id="1498a-118">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="1498a-118">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1498a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1498a-119">-DefaultProfile</span></span>
<span data-ttu-id="1498a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1498a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1498a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1498a-121">-InputObject</span></span>
<span data-ttu-id="1498a-122">Объект исправлений.</span><span class="sxs-lookup"><span data-stu-id="1498a-122">The Remediation object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1498a-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="1498a-123">-ManagementGroupName</span></span>
<span data-ttu-id="1498a-124">ИД группы управления.</span><span class="sxs-lookup"><span data-stu-id="1498a-124">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1498a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1498a-125">-Name</span></span>
<span data-ttu-id="1498a-126">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="1498a-126">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1498a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1498a-127">-PassThru</span></span>
<span data-ttu-id="1498a-128">Если команда успешно завершена, возвращается "Истина".</span><span class="sxs-lookup"><span data-stu-id="1498a-128">Return True if the command completes successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1498a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1498a-129">-ResourceGroupName</span></span>
<span data-ttu-id="1498a-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1498a-130">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1498a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1498a-131">-ResourceId</span></span>
<span data-ttu-id="1498a-132">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="1498a-132">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1498a-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="1498a-133">-Scope</span></span>
<span data-ttu-id="1498a-134">Область действия ресурса.</span><span class="sxs-lookup"><span data-stu-id="1498a-134">Scope of the resource.</span></span>
<span data-ttu-id="1498a-135">Например,</span><span class="sxs-lookup"><span data-stu-id="1498a-135">E.g.</span></span>
<span data-ttu-id="1498a-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="1498a-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1498a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1498a-137">-Confirm</span></span>
<span data-ttu-id="1498a-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1498a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1498a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1498a-139">-WhatIf</span></span>
<span data-ttu-id="1498a-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1498a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1498a-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1498a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1498a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1498a-142">CommonParameters</span></span>
<span data-ttu-id="1498a-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1498a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1498a-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1498a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1498a-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1498a-145">INPUTS</span></span>

### <span data-ttu-id="1498a-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1498a-146">System.String</span></span>

### <span data-ttu-id="1498a-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="1498a-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="1498a-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1498a-148">OUTPUTS</span></span>

### <span data-ttu-id="1498a-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1498a-149">System.Boolean</span></span>

## <span data-ttu-id="1498a-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1498a-150">NOTES</span></span>

## <span data-ttu-id="1498a-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1498a-151">RELATED LINKS</span></span>
