---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: eed437a235072972778925c0b94f2d22466399b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905561"
---
# <span data-ttu-id="b934e-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b934e-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="b934e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b934e-102">SYNOPSIS</span></span>
<span data-ttu-id="b934e-103">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b934e-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="b934e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b934e-104">SYNTAX</span></span>

### <span data-ttu-id="b934e-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b934e-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b934e-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b934e-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b934e-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b934e-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b934e-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b934e-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b934e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b934e-109">DESCRIPTION</span></span>
<span data-ttu-id="b934e-110">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b934e-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="b934e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b934e-111">EXAMPLES</span></span>

### <span data-ttu-id="b934e-112">Пример 1: Удаление приложения по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="b934e-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="b934e-113">Удаляет приложение с идентификатором объекта "b4cd1619-80b3-4cfb-9f8f-9f2333425738" из клиента.</span><span class="sxs-lookup"><span data-stu-id="b934e-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="b934e-114">Пример 2: Удаление приложения по идентификатору приложения</span><span class="sxs-lookup"><span data-stu-id="b934e-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="b934e-115">Удаляет приложение с идентификатором приложения "f9c5ea4f-28f0-401A-a491-491a037fa346" из клиента.</span><span class="sxs-lookup"><span data-stu-id="b934e-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="b934e-116">Пример 3-Удаление приложения с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="b934e-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="b934e-117">Возвращает приложение с идентификатором объекта "b4cd1619-80b3-4cfb-9f8f-9f2333425738" и каналами, которые должны быть удалены из клиента с помощью командлета Remove-AzADApplication.</span><span class="sxs-lookup"><span data-stu-id="b934e-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="b934e-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b934e-118">PARAMETERS</span></span>

### <span data-ttu-id="b934e-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b934e-119">-ApplicationId</span></span>
<span data-ttu-id="b934e-120">Идентификатор приложения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b934e-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="b934e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b934e-121">-DefaultProfile</span></span>
<span data-ttu-id="b934e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b934e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b934e-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b934e-123">-DisplayName</span></span>
<span data-ttu-id="b934e-124">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="b934e-124">The display name of the application.</span></span>

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

### <span data-ttu-id="b934e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b934e-125">-Force</span></span>
<span data-ttu-id="b934e-126">Переключение на удаление приложения без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b934e-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="b934e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b934e-127">-InputObject</span></span>
<span data-ttu-id="b934e-128">Объект, представляющий приложение, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b934e-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="b934e-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b934e-129">-ObjectId</span></span>
<span data-ttu-id="b934e-130">Идентификатор объекта приложения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b934e-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="b934e-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b934e-131">-PassThru</span></span>
<span data-ttu-id="b934e-132">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b934e-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b934e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b934e-133">-Confirm</span></span>
<span data-ttu-id="b934e-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b934e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b934e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b934e-135">-WhatIf</span></span>
<span data-ttu-id="b934e-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b934e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b934e-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b934e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b934e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b934e-138">CommonParameters</span></span>
<span data-ttu-id="b934e-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b934e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b934e-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b934e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b934e-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b934e-141">INPUTS</span></span>

### <span data-ttu-id="b934e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b934e-142">System.String</span></span>

### <span data-ttu-id="b934e-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b934e-143">System.Guid</span></span>

### <span data-ttu-id="b934e-144">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="b934e-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="b934e-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b934e-145">OUTPUTS</span></span>

### <span data-ttu-id="b934e-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b934e-146">System.Boolean</span></span>

## <span data-ttu-id="b934e-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="b934e-147">NOTES</span></span>
<span data-ttu-id="b934e-148">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="b934e-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b934e-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b934e-149">RELATED LINKS</span></span>

[<span data-ttu-id="b934e-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b934e-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="b934e-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b934e-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="b934e-152">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b934e-152">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="b934e-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b934e-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

