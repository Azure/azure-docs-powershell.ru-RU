---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 956fcf09006e8e65d029bb5e380abc5de0e15c17
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399929"
---
# <span data-ttu-id="d39f0-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d39f0-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="d39f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d39f0-102">SYNOPSIS</span></span>
<span data-ttu-id="d39f0-103">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d39f0-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="d39f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d39f0-104">SYNTAX</span></span>

### <span data-ttu-id="d39f0-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d39f0-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39f0-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d39f0-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39f0-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d39f0-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d39f0-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d39f0-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d39f0-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d39f0-109">DESCRIPTION</span></span>
<span data-ttu-id="d39f0-110">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d39f0-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="d39f0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d39f0-111">EXAMPLES</span></span>

### <span data-ttu-id="d39f0-112">Пример 1. Удаление приложения по ид объекта</span><span class="sxs-lookup"><span data-stu-id="d39f0-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="d39f0-113">Удаляет приложение с ид объекта 'b4cd1619-80b3-4cfb-9f8f-9f233425738' из клиента.</span><span class="sxs-lookup"><span data-stu-id="d39f0-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="d39f0-114">Пример 2. Удаление приложения по ид приложения</span><span class="sxs-lookup"><span data-stu-id="d39f0-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="d39f0-115">Удаляет приложение с ид приложения f9c5ea4f-28f0-401a-a491-491a037fa346' из клиента.</span><span class="sxs-lookup"><span data-stu-id="d39f0-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="d39f0-116">Пример 3. Удаление приложения с помощью piping</span><span class="sxs-lookup"><span data-stu-id="d39f0-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="d39f0-117">Получает приложение с ид объекта 'b4cd1619-80b3-4cfb-9f8f-9f233425738' и каналами, которые до Remove-AzADApplication добираются до Remove-AzADApplication, чтобы удалить приложение из клиента.</span><span class="sxs-lookup"><span data-stu-id="d39f0-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="d39f0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d39f0-118">PARAMETERS</span></span>

### <span data-ttu-id="d39f0-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d39f0-119">-ApplicationId</span></span>
<span data-ttu-id="d39f0-120">ИД приложения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d39f0-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="d39f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d39f0-121">-DefaultProfile</span></span>
<span data-ttu-id="d39f0-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d39f0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d39f0-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d39f0-123">-DisplayName</span></span>
<span data-ttu-id="d39f0-124">Отображаемого имени приложения.</span><span class="sxs-lookup"><span data-stu-id="d39f0-124">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39f0-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d39f0-125">-Force</span></span>
<span data-ttu-id="d39f0-126">Переключение на удаление приложения без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d39f0-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="d39f0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d39f0-127">-InputObject</span></span>
<span data-ttu-id="d39f0-128">Объект, представляющий приложение, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d39f0-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d39f0-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d39f0-129">-ObjectId</span></span>
<span data-ttu-id="d39f0-130">ИД объекта приложения, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="d39f0-130">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39f0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d39f0-131">-PassThru</span></span>
<span data-ttu-id="d39f0-132">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="d39f0-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d39f0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d39f0-133">-Confirm</span></span>
<span data-ttu-id="d39f0-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d39f0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d39f0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d39f0-135">-WhatIf</span></span>
<span data-ttu-id="d39f0-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d39f0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d39f0-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d39f0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d39f0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d39f0-138">CommonParameters</span></span>
<span data-ttu-id="d39f0-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d39f0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d39f0-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d39f0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d39f0-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d39f0-141">INPUTS</span></span>

### <span data-ttu-id="d39f0-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d39f0-142">System.Guid</span></span>

### <span data-ttu-id="d39f0-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d39f0-143">System.String</span></span>

### <span data-ttu-id="d39f0-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d39f0-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="d39f0-145">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d39f0-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d39f0-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d39f0-146">OUTPUTS</span></span>

### <span data-ttu-id="d39f0-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d39f0-147">System.Boolean</span></span>

## <span data-ttu-id="d39f0-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d39f0-148">NOTES</span></span>
<span data-ttu-id="d39f0-149">Ключевые слова: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="d39f0-149">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d39f0-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d39f0-150">RELATED LINKS</span></span>

[<span data-ttu-id="d39f0-151">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d39f0-151">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="d39f0-152">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d39f0-152">Get-AzADApplication</span></span>](./Get-AzADApplication.md)


[<span data-ttu-id="d39f0-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d39f0-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

