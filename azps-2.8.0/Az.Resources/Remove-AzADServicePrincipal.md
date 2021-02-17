---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 2658e5ff70603cb9bbe3aa3a7ccd47713249c726
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413495"
---
# <span data-ttu-id="7605e-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7605e-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="7605e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7605e-102">SYNOPSIS</span></span>
<span data-ttu-id="7605e-103">Удаляет главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7605e-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="7605e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7605e-104">SYNTAX</span></span>

### <span data-ttu-id="7605e-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7605e-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7605e-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7605e-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7605e-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="7605e-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7605e-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7605e-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7605e-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7605e-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7605e-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7605e-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7605e-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7605e-111">DESCRIPTION</span></span>
<span data-ttu-id="7605e-112">Удаляет главную службу Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7605e-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="7605e-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7605e-113">EXAMPLES</span></span>

### <span data-ttu-id="7605e-114">Пример 1. Удаление главной службы по ид объекта</span><span class="sxs-lookup"><span data-stu-id="7605e-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="7605e-115">Удаляет главную службу с ид объекта '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span><span class="sxs-lookup"><span data-stu-id="7605e-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="7605e-116">Пример 2. Удаление основного обслуживания по ид приложения</span><span class="sxs-lookup"><span data-stu-id="7605e-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="7605e-117">Удаляет главную службу с помощью ИД приложения "9263469e-d328-4321-8646-3e3e75d20e76".</span><span class="sxs-lookup"><span data-stu-id="7605e-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="7605e-118">Пример 3. Удаление основного обслуживания по SPN</span><span class="sxs-lookup"><span data-stu-id="7605e-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="7605e-119">Удаление директора-службы с именем "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="7605e-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="7605e-120">Пример 4. Удаление основного обслуживания с помощью piping</span><span class="sxs-lookup"><span data-stu-id="7605e-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="7605e-121">Получает главную службу с ид объекта '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' и каналами, которые до Remove-AzADServicePrincipal-управления, чтобы удалить эту главную службу.</span><span class="sxs-lookup"><span data-stu-id="7605e-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="7605e-122">Пример 5. Удаление основного обслуживания путем перенакладки приложения</span><span class="sxs-lookup"><span data-stu-id="7605e-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="7605e-123">Получает приложение с ИД приложения 9263469e-d328-4321-8646-3e3e75d20e76' и каналами, которые до Remove-AzADServicePrincipal-управления, чтобы удалить главную службу, связанную с этим приложением.</span><span class="sxs-lookup"><span data-stu-id="7605e-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="7605e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7605e-124">PARAMETERS</span></span>

### <span data-ttu-id="7605e-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7605e-125">-ApplicationId</span></span>
<span data-ttu-id="7605e-126">ИД приложения-службы.</span><span class="sxs-lookup"><span data-stu-id="7605e-126">The service principal application id.</span></span>

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

### <span data-ttu-id="7605e-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="7605e-127">-ApplicationObject</span></span>
<span data-ttu-id="7605e-128">Объект приложения, главную службу которого удаляется.</span><span class="sxs-lookup"><span data-stu-id="7605e-128">The application object whose service principal is being removed.</span></span>

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

### <span data-ttu-id="7605e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7605e-129">-DefaultProfile</span></span>
<span data-ttu-id="7605e-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7605e-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7605e-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7605e-131">-DisplayName</span></span>
<span data-ttu-id="7605e-132">Отображаемая имя директора-службы.</span><span class="sxs-lookup"><span data-stu-id="7605e-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="7605e-133">-Force</span><span class="sxs-lookup"><span data-stu-id="7605e-133">-Force</span></span>
<span data-ttu-id="7605e-134">Перейти к удалите главную службу без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7605e-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="7605e-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7605e-135">-InputObject</span></span>
<span data-ttu-id="7605e-136">Объект-служба.</span><span class="sxs-lookup"><span data-stu-id="7605e-136">The service principal object.</span></span>

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

### <span data-ttu-id="7605e-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7605e-137">-ObjectId</span></span>
<span data-ttu-id="7605e-138">Object Id of the service principal to delete.</span><span class="sxs-lookup"><span data-stu-id="7605e-138">The object id of the service principal to delete.</span></span>

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

### <span data-ttu-id="7605e-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7605e-139">-PassThru</span></span>
<span data-ttu-id="7605e-140">Если указано, возвращает удаленную главную службу.</span><span class="sxs-lookup"><span data-stu-id="7605e-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="7605e-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7605e-141">-ServicePrincipalName</span></span>
<span data-ttu-id="7605e-142">Имя директора-службы.</span><span class="sxs-lookup"><span data-stu-id="7605e-142">The service principal name.</span></span>

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

### <span data-ttu-id="7605e-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7605e-143">-Confirm</span></span>
<span data-ttu-id="7605e-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7605e-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7605e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7605e-145">-WhatIf</span></span>
<span data-ttu-id="7605e-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7605e-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7605e-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7605e-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7605e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7605e-148">CommonParameters</span></span>
<span data-ttu-id="7605e-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7605e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7605e-150">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7605e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7605e-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7605e-151">INPUTS</span></span>

### <span data-ttu-id="7605e-152">System.String</span><span class="sxs-lookup"><span data-stu-id="7605e-152">System.String</span></span>

### <span data-ttu-id="7605e-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7605e-153">System.Guid</span></span>

### <span data-ttu-id="7605e-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7605e-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="7605e-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="7605e-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="7605e-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7605e-156">OUTPUTS</span></span>

### <span data-ttu-id="7605e-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7605e-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="7605e-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7605e-158">NOTES</span></span>
<span data-ttu-id="7605e-159">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="7605e-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7605e-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7605e-160">RELATED LINKS</span></span>

[<span data-ttu-id="7605e-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7605e-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="7605e-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7605e-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)


[<span data-ttu-id="7605e-163">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7605e-163">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="7605e-164">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7605e-164">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
