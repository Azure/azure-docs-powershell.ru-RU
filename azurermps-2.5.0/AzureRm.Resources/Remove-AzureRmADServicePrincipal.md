---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 462acabd83090a893119d94d93fd767907c5144b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913273"
---
# <span data-ttu-id="2fade-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2fade-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="2fade-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fade-102">SYNOPSIS</span></span>
<span data-ttu-id="2fade-103">Удаление субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2fade-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fade-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fade-104">SYNTAX</span></span>

### <span data-ttu-id="2fade-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2fade-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fade-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fade-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fade-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fade-107">SPNParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fade-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fade-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fade-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fade-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fade-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fade-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fade-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fade-111">DESCRIPTION</span></span>
<span data-ttu-id="2fade-112">Удаление субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2fade-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="2fade-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fade-113">EXAMPLES</span></span>

### <span data-ttu-id="2fade-114">Пример 1: удаление субъекта-службы по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="2fade-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="2fade-115">Удаление субъекта-службы с идентификатором объекта "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45".</span><span class="sxs-lookup"><span data-stu-id="2fade-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="2fade-116">Пример 2: удаление субъекта-службы с помощью кода приложения</span><span class="sxs-lookup"><span data-stu-id="2fade-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="2fade-117">Удаление субъекта-службы с идентификатором приложения "9263469e-d328-4321-8646-3e3e75d20e76".</span><span class="sxs-lookup"><span data-stu-id="2fade-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="2fade-118">Пример 3: удаление субъекта-службы по имени участника-службы</span><span class="sxs-lookup"><span data-stu-id="2fade-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="2fade-119">Удаление субъекта-службы с именем субъекта-службы "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="2fade-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="2fade-120">Пример 4: удаление субъекта-службы с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="2fade-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="2fade-121">Возвращает субъекта-службы с идентификатором объекта "61b5d8ea-fdc6-40a2-8d5b-ad447c678d45" и каналами, которые должны быть удалены с помощью командлета Remove-AzureRmADServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="2fade-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="2fade-122">Пример 5: удаление субъекта-службы путем передачи приложения по конвейеру</span><span class="sxs-lookup"><span data-stu-id="2fade-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzureRmApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="2fade-123">Возвращает приложение с ИД приложения "9263469e-d328-4321-8646-3e3e75d20e76" и каналами, которые должны быть связаны с командлетом Remove-AzureRmADServicePrincipal, для удаления субъекта-службы, связанного с этим приложением.</span><span class="sxs-lookup"><span data-stu-id="2fade-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="2fade-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fade-124">PARAMETERS</span></span>

### <span data-ttu-id="2fade-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2fade-125">-ApplicationId</span></span>
<span data-ttu-id="2fade-126">Идентификатор приложения субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="2fade-126">The service principal application id.</span></span>

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

### <span data-ttu-id="2fade-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="2fade-127">-ApplicationObject</span></span>
<span data-ttu-id="2fade-128">Объект приложения, субъект-служба которого удаляется.</span><span class="sxs-lookup"><span data-stu-id="2fade-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fade-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fade-129">-DefaultProfile</span></span>
<span data-ttu-id="2fade-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2fade-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fade-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2fade-131">-DisplayName</span></span>
<span data-ttu-id="2fade-132">Отображаемое имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="2fade-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="2fade-133">-Force</span><span class="sxs-lookup"><span data-stu-id="2fade-133">-Force</span></span>
<span data-ttu-id="2fade-134">Переключиться в режим удаления субъекта-службы без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2fade-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="2fade-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fade-135">-InputObject</span></span>
<span data-ttu-id="2fade-136">Объект субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="2fade-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fade-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2fade-137">-ObjectId</span></span>
<span data-ttu-id="2fade-138">Идентификатор объекта субъекта-службы, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2fade-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fade-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fade-139">-PassThru</span></span>
<span data-ttu-id="2fade-140">Если указан, возвращает участника-службы.</span><span class="sxs-lookup"><span data-stu-id="2fade-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="2fade-141">-Намерено</span><span class="sxs-lookup"><span data-stu-id="2fade-141">-ServicePrincipalName</span></span>
<span data-ttu-id="2fade-142">Имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="2fade-142">The service principal name.</span></span>

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

### <span data-ttu-id="2fade-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fade-143">-Confirm</span></span>
<span data-ttu-id="2fade-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2fade-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fade-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fade-145">-WhatIf</span></span>
<span data-ttu-id="2fade-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2fade-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fade-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fade-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fade-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fade-148">CommonParameters</span></span>
<span data-ttu-id="2fade-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fade-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fade-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fade-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fade-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fade-151">INPUTS</span></span>

### <span data-ttu-id="2fade-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2fade-152">System.Guid</span></span>

### <span data-ttu-id="2fade-153">System. String</span><span class="sxs-lookup"><span data-stu-id="2fade-153">System.String</span></span>

### <span data-ttu-id="2fade-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2fade-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="2fade-155">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2fade-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2fade-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="2fade-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="2fade-157">Параметры: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2fade-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="2fade-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fade-158">OUTPUTS</span></span>

### <span data-ttu-id="2fade-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2fade-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="2fade-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fade-160">NOTES</span></span>
<span data-ttu-id="2fade-161">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="2fade-161">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="2fade-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fade-162">RELATED LINKS</span></span>

[<span data-ttu-id="2fade-163">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2fade-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="2fade-164">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2fade-164">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



[<span data-ttu-id="2fade-165">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="2fade-165">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="2fade-166">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2fade-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
