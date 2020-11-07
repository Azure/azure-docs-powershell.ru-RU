---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 0fa6dde8584eb003bd479e9a73ec96176282d83c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905554"
---
# <span data-ttu-id="49ba4-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="49ba4-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="49ba4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="49ba4-103">Удаление субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="49ba4-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="49ba4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49ba4-104">SYNTAX</span></span>

### <span data-ttu-id="49ba4-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49ba4-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ba4-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ba4-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ba4-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ba4-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ba4-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ba4-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ba4-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ba4-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49ba4-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="49ba4-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ba4-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49ba4-111">DESCRIPTION</span></span>
<span data-ttu-id="49ba4-112">Удаление субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="49ba4-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="49ba4-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49ba4-113">EXAMPLES</span></span>

### <span data-ttu-id="49ba4-114">Пример 1: удаление субъекта-службы по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="49ba4-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="49ba4-115">Удаление субъекта-службы с идентификатором объекта "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45".</span><span class="sxs-lookup"><span data-stu-id="49ba4-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="49ba4-116">Пример 2: удаление субъекта-службы с помощью кода приложения</span><span class="sxs-lookup"><span data-stu-id="49ba4-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="49ba4-117">Удаление субъекта-службы с идентификатором приложения "9263469e-d328-4321-8646-3e3e75d20e76".</span><span class="sxs-lookup"><span data-stu-id="49ba4-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="49ba4-118">Пример 3: удаление субъекта-службы по имени участника-службы</span><span class="sxs-lookup"><span data-stu-id="49ba4-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="49ba4-119">Удаление субъекта-службы с именем субъекта-службы "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="49ba4-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="49ba4-120">Пример 4: удаление субъекта-службы с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="49ba4-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="49ba4-121">Возвращает субъекта-службы с идентификатором объекта "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" и каналами, которые должны быть удалены с помощью командлета Remove-AzADServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="49ba4-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="49ba4-122">Пример 5: удаление субъекта-службы путем передачи приложения по конвейеру</span><span class="sxs-lookup"><span data-stu-id="49ba4-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="49ba4-123">Возвращает приложение с ИД приложения "9263469e-d328-4321-8646-3e3e75d20e76" и каналами, которые должны быть связаны с командлетом Remove-AzADServicePrincipal, для удаления субъекта-службы, связанного с этим приложением.</span><span class="sxs-lookup"><span data-stu-id="49ba4-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="49ba4-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49ba4-124">PARAMETERS</span></span>

### <span data-ttu-id="49ba4-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="49ba4-125">-ApplicationId</span></span>
<span data-ttu-id="49ba4-126">Идентификатор приложения субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="49ba4-126">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ba4-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="49ba4-127">-ApplicationObject</span></span>
<span data-ttu-id="49ba4-128">Объект приложения, субъект-служба которого удаляется.</span><span class="sxs-lookup"><span data-stu-id="49ba4-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ba4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ba4-129">-DefaultProfile</span></span>
<span data-ttu-id="49ba4-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="49ba4-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49ba4-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="49ba4-131">-DisplayName</span></span>
<span data-ttu-id="49ba4-132">Отображаемое имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="49ba4-132">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ba4-133">-Force</span><span class="sxs-lookup"><span data-stu-id="49ba4-133">-Force</span></span>
<span data-ttu-id="49ba4-134">Переключиться в режим удаления субъекта-службы без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="49ba4-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="49ba4-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49ba4-135">-InputObject</span></span>
<span data-ttu-id="49ba4-136">Объект субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="49ba4-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49ba4-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="49ba4-137">-ObjectId</span></span>
<span data-ttu-id="49ba4-138">Идентификатор объекта субъекта-службы, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="49ba4-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ba4-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49ba4-139">-PassThru</span></span>
<span data-ttu-id="49ba4-140">Если указан, возвращает участника-службы.</span><span class="sxs-lookup"><span data-stu-id="49ba4-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="49ba4-141">-Намерено</span><span class="sxs-lookup"><span data-stu-id="49ba4-141">-ServicePrincipalName</span></span>
<span data-ttu-id="49ba4-142">Имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="49ba4-142">The service principal name.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ba4-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49ba4-143">-Confirm</span></span>
<span data-ttu-id="49ba4-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49ba4-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49ba4-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ba4-145">-WhatIf</span></span>
<span data-ttu-id="49ba4-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49ba4-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49ba4-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49ba4-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49ba4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ba4-148">CommonParameters</span></span>
<span data-ttu-id="49ba4-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49ba4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ba4-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ba4-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ba4-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49ba4-151">INPUTS</span></span>

### <span data-ttu-id="49ba4-152">System. String</span><span class="sxs-lookup"><span data-stu-id="49ba4-152">System.String</span></span>

### <span data-ttu-id="49ba4-153">System. GUID</span><span class="sxs-lookup"><span data-stu-id="49ba4-153">System.Guid</span></span>

### <span data-ttu-id="49ba4-154">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="49ba4-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="49ba4-155">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="49ba4-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="49ba4-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49ba4-156">OUTPUTS</span></span>

### <span data-ttu-id="49ba4-157">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="49ba4-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="49ba4-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="49ba4-158">NOTES</span></span>
<span data-ttu-id="49ba4-159">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="49ba4-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="49ba4-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49ba4-160">RELATED LINKS</span></span>

[<span data-ttu-id="49ba4-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="49ba4-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="49ba4-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="49ba4-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="49ba4-163">Set-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="49ba4-163">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="49ba4-164">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="49ba4-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="49ba4-165">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="49ba4-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
