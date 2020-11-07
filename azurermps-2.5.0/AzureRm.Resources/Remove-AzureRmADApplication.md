---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 73aa80f7d42a2ad29b0e5af0ae5e0e6340691733
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914686"
---
# <span data-ttu-id="1885f-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1885f-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="1885f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1885f-102">SYNOPSIS</span></span>
<span data-ttu-id="1885f-103">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1885f-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1885f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1885f-104">SYNTAX</span></span>

### <span data-ttu-id="1885f-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1885f-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1885f-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1885f-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1885f-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1885f-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1885f-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1885f-108">InputObjectParameterSet</span></span>
```
Remove-AzureRmADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1885f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1885f-109">DESCRIPTION</span></span>
<span data-ttu-id="1885f-110">Удаляет приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1885f-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="1885f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1885f-111">EXAMPLES</span></span>

### <span data-ttu-id="1885f-112">Пример 1: Удаление приложения по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="1885f-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="1885f-113">Удаляет приложение с идентификатором объекта "b4cd1619-80b3-4cfb-9f8f-9f2333425738" из клиента.</span><span class="sxs-lookup"><span data-stu-id="1885f-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="1885f-114">Пример 2: Удаление приложения по идентификатору приложения</span><span class="sxs-lookup"><span data-stu-id="1885f-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="1885f-115">Удаляет приложение с идентификатором приложения "f9c5ea4f-28f0-401A-a491-491a037fa346" из клиента.</span><span class="sxs-lookup"><span data-stu-id="1885f-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="1885f-116">Пример 3-Удаление приложения с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="1885f-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzureRmADApplication
```

<span data-ttu-id="1885f-117">Возвращает приложение с идентификатором объекта "b4cd1619-80b3-4cfb-9f8f-9f2333425738" и каналами, которые должны быть удалены из клиента с помощью командлета Remove-AzureRmADApplication.</span><span class="sxs-lookup"><span data-stu-id="1885f-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzureRmADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="1885f-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1885f-118">PARAMETERS</span></span>

### <span data-ttu-id="1885f-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1885f-119">-ApplicationId</span></span>
<span data-ttu-id="1885f-120">Идентификатор приложения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1885f-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="1885f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1885f-121">-DefaultProfile</span></span>
<span data-ttu-id="1885f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1885f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1885f-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1885f-123">-DisplayName</span></span>
<span data-ttu-id="1885f-124">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="1885f-124">The display name of the application.</span></span>

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

### <span data-ttu-id="1885f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="1885f-125">-Force</span></span>
<span data-ttu-id="1885f-126">Переключение на удаление приложения без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1885f-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="1885f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1885f-127">-InputObject</span></span>
<span data-ttu-id="1885f-128">Объект, представляющий приложение, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1885f-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="1885f-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1885f-129">-ObjectId</span></span>
<span data-ttu-id="1885f-130">Идентификатор объекта приложения, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1885f-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="1885f-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1885f-131">-PassThru</span></span>
<span data-ttu-id="1885f-132">Если указать это, будет возвращено значение истина, если команда была выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1885f-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1885f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1885f-133">-Confirm</span></span>
<span data-ttu-id="1885f-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1885f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1885f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1885f-135">-WhatIf</span></span>
<span data-ttu-id="1885f-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1885f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1885f-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1885f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1885f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1885f-138">CommonParameters</span></span>
<span data-ttu-id="1885f-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1885f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1885f-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1885f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1885f-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1885f-141">INPUTS</span></span>

### <span data-ttu-id="1885f-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1885f-142">System.Guid</span></span>

### <span data-ttu-id="1885f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1885f-143">System.String</span></span>

### <span data-ttu-id="1885f-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="1885f-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="1885f-145">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1885f-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1885f-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1885f-146">OUTPUTS</span></span>

### <span data-ttu-id="1885f-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1885f-147">System.Boolean</span></span>

## <span data-ttu-id="1885f-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="1885f-148">NOTES</span></span>
<span data-ttu-id="1885f-149">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, ресурс, группа, шаблон, развертывание</span><span class="sxs-lookup"><span data-stu-id="1885f-149">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1885f-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1885f-150">RELATED LINKS</span></span>

[<span data-ttu-id="1885f-151">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1885f-151">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="1885f-152">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1885f-152">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)



[<span data-ttu-id="1885f-153">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1885f-153">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

