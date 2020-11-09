---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 7f306503754ca945ab4abb001cf08f8574b67025
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245886"
---
# <span data-ttu-id="3150b-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3150b-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="3150b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3150b-102">SYNOPSIS</span></span>
<span data-ttu-id="3150b-103">Удаление субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3150b-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="3150b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3150b-104">SYNTAX</span></span>

### <span data-ttu-id="3150b-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3150b-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3150b-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3150b-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3150b-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="3150b-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3150b-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3150b-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3150b-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3150b-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3150b-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3150b-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3150b-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3150b-111">DESCRIPTION</span></span>
<span data-ttu-id="3150b-112">Удаление субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3150b-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="3150b-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3150b-113">EXAMPLES</span></span>

### <span data-ttu-id="3150b-114">Пример 1: удаление субъекта-службы по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="3150b-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="3150b-115">Удаление субъекта-службы с идентификатором объекта "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45".</span><span class="sxs-lookup"><span data-stu-id="3150b-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="3150b-116">Пример 2: удаление субъекта-службы с помощью кода приложения</span><span class="sxs-lookup"><span data-stu-id="3150b-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="3150b-117">Удаление субъекта-службы с идентификатором приложения "9263469e-d328-4321-8646-3e3e75d20e76".</span><span class="sxs-lookup"><span data-stu-id="3150b-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="3150b-118">Пример 3: удаление субъекта-службы по имени участника-службы</span><span class="sxs-lookup"><span data-stu-id="3150b-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="3150b-119">Удаление субъекта-службы с именем субъекта-службы "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="3150b-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="3150b-120">Пример 4: удаление субъекта-службы с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="3150b-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="3150b-121">Возвращает субъекта-службы с идентификатором объекта "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" и каналами, которые должны быть удалены с помощью командлета Remove-AzADServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="3150b-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="3150b-122">Пример 5: удаление субъекта-службы путем передачи приложения по конвейеру</span><span class="sxs-lookup"><span data-stu-id="3150b-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="3150b-123">Возвращает приложение с ИД приложения "9263469e-d328-4321-8646-3e3e75d20e76" и каналами, которые должны быть связаны с командлетом Remove-AzADServicePrincipal, для удаления субъекта-службы, связанного с этим приложением.</span><span class="sxs-lookup"><span data-stu-id="3150b-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="3150b-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3150b-124">PARAMETERS</span></span>

### <span data-ttu-id="3150b-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3150b-125">-ApplicationId</span></span>
<span data-ttu-id="3150b-126">Идентификатор приложения субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="3150b-126">The service principal application id.</span></span>

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

### <span data-ttu-id="3150b-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="3150b-127">-ApplicationObject</span></span>
<span data-ttu-id="3150b-128">Объект приложения, субъект-служба которого удаляется.</span><span class="sxs-lookup"><span data-stu-id="3150b-128">The application object whose service principal is being removed.</span></span>

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

### <span data-ttu-id="3150b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3150b-129">-DefaultProfile</span></span>
<span data-ttu-id="3150b-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3150b-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3150b-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3150b-131">-DisplayName</span></span>
<span data-ttu-id="3150b-132">Отображаемое имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="3150b-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="3150b-133">-Force</span><span class="sxs-lookup"><span data-stu-id="3150b-133">-Force</span></span>
<span data-ttu-id="3150b-134">Переключиться в режим удаления субъекта-службы без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="3150b-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="3150b-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3150b-135">-InputObject</span></span>
<span data-ttu-id="3150b-136">Объект субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="3150b-136">The service principal object.</span></span>

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

### <span data-ttu-id="3150b-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3150b-137">-ObjectId</span></span>
<span data-ttu-id="3150b-138">Идентификатор объекта субъекта-службы, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3150b-138">The object id of the service principal to delete.</span></span>

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

### <span data-ttu-id="3150b-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3150b-139">-PassThru</span></span>
<span data-ttu-id="3150b-140">Если указан, возвращает участника-службы.</span><span class="sxs-lookup"><span data-stu-id="3150b-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="3150b-141">-Намерено</span><span class="sxs-lookup"><span data-stu-id="3150b-141">-ServicePrincipalName</span></span>
<span data-ttu-id="3150b-142">Имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="3150b-142">The service principal name.</span></span>

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

### <span data-ttu-id="3150b-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3150b-143">-Confirm</span></span>
<span data-ttu-id="3150b-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3150b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3150b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3150b-145">-WhatIf</span></span>
<span data-ttu-id="3150b-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3150b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3150b-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3150b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3150b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3150b-148">CommonParameters</span></span>
<span data-ttu-id="3150b-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3150b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3150b-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3150b-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3150b-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3150b-151">INPUTS</span></span>

### <span data-ttu-id="3150b-152">System. String</span><span class="sxs-lookup"><span data-stu-id="3150b-152">System.String</span></span>

### <span data-ttu-id="3150b-153">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3150b-153">System.Guid</span></span>

### <span data-ttu-id="3150b-154">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3150b-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="3150b-155">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="3150b-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="3150b-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3150b-156">OUTPUTS</span></span>

### <span data-ttu-id="3150b-157">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3150b-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="3150b-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="3150b-158">NOTES</span></span>
<span data-ttu-id="3150b-159">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="3150b-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3150b-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3150b-160">RELATED LINKS</span></span>

[<span data-ttu-id="3150b-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3150b-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="3150b-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3150b-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="3150b-163">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3150b-163">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="3150b-164">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="3150b-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="3150b-165">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="3150b-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)