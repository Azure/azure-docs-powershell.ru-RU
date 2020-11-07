---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d558e7104027e4c3fcef3b6e8d8427d5fd3802fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734298"
---
# <span data-ttu-id="d3586-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="d3586-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="d3586-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3586-102">SYNOPSIS</span></span>
<span data-ttu-id="d3586-103">Изменение определения Set политики</span><span class="sxs-lookup"><span data-stu-id="d3586-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3586-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3586-104">SYNTAX</span></span>

### <span data-ttu-id="d3586-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3586-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3586-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3586-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3586-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3586-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3586-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3586-108">IdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3586-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3586-109">DESCRIPTION</span></span>
<span data-ttu-id="d3586-110">Командлет **Set-AzureRmPolicySetDefinition** изменяет определение политики.</span><span class="sxs-lookup"><span data-stu-id="d3586-110">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="d3586-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3586-111">EXAMPLES</span></span>

### <span data-ttu-id="d3586-112">Пример 1: Обновление описания определения набора политик</span><span class="sxs-lookup"><span data-stu-id="d3586-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="d3586-113">Первая команда получает определение политики с помощью командлета Get-AzureRmPolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="d3586-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="d3586-114">Команда сохраняет этот объект в переменной $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="d3586-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="d3586-115">Вторая команда обновляет описание определения политики, определяемое свойством **ResourceId** для $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="d3586-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="d3586-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3586-116">PARAMETERS</span></span>

### <span data-ttu-id="d3586-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d3586-117">-ApiVersion</span></span>
<span data-ttu-id="d3586-118">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d3586-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d3586-119">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="d3586-119">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3586-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3586-120">-DefaultProfile</span></span>
<span data-ttu-id="d3586-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d3586-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3586-122">-Описание</span><span class="sxs-lookup"><span data-stu-id="d3586-122">-Description</span></span>
<span data-ttu-id="d3586-123">Описание определения политики.</span><span class="sxs-lookup"><span data-stu-id="d3586-123">The description for policy set definition.</span></span>

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

### <span data-ttu-id="d3586-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d3586-124">-DisplayName</span></span>
<span data-ttu-id="d3586-125">Отображаемое имя определения множества политик.</span><span class="sxs-lookup"><span data-stu-id="d3586-125">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="d3586-126">-ID</span><span class="sxs-lookup"><span data-stu-id="d3586-126">-Id</span></span>
<span data-ttu-id="d3586-127">Полный идентификатор определения политики, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="d3586-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="d3586-128">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="d3586-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3586-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d3586-129">-ManagementGroupName</span></span>
<span data-ttu-id="d3586-130">Имя группы управления для определения политики, которую требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="d3586-130">The name of the management group of the policy set definition to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3586-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d3586-131">-Metadata</span></span>
<span data-ttu-id="d3586-132">Метаданные определения обновленного набора политик.</span><span class="sxs-lookup"><span data-stu-id="d3586-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="d3586-133">Это может быть либо путь к имени файла, содержащему метаданные, либо метаданные в виде строки.</span><span class="sxs-lookup"><span data-stu-id="d3586-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="d3586-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d3586-134">-Name</span></span>
<span data-ttu-id="d3586-135">Имя определения настройки политики.</span><span class="sxs-lookup"><span data-stu-id="d3586-135">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3586-136">-Параметр</span><span class="sxs-lookup"><span data-stu-id="d3586-136">-Parameter</span></span>
<span data-ttu-id="d3586-137">Объявление параметров обновленного определения набора политик.</span><span class="sxs-lookup"><span data-stu-id="d3586-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="d3586-138">Это может быть путь к имени файла или универсальному коду ресурса (URI), содержащему объявление параметров, или объявление параметров в виде строки.</span><span class="sxs-lookup"><span data-stu-id="d3586-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

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

### <span data-ttu-id="d3586-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d3586-139">-PolicyDefinition</span></span>
<span data-ttu-id="d3586-140">Определение настройки политики.</span><span class="sxs-lookup"><span data-stu-id="d3586-140">The policy set definition.</span></span> <span data-ttu-id="d3586-141">Это может быть путь к имени файла, содержащему определения политики, или определению политики как String.</span><span class="sxs-lookup"><span data-stu-id="d3586-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="d3586-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="d3586-142">-Pre</span></span>
<span data-ttu-id="d3586-143">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="d3586-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d3586-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3586-144">-SubscriptionId</span></span>
<span data-ttu-id="d3586-145">Идентификатор подписки для определения политики, которую требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="d3586-145">The subscription ID of the policy set definition to update.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3586-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3586-146">-Confirm</span></span>
<span data-ttu-id="d3586-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d3586-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3586-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3586-148">-WhatIf</span></span>
<span data-ttu-id="d3586-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d3586-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3586-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d3586-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3586-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3586-151">CommonParameters</span></span>
<span data-ttu-id="d3586-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3586-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3586-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3586-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3586-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3586-154">INPUTS</span></span>

### <span data-ttu-id="d3586-155">System. String</span><span class="sxs-lookup"><span data-stu-id="d3586-155">System.String</span></span>

### <span data-ttu-id="d3586-156">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d3586-156">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d3586-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3586-157">OUTPUTS</span></span>

### <span data-ttu-id="d3586-158">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d3586-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d3586-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3586-159">NOTES</span></span>

## <span data-ttu-id="d3586-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3586-160">RELATED LINKS</span></span>
