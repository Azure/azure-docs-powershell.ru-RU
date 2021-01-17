---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: e27dcc838499e742c887f60a30021d8ac99277f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412436"
---
# <span data-ttu-id="dc539-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="dc539-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="dc539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc539-102">SYNOPSIS</span></span>
<span data-ttu-id="dc539-103">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dc539-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="dc539-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc539-104">SYNTAX</span></span>

### <span data-ttu-id="dc539-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc539-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc539-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc539-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc539-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc539-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc539-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc539-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc539-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc539-109">DESCRIPTION</span></span>
<span data-ttu-id="dc539-110">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dc539-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="dc539-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc539-111">EXAMPLES</span></span>

### <span data-ttu-id="dc539-112">Пример 1. Удаление приложения по ид объекта</span><span class="sxs-lookup"><span data-stu-id="dc539-112">Example 1: Remove application by object id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="dc539-113">Удаляет приложение с ид объекта 'b4cd1619-80b3-4cfb-9f8f-9f233425738' из клиента.</span><span class="sxs-lookup"><span data-stu-id="dc539-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="dc539-114">Пример 2. Удаление приложения по его ид</span><span class="sxs-lookup"><span data-stu-id="dc539-114">Example 2: Remove application by application id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="dc539-115">Удаляет приложение с ид приложения "f9c5ea4f-28f0-401a-a491-491a037fa346" из клиента.</span><span class="sxs-lookup"><span data-stu-id="dc539-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="dc539-116">Пример 3. Удаление приложения с помощью piping</span><span class="sxs-lookup"><span data-stu-id="dc539-116">Example 3: Remove application by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="dc539-117">Получает приложение с ид объекта 'b4cd1619-80b3-4cfb-9f8f-9f233425738' и каналами, которые до Remove-AzADApplication можно удалить приложение из клиента.</span><span class="sxs-lookup"><span data-stu-id="dc539-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="dc539-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc539-118">PARAMETERS</span></span>

### <span data-ttu-id="dc539-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dc539-119">-ApplicationId</span></span>
<span data-ttu-id="dc539-120">ИД приложения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="dc539-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="dc539-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc539-121">-DefaultProfile</span></span>
<span data-ttu-id="dc539-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dc539-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc539-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dc539-123">-DisplayName</span></span>
<span data-ttu-id="dc539-124">Отображаемого имени приложения.</span><span class="sxs-lookup"><span data-stu-id="dc539-124">The display name of the application.</span></span>

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

### <span data-ttu-id="dc539-125">-Force</span><span class="sxs-lookup"><span data-stu-id="dc539-125">-Force</span></span>
<span data-ttu-id="dc539-126">Переключение на удаление приложения без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="dc539-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="dc539-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc539-127">-InputObject</span></span>
<span data-ttu-id="dc539-128">Объект, представляющий приложение, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="dc539-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc539-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="dc539-129">-ObjectId</span></span>
<span data-ttu-id="dc539-130">ИД объекта приложения, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="dc539-130">The object id of the application to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc539-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc539-131">-PassThru</span></span>
<span data-ttu-id="dc539-132">Если эта команда была успешной, ее можно указать как истина.</span><span class="sxs-lookup"><span data-stu-id="dc539-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="dc539-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc539-133">-Confirm</span></span>
<span data-ttu-id="dc539-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dc539-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc539-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc539-135">-WhatIf</span></span>
<span data-ttu-id="dc539-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc539-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc539-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dc539-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc539-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc539-138">CommonParameters</span></span>
<span data-ttu-id="dc539-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc539-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc539-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc539-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc539-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc539-141">INPUTS</span></span>

### <span data-ttu-id="dc539-142">System.String</span><span class="sxs-lookup"><span data-stu-id="dc539-142">System.String</span></span>

### <span data-ttu-id="dc539-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="dc539-143">System.Guid</span></span>

### <span data-ttu-id="dc539-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="dc539-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="dc539-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc539-145">OUTPUTS</span></span>

### <span data-ttu-id="dc539-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc539-146">System.Boolean</span></span>

## <span data-ttu-id="dc539-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc539-147">NOTES</span></span>
<span data-ttu-id="dc539-148">Ключевые слова: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="dc539-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="dc539-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc539-149">RELATED LINKS</span></span>

[<span data-ttu-id="dc539-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="dc539-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="dc539-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="dc539-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="dc539-152">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="dc539-152">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

[<span data-ttu-id="dc539-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="dc539-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

