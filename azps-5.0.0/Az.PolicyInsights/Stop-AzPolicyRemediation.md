---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/stop-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Stop-AzPolicyRemediation.md
ms.openlocfilehash: 9dfb3ff2f50df7a858ab8194ec86fa312501dcff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246864"
---
# <span data-ttu-id="aa438-101">Stop-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="aa438-101">Stop-AzPolicyRemediation</span></span>

## <span data-ttu-id="aa438-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa438-102">SYNOPSIS</span></span>
<span data-ttu-id="aa438-103">Отмена выполняющегося исправления политики.</span><span class="sxs-lookup"><span data-stu-id="aa438-103">Cancels an in-progress policy remediation.</span></span>

## <span data-ttu-id="aa438-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa438-104">SYNTAX</span></span>

### <span data-ttu-id="aa438-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa438-105">ByName (Default)</span></span>
```
Stop-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa438-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aa438-106">ByResourceId</span></span>
```
Stop-AzPolicyRemediation -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa438-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aa438-107">ByInputObject</span></span>
```
Stop-AzPolicyRemediation -InputObject <PSRemediation> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa438-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa438-108">DESCRIPTION</span></span>
<span data-ttu-id="aa438-109">Командлет **Stop-AzPolicyRemediation** отменяет выполняющиеся исправления политики.</span><span class="sxs-lookup"><span data-stu-id="aa438-109">The **Stop-AzPolicyRemediation** cmdlet cancels an in-progress policy remediation.</span></span> <span data-ttu-id="aa438-110">Активные развертывания будут отменены, а новые развертывания создаваться не будут.</span><span class="sxs-lookup"><span data-stu-id="aa438-110">Active deployments will be canceled and no new deployments will be created.</span></span>

## <span data-ttu-id="aa438-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa438-111">EXAMPLES</span></span>

### <span data-ttu-id="aa438-112">Пример 1: отмена исправления политики в области "Группа ресурсов"</span><span class="sxs-lookup"><span data-stu-id="aa438-112">Example 1: Cancel a policy remediation at resource group scope</span></span>
```
PS C:\> Stop-AzPolicyRemediation -ResourceGroupName "myRG" -Name "remediation1"
```

<span data-ttu-id="aa438-113">Эта команда отменяет исправление с именем "remediation1" в группе ресурсов "myRG".</span><span class="sxs-lookup"><span data-stu-id="aa438-113">This command cancels the remediation named 'remediation1' in resource group 'myRG'.</span></span>

### <span data-ttu-id="aa438-114">Пример 2: отмена исправления группы управления с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="aa438-114">Example 2: Cancel a management group remediation via piping</span></span>
```
PS C:\> $remediation = Get-AzPolicyRemediation -ManagementGroupName "mg1" -Name "remediation1"
PS C:\> $remediation | Stop-AzPolicyRemediation
```

<span data-ttu-id="aa438-115">Эта команда отменяет исправление с именем "remediation1" в группе управления "MG1".</span><span class="sxs-lookup"><span data-stu-id="aa438-115">This command cancels the remediation named 'remediation1' in management group 'mg1'.</span></span>

## <span data-ttu-id="aa438-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa438-116">PARAMETERS</span></span>

### <span data-ttu-id="aa438-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa438-117">-AsJob</span></span>
<span data-ttu-id="aa438-118">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="aa438-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="aa438-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa438-119">-DefaultProfile</span></span>
<span data-ttu-id="aa438-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa438-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa438-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa438-121">-InputObject</span></span>
<span data-ttu-id="aa438-122">Объект исправления.</span><span class="sxs-lookup"><span data-stu-id="aa438-122">The Remediation object.</span></span>

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

### <span data-ttu-id="aa438-123">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="aa438-123">-ManagementGroupName</span></span>
<span data-ttu-id="aa438-124">Идентификатор группы управления.</span><span class="sxs-lookup"><span data-stu-id="aa438-124">Management group ID.</span></span>

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

### <span data-ttu-id="aa438-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa438-125">-Name</span></span>
<span data-ttu-id="aa438-126">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="aa438-126">Resource name.</span></span>

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

### <span data-ttu-id="aa438-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa438-127">-PassThru</span></span>
<span data-ttu-id="aa438-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="aa438-128">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="aa438-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa438-129">-ResourceGroupName</span></span>
<span data-ttu-id="aa438-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa438-130">Resource group name.</span></span>

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

### <span data-ttu-id="aa438-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa438-131">-ResourceId</span></span>
<span data-ttu-id="aa438-132">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="aa438-132">Resource ID.</span></span>

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

### <span data-ttu-id="aa438-133">-Scope</span><span class="sxs-lookup"><span data-stu-id="aa438-133">-Scope</span></span>
<span data-ttu-id="aa438-134">Область действия ресурса.</span><span class="sxs-lookup"><span data-stu-id="aa438-134">Scope of the resource.</span></span>
<span data-ttu-id="aa438-135">Сокращен.</span><span class="sxs-lookup"><span data-stu-id="aa438-135">E.g.</span></span>
<span data-ttu-id="aa438-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="aa438-136">'/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="aa438-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa438-137">-Confirm</span></span>
<span data-ttu-id="aa438-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa438-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa438-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa438-139">-WhatIf</span></span>
<span data-ttu-id="aa438-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa438-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa438-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa438-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa438-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa438-142">CommonParameters</span></span>
<span data-ttu-id="aa438-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa438-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa438-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa438-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa438-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa438-145">INPUTS</span></span>

### <span data-ttu-id="aa438-146">System. String</span><span class="sxs-lookup"><span data-stu-id="aa438-146">System.String</span></span>

### <span data-ttu-id="aa438-147">Microsoft. Azure. Commands. PolicyInsights. Models. unисправление. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="aa438-147">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="aa438-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa438-148">OUTPUTS</span></span>

### <span data-ttu-id="aa438-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa438-149">System.Boolean</span></span>

## <span data-ttu-id="aa438-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa438-150">NOTES</span></span>

## <span data-ttu-id="aa438-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa438-151">RELATED LINKS</span></span>
