---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 7f306503754ca945ab4abb001cf08f8574b67025
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412431"
---
# <span data-ttu-id="8fd34-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8fd34-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="8fd34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fd34-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd34-103">Удаляет главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8fd34-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="8fd34-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8fd34-104">SYNTAX</span></span>

### <span data-ttu-id="8fd34-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8fd34-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd34-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fd34-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd34-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fd34-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd34-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fd34-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd34-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fd34-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd34-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fd34-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fd34-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8fd34-111">DESCRIPTION</span></span>
<span data-ttu-id="8fd34-112">Удаляет главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8fd34-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="8fd34-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8fd34-113">EXAMPLES</span></span>

### <span data-ttu-id="8fd34-114">Пример 1. Удаление главной службы по ид объекта</span><span class="sxs-lookup"><span data-stu-id="8fd34-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="8fd34-115">Удаляет главную службу с ид объекта '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span><span class="sxs-lookup"><span data-stu-id="8fd34-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="8fd34-116">Пример 2. Удаление основного обслуживания по ид приложения</span><span class="sxs-lookup"><span data-stu-id="8fd34-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="8fd34-117">Удаляет главную службу с помощью ИД приложения "9263469e-d328-4321-8646-3e3e75d20e76".</span><span class="sxs-lookup"><span data-stu-id="8fd34-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="8fd34-118">Пример 3. Удаление основной услуги по SPN</span><span class="sxs-lookup"><span data-stu-id="8fd34-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="8fd34-119">Удаление директора-службы с именем "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="8fd34-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="8fd34-120">Пример 4. Удаление основного обслуживания с помощью piping</span><span class="sxs-lookup"><span data-stu-id="8fd34-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="8fd34-121">Получает главную службу с ид объекта '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' и каналами, которые до Remove-AzADServicePrincipal-управления, чтобы удалить эту главную службу.</span><span class="sxs-lookup"><span data-stu-id="8fd34-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="8fd34-122">Пример 5. Удаление основного обслуживания путем перенакладки приложения</span><span class="sxs-lookup"><span data-stu-id="8fd34-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="8fd34-123">Получает приложение с ИД приложения 9263469e-d328-4321-8646-3e3e75d20e76' и каналами, которые до Remove-AzADServicePrincipal-управления, чтобы удалить главную службу, связанную с этим приложением.</span><span class="sxs-lookup"><span data-stu-id="8fd34-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="8fd34-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fd34-124">PARAMETERS</span></span>

### <span data-ttu-id="8fd34-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8fd34-125">-ApplicationId</span></span>
<span data-ttu-id="8fd34-126">ИД приложения-службы.</span><span class="sxs-lookup"><span data-stu-id="8fd34-126">The service principal application id.</span></span>

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

### <span data-ttu-id="8fd34-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="8fd34-127">-ApplicationObject</span></span>
<span data-ttu-id="8fd34-128">Объект приложения, главную службу которого удаляется.</span><span class="sxs-lookup"><span data-stu-id="8fd34-128">The application object whose service principal is being removed.</span></span>

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

### <span data-ttu-id="8fd34-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd34-129">-DefaultProfile</span></span>
<span data-ttu-id="8fd34-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8fd34-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fd34-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8fd34-131">-DisplayName</span></span>
<span data-ttu-id="8fd34-132">Отображаемая имя директора-службы.</span><span class="sxs-lookup"><span data-stu-id="8fd34-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="8fd34-133">-Force</span><span class="sxs-lookup"><span data-stu-id="8fd34-133">-Force</span></span>
<span data-ttu-id="8fd34-134">Перейти к удалите главную службу без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8fd34-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="8fd34-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fd34-135">-InputObject</span></span>
<span data-ttu-id="8fd34-136">Объект-служба.</span><span class="sxs-lookup"><span data-stu-id="8fd34-136">The service principal object.</span></span>

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

### <span data-ttu-id="8fd34-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8fd34-137">-ObjectId</span></span>
<span data-ttu-id="8fd34-138">Object id of the service principal to delete.</span><span class="sxs-lookup"><span data-stu-id="8fd34-138">The object id of the service principal to delete.</span></span>

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

### <span data-ttu-id="8fd34-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fd34-139">-PassThru</span></span>
<span data-ttu-id="8fd34-140">Если указано, возвращает удаленную главную службу.</span><span class="sxs-lookup"><span data-stu-id="8fd34-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="8fd34-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8fd34-141">-ServicePrincipalName</span></span>
<span data-ttu-id="8fd34-142">Имя директора-службы.</span><span class="sxs-lookup"><span data-stu-id="8fd34-142">The service principal name.</span></span>

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

### <span data-ttu-id="8fd34-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fd34-143">-Confirm</span></span>
<span data-ttu-id="8fd34-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fd34-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fd34-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd34-145">-WhatIf</span></span>
<span data-ttu-id="8fd34-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fd34-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd34-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8fd34-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fd34-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd34-148">CommonParameters</span></span>
<span data-ttu-id="8fd34-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd34-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd34-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fd34-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd34-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fd34-151">INPUTS</span></span>

### <span data-ttu-id="8fd34-152">System.String</span><span class="sxs-lookup"><span data-stu-id="8fd34-152">System.String</span></span>

### <span data-ttu-id="8fd34-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="8fd34-153">System.Guid</span></span>

### <span data-ttu-id="8fd34-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8fd34-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="8fd34-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="8fd34-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="8fd34-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8fd34-156">OUTPUTS</span></span>

### <span data-ttu-id="8fd34-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8fd34-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="8fd34-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8fd34-158">NOTES</span></span>
<span data-ttu-id="8fd34-159">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="8fd34-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8fd34-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8fd34-160">RELATED LINKS</span></span>

[<span data-ttu-id="8fd34-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8fd34-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="8fd34-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8fd34-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="8fd34-163">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8fd34-163">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="8fd34-164">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8fd34-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="8fd34-165">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8fd34-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
