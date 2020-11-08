---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: e27dcc838499e742c887f60a30021d8ac99277f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246554"
---
# <span data-ttu-id="a214c-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a214c-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="a214c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a214c-102">SYNOPSIS</span></span>
<span data-ttu-id="a214c-103">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a214c-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="a214c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a214c-104">SYNTAX</span></span>

### <span data-ttu-id="a214c-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a214c-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a214c-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a214c-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a214c-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a214c-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a214c-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a214c-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a214c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a214c-109">DESCRIPTION</span></span>
<span data-ttu-id="a214c-110">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a214c-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="a214c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a214c-111">EXAMPLES</span></span>

### <span data-ttu-id="a214c-112">Пример 1: Удаление приложения по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="a214c-112">Example 1: Remove application by object id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="a214c-113">Удаляет приложение с идентификатором объекта "b4cd1619-80b3-4cfb-9f8f-9f2333425738" из клиента.</span><span class="sxs-lookup"><span data-stu-id="a214c-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="a214c-114">Пример 2: Удаление приложения по идентификатору приложения</span><span class="sxs-lookup"><span data-stu-id="a214c-114">Example 2: Remove application by application id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="a214c-115">Удаляет приложение с идентификатором приложения "f9c5ea4f-28f0-401A-a491-491a037fa346" из клиента.</span><span class="sxs-lookup"><span data-stu-id="a214c-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="a214c-116">Пример 3: Удаление приложения с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="a214c-116">Example 3: Remove application by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="a214c-117">Возвращает приложение с идентификатором объекта "b4cd1619-80b3-4cfb-9f8f-9f2333425738" и каналами, которые должны быть удалены из клиента с помощью командлета Remove-AzADApplication.</span><span class="sxs-lookup"><span data-stu-id="a214c-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="a214c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a214c-118">PARAMETERS</span></span>

### <span data-ttu-id="a214c-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a214c-119">-ApplicationId</span></span>
<span data-ttu-id="a214c-120">Идентификатор приложения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a214c-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="a214c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a214c-121">-DefaultProfile</span></span>
<span data-ttu-id="a214c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a214c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a214c-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a214c-123">-DisplayName</span></span>
<span data-ttu-id="a214c-124">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="a214c-124">The display name of the application.</span></span>

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

### <span data-ttu-id="a214c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a214c-125">-Force</span></span>
<span data-ttu-id="a214c-126">Переключение на удаление приложения без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a214c-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="a214c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a214c-127">-InputObject</span></span>
<span data-ttu-id="a214c-128">Объект, представляющий приложение, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a214c-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="a214c-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a214c-129">-ObjectId</span></span>
<span data-ttu-id="a214c-130">Идентификатор объекта приложения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a214c-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="a214c-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a214c-131">-PassThru</span></span>
<span data-ttu-id="a214c-132">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a214c-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a214c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a214c-133">-Confirm</span></span>
<span data-ttu-id="a214c-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a214c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a214c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a214c-135">-WhatIf</span></span>
<span data-ttu-id="a214c-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a214c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a214c-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a214c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a214c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a214c-138">CommonParameters</span></span>
<span data-ttu-id="a214c-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a214c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a214c-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a214c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a214c-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a214c-141">INPUTS</span></span>

### <span data-ttu-id="a214c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a214c-142">System.String</span></span>

### <span data-ttu-id="a214c-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a214c-143">System.Guid</span></span>

### <span data-ttu-id="a214c-144">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a214c-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="a214c-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a214c-145">OUTPUTS</span></span>

### <span data-ttu-id="a214c-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a214c-146">System.Boolean</span></span>

## <span data-ttu-id="a214c-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="a214c-147">NOTES</span></span>
<span data-ttu-id="a214c-148">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="a214c-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a214c-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a214c-149">RELATED LINKS</span></span>

[<span data-ttu-id="a214c-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a214c-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="a214c-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a214c-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="a214c-152">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a214c-152">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

[<span data-ttu-id="a214c-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a214c-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

